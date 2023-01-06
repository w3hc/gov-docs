---
title: Plugins
layout: home
nav_order: 80
---

# Plugins

The Governor contract allows us to trigger custom on-chain actions. When you deploy a Solidity contract and transfer its ownership to the Gov, the DAO is the only entity allowed to interact with functions marked `onlyOwner`. The plugins are optional functionalities you can add to your DAO.

We have a long list of plugins to be built. Feel free to join [our Discord](https://discord.gg/bHKJV3NWUQ) if you have ideas to share.

## Roadmap

We're planning to release the following three plugins:

### Vault

Gov is already fully compatible with [Gnosis Safe](https://help.tally.xyz/article/42-what-is-a-gnosis-safe) but we might want to use a special vault which would allow donors to **take back their donation**. They would do that if they're not happy with one of the proposals (upcoming, active or passed). 

If some money were spent in the meantime, people who donated could withdraw proportionally.

### Hypercerts

> Hypercerts are a tool to build scalable retrospective reward systems for impact.

[https://hypercerts.xyz/](https://hypercerts.xyz/)

Since the DAO members do the work of verifying every proposal, it can make sense to issue a hypercert when the proposal is executed. Fractions of these could then be sold.

### Onbording

As of now, only a community vote can add a new member. We're working on a plugin that would allow the following workflow: 

- Alice wants to join the DAO
- A member sends her a link
- She gets her membership NFT

Alice will need to have MetaMask installed, BUT she wouldn't need to buy any ETH to withdraw her NFT and become a member.

## Under dev

You can find the draft plugins in the [`/contracts/plugins`](https://github.com/w3hc/gov/tree/main/contracts/plugins) directory. Please note they're unsafe to use right now.

### [HypercertsMock.sol](https://github.com/w3hc/gov/blob/main/contracts/mocks/ERC1155Mock.sol)

For now, I'm using an ERC-721 to mimick the behavior of [Hypercerts](https://network-goods.github.io/hypercerts-docs/), which is using [ERC-3525](https://eips.ethereum.org/EIPS/eip-3525). A future integration of Hypercerts is being considered.

A hypercert represents the contribution verified and voted by the DAO members. Fractions are automatically put for sale.

### [Shop.sol](https://github.com/w3hc/gov/blob/main/contracts/plugins/Shop.sol)

Allows to buy a fraction of a hypercert. The proceeds are automatically transferred to the the vault, meaning they can be withdrawn by the donors.

### [Vault.sol](https://github.com/w3hc/gov/blob/main/contracts/plugins/Vault.sol)

Supports USDC only.

Allow donors to take back their donation when they want to. If the DAO spent some funds in the meantime, they can withdraw USDC proportionally to what's left in the vault.

Those who donated to the vault can either withdraw the proceeds (USDC) or withdraw a fraction of the hypercert.

Please note that Gov is already fully compatible with [Gnosis Safe](https://help.tally.xyz/article/42-what-is-a-gnosis-safe).

### [ERC4626.sol](https://github.com/w3hc/gov/blob/main/contracts/plugins/ERC4626.sol)

This is the [OZ implementation](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/extensions/ERC4626.sol) of the [ERC-4626](https://eips.ethereum.org/EIPS/eip-4626), which is considered to replace the vault.
