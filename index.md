---
title: Home
layout: home
nav_order: 1
---

# Welcome! ✨

[Gov](https://github.com/w3hc/gov) is a DAO framework built with Open Zeppelin's Governor contract in combination with NFTs. It provides **a coordination tool that fits the needs of everyday people**.

We're inviting orgs, federations of orgs, activists, neighborhoods, stewards of the commons, collectives, and all communities to create their own DAO. The [Web3 Hackers Collective](https://www.tally.xyz/gov/web3-hackers-collective) has recently released the [v0.10.0](https://github.com/w3hc/gov/releases/tag/v0.10.0) of Gov. We want to run a series of [pilots](./pilots.html) and **focus on the impact evaluation process** of each DAO.

Gov is fully compatible with [Tally](https://www.tally.xyz/), and you can also use [Gov UI](https://github.com/w3hc/gov-ui) `v0.10.1` (view the [deployment](./deployment.html) section). You can test the web app here: 

[Test Gov UI](https://gov-ui.netlify.app/){: .btn .btn-green }

**You don't need any wallet or ETH to test it!** 

## Deploy your own DAO

You can find the deployment checklist [here](./deployment.html#checklist). Once you decided about (1) your mission statement, (2) the types of proposals you expect, and (3) the [vote settings](./vote-settings.html#guide), we can take an hour to deploy your DAO to the network of your choice. Feel very free to contact Julien directly via [Element](https://matrix.to/#/@julienbrg:matrix.org), [Telegram](https://t.me/julienbrg), [Twitter](https://twitter.com/julienbrg), [Discord](https://discord.com/invite/uSxzJp3J76), or [LinkedIn](https://www.linkedin.com/in/julienberanger/).

 {: .custom }
You can use Gov Deployer but it is currently under development. 

[Deploy your own DAO](gov-deployer.netlify.app){: .btn .btn-purple } 

## Features

- [DAO membership NFTS (ERC-721)](./#dao-membership-nfts)
- [On-chain voting system (Governor)](./#on-chain-voting-system)
- [Customizable interface with email login](./#customizable-interface-with-email-login)
- [Members vote to add or ban a member](./#members-vote-to-add-or-ban-a-member)
- [Timestamp-based](./#timestamp-based)
- [Easy to config, deploy and run](./#easy-to-config-deploy-and-run)
- [Fully compatible with Tally](./#fully-compatible-with-tally)
- [Extreme composability/modularity](./#extreme-composabilitymodularity)
- [Upgradeable governance settings](./#upgradeable-governance-settings)

### DAO membership NFTS

The membership of your DAO is represented by an NFT. One person, one vote. These NFTs can be viewed as 'membership cards'. They're customizable: you can submit a proposal to modify the metadata of your NFT.

Since `v0.10.0`, these NFTs are non-transferable by default ("SBT"). 

### On-chain voting system

Open Zeppelin's Governor contract defines the voting rules: it allows members to cast a their vote, it counts the votes and execute the proposal if successful.

### Customizable interface with email login

In addition to Tally interface, you can get your own web app (website). The users, members of your DAO, don't need any wallet to submit proposals, vote, delegate their voting power, etc. 

### Members vote to add or ban a member

You can add or ban a member of the DAO by submitting a proposal. 

### Timestamp-based

Gov is timestamp-based by default, as opposed to `blockNumber`-based. 

### Easy to config, deploy and run

Gov is one of the easiest existing way to launch a secure and scalable DAO. 

### Fully compatible with Tally

You can use [Tally](https://www.tally.xyz/) to monitor your DAO, submit proposal and vote. 

### Extreme composability/modularity

The Governor contract allows us to trigger custom on-chain actions. When you deploy a Solidity contract and transfer its ownership to the Gov, the DAO is the only entity allowed to interact with functions marked `onlyOwner`. The [plugins](./plugins.html) are optional functionalities you can add to your DAO.

### Upgradeable governance settings

You can upgrade the voting parameters by a community vote. Learn more about the [vote settings](./vote-settings.html).

## Supported networks

We're currently supporting the following networks: 

- Optimism Mainnet
- Optimism Sepolia Testnet
- Sepolia
- Arthera Testnet 

## Github repositories

- [gov](https://github.com/w3hc/gov)
- [gov-ui](https://github.com/w3hc/gov-ui)
- [gov-deployer](https://github.com/w3hc/gov-deployer)
- [gov-docs](https://github.com/w3hc/gov-docs)

[Have a look at our current to-do list](https://github.com/orgs/w3hc/projects/8/views/9){: .btn .btn-green }