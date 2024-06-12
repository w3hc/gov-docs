---
title: Changelog
layout: home
nav_order: 100
---

# Changelog

## Gov UI

* Switch to op sepolia by @julienbrg in https://github.com/w3hc/gov-ui/pull/67
* Integrate with Web3 Modal by @julienbrg in https://github.com/w3hc/gov-ui/pull/69
* New deployment by @julienbrg in https://github.com/w3hc/gov-ui/pull/73
* Fix email login by @julienbrg in https://github.com/w3hc/gov-ui/pull/75
* Add subgraph by @julienbrg in https://github.com/w3hc/gov-ui/pull/77
* Fix indexing by @julienbrg in https://github.com/w3hc/gov-ui/pull/80
* Fix error management by @julienbrg in https://github.com/w3hc/gov-ui/pull/82

**Full Changelog**: https://github.com/w3hc/gov-ui/compare/v0.10.0...v0.10.1

## Gov contracts

### [v0.10.0](https://github.com/w3hc/gov/releases/tag/v0.10.0)

- Refactoring
- pnpm support
- automatic verification
- hardhat-deploy
- Ethersjs v6
- SBT (non-transferable NFT) by default
- Timestamp-based by default
- Gov UI finalised
- Gov Deployer refactored (nft.storage support)

### [v0.9.0-beta](https://github.com/w3hc/gov/releases/tag/v0.9.0-beta)

- Fixed the quorum calculation issue
- Added `setManifesto()` in `Gov.sol`
- Added the 1st version of Vault + Hypercerts plugins
- Created **legal** contract to add to the manifesto
- Added comments in Gov and NFT
- Added proposal upload script
- Added tests for nft delegation
- Added scalability test

### [v0.8.0-alpha](https://github.com/w3hc/gov/releases/tag/v0.8.0-alpha)

- Added Manifesto contract
- Added tests for handling ERC-20, ERC-721, ERC-1155
- Added Optimism Testnet
- Made the NFT contract upgradeable
- Made the NFT metadata dynamic (updatable)

### [v0.1](https://github.com/w3hc/gov/releases/tag/v.0.1.0)

- DAO membership NFTS (ERC-721)
- On-chain voting system (Governor)
- Members vote to add or ban a member
- Easy to config, deploy and run
- Fully compatible with [Tally](https://www.tally.xyz/)
- Extreme composability/modularity
- Upgradeable governance settings