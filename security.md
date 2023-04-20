---
title: Security
layout: home
nav_order: 40
---

# Security

Here are the differences between the Governor/ERC-721 implementations suggested by Open Zeppelin and ours:

### [Gov.sol](https://github.com/w3hc/gov/blob/main/contracts/Gov.sol)

The following function is `onlyGovernance`, meaning it can only be triggered by a vote.

- `setManifesto()` updates the CID.

### [NFT.sol](https://github.com/w3hc/gov/blob/main/contracts/NFT.sol)

The following functions are `onlyOwner`, and since the NFT contract ownership is transfered to the Gov contract, they can only be triggered by a vote.

- `safeMint()` adds a new member.
- `govBurn()` adds to ban a member.
- `setMetadata()` changes the tokenURI of a given NFT ID.