---
title: Home
layout: home
nav_order: 1
---

# Welcome! ✨

[Gov](https://github.com/w3hc/gov) is a DAO framework built with Open Zeppelin's Governor contract in combination with NFTs.

The goal of the project is to provide **a coordination tool that fits the needs of everyday people**.

We're inviting orgs, federations of orgs, activists, neighborhoods, stewards of the commons, collectives, and all communities to create their own DAO. The [Web3 Hackers Collective](https://github.com/w3hc) is about to release the [beta version](https://github.com/w3hc/gov/milestone/3) of [Gov](https://github.com/w3hc/gov). We'll run **five different pilots** and focus exclusively on the impact evaluation process of each DAO. 

[Gov](https://github.com/w3hc/gov) can be viewed as a retroactive funding tool: people can use it to **fund on-the-ground actions that has already been delivered** (as opposed to funding actions *planned in the future*).

## Deployment

You can find the deployment checklist [here](./deployment.html#checklist). For the moment we don't provide a no-code interface to launch your DAO, so once you decided about (1) your mission statement, (2) the types of proposals your collective is willing to vote, and (3) the [vote settings](./vote-settings.html#guide), we can take an hour to deploy your DAO to the network of your choice. Feel very free to contact Julien directly via [Element](https://matrix.to/#/@julienbrg:matrix.org), [Telegram](https://t.me/julienbrg), [Twitter](https://twitter.com/julienbrg), [Discord](https://discord.gg/xw9dCeQ94Y), or [LinkedIn](https://www.linkedin.com/in/julienberanger/).

Once your DAO is deployed, you can use [Tally](https://www.tally.xyz/) to submit proposals and vote. 

## Features

- [DAO membership NFTS (ERC-721)](./#dao-membership-nfts)
- [On-chain voting system (Governor)](./#on-chain-voting-system)
- [Members vote to add or ban a member](./#members-vote-to-add-or-ban-a-member)
- [Easy to config, deploy and run](./#easy-to-config-deploy-and-run)
- [Fully compatible with Tally](./#fully-compatible-with-tally)
- [Extreme composability/modularity](./#extreme-composabilitymodularity)
- [Upgradeable governance settings](./#upgradeable-governance-settings)

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

The Governor contract allows us to trigger custom on-chain actions. When you deploy a Solidity contract and transfer its ownership to the Gov, the DAO is the only entity allowed to interact with functions marked `onlyOwner`. The [plugins](./plugins.html) are optional functionalities you can add to your DAO.

### Upgradeable governance settings

You can upgrade the voting parameters by a community vote. Learn more about the [vote settings](./vote-settings.html).  