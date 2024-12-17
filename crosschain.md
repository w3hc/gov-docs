---
title: Crosschain Variant
layout: home
nav_order: 45
---

# Crosschain DAO Implementation

The crosschain variant of Gov enables DAOs to operate across multiple blockchain networks while maintaining consistent governance and membership state. This implementation consists of two main contracts - Gov and NFT - working together to provide cross-chain governance and membership management.

Gov can be deployed at the same contract address to any EVM networks supporting CREATE2. This means you can have identical contract addresses across different networks like Optimism, Arbitrum, and Base, making it easier to manage and interact with your DAO across multiple chains.

## Core Concepts

### Home Chain
- A designated primary chain where governance and membership actions originate
- Identified by the immutable `home` variable in both contracts
- All governance proposals, voting, and membership management must originate here
- Serves as the source of truth for both governance parameters and membership status

## Gov Contract

### Operation Types
```solidity
enum OperationType {
    SET_MANIFESTO,
    UPDATE_VOTING_DELAY, 
    UPDATE_VOTING_PERIOD,
    UPDATE_PROPOSAL_THRESHOLD,
    UPDATE_QUORUM
}
```

### Governance Functions

#### Proof Generation
```solidity
function generateManifestoProof(string memory newManifesto) external view returns (bytes memory)
function generateParameterProof(OperationType operationType, bytes memory value) external view returns (bytes memory)
```
- Generate cryptographic proofs for governance state updates
- Only callable on home chain
- Returns encoded proof data with update details and message digest

#### Proof Verification & Claiming
```solidity
function claimManifestoUpdate(bytes memory proof) external
function claimParameterUpdate(bytes memory proof) external
```
- Verify and apply governance state updates from home chain
- Validate proof data before applying changes

## NFT Contract

### Operation Types
```solidity
enum OperationType {
    MINT,
    BURN,
    SET_METADATA,
    SET_DELEGATION
}
```

### Membership Functions

#### Proof Generation
```solidity
function generateMintProof(uint256 tokenId) external view returns (bytes memory)
function generateBurnProof(uint256 tokenId) external view returns (bytes memory)
function generateMetadataProof(uint256 tokenId, string memory uri) external view returns (bytes memory)
function generateDelegationProof(address delegator, address delegatee) external view returns (bytes memory)
```
- Generate proofs for membership operations
- Only callable on home chain
- Includes token details, ownership, and operation specifics in proof

#### Proof Verification & Claiming
```solidity
function claimMint(bytes memory proof) external
function claimBurn(bytes memory proof) external
function claimMetadataUpdate(bytes memory proof) external
function claimDelegation(bytes memory proof) external
```
- Verify and execute membership operations on secondary chains
- Each operation requires valid proof from home chain

## Cross-chain Synchronization Flow

### Governance Updates
1. Proposal created and voted on home chain
2. Upon successful execution:
   - Parameter is updated on home chain
   - Proof is generated for the update
3. Proof is submitted to other chains via claim functions
4. Secondary chains verify and apply the update

### Membership Operations
1. Membership action (mint/burn/etc.) executed on home chain
2. Proof generated for the operation
3. Proof submitted to secondary chains
4. Operation replicated after proof verification

## Security Features

### Home Chain Restriction
```solidity
modifier onlyHomeChain() {
    require(block.chainid == home, "Operation only allowed on home chain");
    _;
}
```
- Applied to all state-changing operations on both contracts
- Ensures primary operations occur only on designated home chain

### Proof Validation
- Uses keccak256 hashing for all proofs
- Includes contract address and chain-specific data
- Prevents cross-chain and cross-contract replay attacks

## Events

### Gov Contract Events
```solidity
event ManifestoUpdated(string oldManifesto, string newManifesto);
event GovernanceParameterUpdated(
    OperationType indexed operationType,
    uint256 oldValue,
    uint256 newValue
);
```

### NFT Contract Events
```solidity
event MembershipClaimed(uint256 indexed tokenId, address indexed member, address indexed claimer);
event MembershipRevoked(uint256 indexed tokenId, address indexed member);
event MetadataUpdated(uint256 indexed tokenId, string newUri);
event DelegationUpdated(address indexed delegator, address indexed delegate);
event CrosschainDelegationClaimed(address indexed delegator, address indexed delegate, address indexed claimer);
```

## Implementation Example

### Adding a New Member
```typescript
// 1. On Home Chain
// Propose and execute membership mint
await gov.propose([nft.address], [0], [mintCalldata], description);
// After proposal passes and executes:
const proof = await nft.generateMintProof(newTokenId);

// 2. On Secondary Chains
await nft.claimMint(proof);
```

### Updating Governance Parameters
```typescript
// 1. On Home Chain
// Propose and execute parameter update
await gov.propose([gov.address], [0], [updateCalldata], description);
// After proposal passes and executes:
const proof = await gov.generateParameterProof(
    OperationType.UPDATE_VOTING_DELAY,
    encodedNewValue
);

// 2. On Secondary Chains
await gov.claimParameterUpdate(proof);
```

## Security Considerations

1. **Proof Generation**
   - Only possible on home chain
   - Includes contract address and chain ID
   - Prevents replay attacks across chains and contracts

2. **State Consistency**
   - All state changes must originate from home chain
   - Secondary chains only accept proven updates
   - Membership state tracked separately on each chain

3. **Delegation Security**
   - Delegation state synchronized across chains
   - Requires proof verification for cross-chain updates
   - Maintains voting power consistency

## Best Practices

1. **Deployment**
   - Deploy to home chain first
   - Use deterministic deployment for consistent addresses
   - Verify home chain ID configuration
   - Test proof generation and verification before going live

2. **Operation**
   - Monitor events on all chains
   - Verify state consistency periodically
   - Keep records of cross-chain operations
   - Handle failed synchronizations promptly

3. **Maintenance**
   - Regular state verification across chains
   - Monitor for synchronization delays
   - Maintain emergency procedures for critical updates

## Limitations and Considerations

1. **Latency**
   - Cross-chain operations require manual proof submission
   - Updates not automatic across chains
   - May need monitoring and automation systems

2. **Cost**
   - Each chain synchronization requires gas payment
   - Operating on multiple chains increases overall costs
   - Consider gas optimization strategies

3. **Complexity**
   - More complex than single-chain deployment
   - Requires additional monitoring and maintenance
   - Need for proper documentation and training