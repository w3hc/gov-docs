---
title: Home
layout: home
nav_order: 1
---

# Welcome! ✨

[Gov](https://github.com/w3hc/gov-docs) is a DAO template built with Open Zeppelin's Governor contract in combination with NFTs.

The goal of the project is to provide a coordination tool that fits the needs of everyday people.

[View a test DAO on Tally](https://www.tally.xyz/gov/eip155:5:0x690C775dD85365a0b288B30c338ca1E725abD50E){: .btn .btn-purple }

## Features

- [DAO membership NFTS (ERC-721)](/#dao-membership-nfts)
- [On-chain voting system (Governor)](/#on-chain-voting-system)
- [Members vote to add or ban a member](/#members-vote-to-add-or-ban-a-member)
- [Easy to config, deploy and run](/#easy-to-config-deploy-and-run)
- [Fully compatible with Tally](/#fully-compatible-with-tally)
- [Extreme composability/modularity](/#extreme-composabilitymodularity)
- [Upgradeable governance settings](/#upgradeable-governance-settings)

### DAO membership NFTS

The membership of your DAO is represented by an NFT. One person, one vote. This NFT is customizable: you can submit a proposal to modify the metadata of your NFT. 

### On-chain voting system

Open Zeppelin's Governor contract defines the voting rules: it allows members to cast a their vote, it counts the votes and execute the proposal if successful.

### Members vote to add or ban a member

You can add or ban a member of the DAO by submitting a proposal. 

### Easy to config, deploy and run

Gov is one of the easiest existing way to launch a secure and scalable DAO. 

### Fully compatible with Tally

You can use [Tally](https://www.tally.xyz/) to monitor your DAO. 

### Extreme composability/modularity

The Governor contract allows us to trigger custom on-chain actions. When you deploy a Solidity contract and transfer its ownership to the Gov, the DAO is the only entity allowed to interact with functions marked `onlyOwner`. The [plugins](/plugins.html) are optional functionalities you can add to your DAO.

### Upgradeable governance settings

You can upgrade the voting parameters by a community vote. Learn more about the [vote settings](/vote-settings.html).  