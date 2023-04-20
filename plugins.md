---
title: Plugins
layout: home
nav_order: 70
---

# Plugins

The Governor contract allows us to trigger custom on-chain actions. When you deploy a Solidity contract and transfer its ownership to the Gov, the DAO is the only entity allowed to interact with functions marked `onlyOwner`. The plugins are optional functionalities you can add to your DAO.

We have a long list of plugins to be built. Feel free to join [our Discord](https://discord.com/invite/uSxzJp3J76) if you have ideas to share.

To add a plugin to your DAO, you would: 

1. Deploy the contract
2. Transfer the ownership to the DAO

Once it's in place, the community can interact with it via a proposal.

## Roadmap

We're planning to release the following three plugins:

### Vault

Gov is already fully compatible with [Gnosis Safe](https://help.tally.xyz/article/42-what-is-a-gnosis-safe) but we might want to use a special vault which would allow funders to **take back their donation**. They would do that if they're not happy with one of the proposals. 

If some money were spent in the meantime, people who donated can just take their USDC back.

### Hypercerts

> Hypercerts are a tool to build scalable retrospective reward systems for impact.

[https://hypercerts.xyz/](https://hypercerts.xyz/)

Since the DAO members (aka 'auditors') do the work of verifying every proposals, it makes sense to issue a hypercert when the proposal is executed. Fractions of these could then be sold.

## Contracts

You can find the draft plugins in the [`/contracts/plugins`](https://github.com/w3hc/gov/tree/main/contracts/plugins) directory. Please note they're unsafe to use right now.

### [HypercertsMock.sol](https://github.com/w3hc/gov/blob/main/contracts/mocks/ERC1155Mock.sol)

For now, I'm using an ERC-721 to mimick the behavior of [HypercertMinter](https://goerli.etherscan.io/address/0x822f17a9a5eecfd66dbaff7946a8071c265d1d07#code).

A hypercert represents the contribution verified by the DAO members (aka 'auditors').

### [Vault2.sol](https://github.com/w3hc/gov/blob/main/contracts/plugins/Vault2.sol)

Supports USDC only.

Allow funders to take back their donation when they want to. If the DAO spent some funds in the meantime, they can withdraw USDC proportionally to what's left in the vault. Funders can also mint the hypercert associated with a given proposal.
