---
title: Home
layout: home
nav_order: 1
---

# Welcome! ✨

[Gov](https://github.com/w3hc/gov) is a DAO framework built with Open Zeppelin's Governor contract in combination with NFTs. It provides **a coordination tool that fits the needs of everyday people**.

We're inviting orgs, federations of orgs, activists, neighborhoods, stewards of the commons, collectives, and all communities to create their own DAO. The [Web3 Hackers Collective](https://www.tally.xyz/gov/web3-hackers-collective) has recently released the [beta version](https://github.com/w3hc/gov/releases/tag/v0.9.0-beta) of [Gov](https://github.com/w3hc/gov). We want to run five different pilots and **focus exclusively on the impact evaluation process** of each DAO.

[Gov](https://github.com/w3hc/gov) can be viewed as a retroactive funding tool: people can use it to **fund on-the-ground actions that has already been delivered** (as opposed to funding actions *planned in the future*).

Gov is fully compatible with [Tally](https://www.tally.xyz/) (they have the best existing UI in town!)

We're currently supporting the following networks: 

- Optimism Mainnet
- Ethereum Goerli Testnet 
- Optimism Goerli Testnet
- Arbitrum Goerli Testnet

Also, we have successfully tested [Medusa](https://medusanet.xyz/) (Arbitrum Goerli Testnet only for now). This allows anyone to share a document **that can only be decrypted by the members** of a given DAO.

## Roadmap

- Finalize the legal aspects of the project (yes!)
- Integrate with [Hypercerts](https://hypercerts.org/)
- Provide a 'one-click deployment' UI
- Develop the 'dynamic vault' (using the [ERC-4626](https://eips.ethereum.org/EIPS/eip-4626))
- Support other EVM-compatible networks

## Deploy your own DAO

You can find the deployment checklist [here](./deployment.html#checklist). For the moment we don't provide any interface to launch your DAO, so once you decided about (1) your mission statement, (2) the types of proposals your collective is willing to vote, and (3) the [vote settings](./vote-settings.html#guide), we can take an hour to deploy your DAO to the network of your choice. Feel very free to contact Julien directly via [Element](https://matrix.to/#/@julienbrg:matrix.org), [Telegram](https://t.me/julienbrg), [Twitter](https://twitter.com/julienbrg), [Discord](https://discord.gg/xw9dCeQ94Y), or [LinkedIn](https://www.linkedin.com/in/julienberanger/).

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

The membership of your DAO is represented by an NFT. One person, one vote. These NFTs can be viewed as 'membership cards'. They're customizable: you can submit a proposal to modify the metadata of your NFT.

### On-chain voting system

Open Zeppelin's Governor contract defines the voting rules: it allows members to cast a their vote, it counts the votes and execute the proposal if successful.

### Members vote to add or ban a member

You can add or ban a member of the DAO by submitting a proposal. 

### Easy to config, deploy and run

Gov is one of the easiest existing way to launch a secure and scalable DAO. 

### Fully compatible with Tally

You can use [Tally](https://www.tally.xyz/) to monitor your DAO, submit proposal and vote. 

### Extreme composability/modularity

The Governor contract allows us to trigger custom on-chain actions. When you deploy a Solidity contract and transfer its ownership to the Gov, the DAO is the only entity allowed to interact with functions marked `onlyOwner`. The [plugins](./plugins.html) are optional functionalities you can add to your DAO.

### Upgradeable governance settings

You can upgrade the voting parameters by a community vote. Learn more about the [vote settings](./vote-settings.html).