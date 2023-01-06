---
title: Home
layout: home
nav_order: 1
---

# Welcome! ✨

[Gov](https://github.com/w3hc/gov-docs) is a DAO template built with Open Zeppelin's Governor contract in combination with NFTs.

The goal of the project is to **provide a coordination tool that fits the needs of everyday people**. Orgs, federations of orgs, activists, neighborhoods, stewards of the commons, collectives, and other communities can use to organize themselves.

We want DAOs to be secure, scalable and easy to use.

[View a test DAO on Tally](https://www.tally.xyz/gov/eip155:5:0x690C775dD85365a0b288B30c338ca1E725abD50E){: .btn .btn-purple }

## Intro

In a [recent post](http://bafybeieaa73llmb6bkq5dau4k2goj5joc5yfqreloowy3aysfcjrsjmqb4.ipfs.localhost:8080/general/2022/09/20/daos.html), Vitalik Buterin wrote: 

> A system that directs funding for a particular cause - whether [Optimism retroactive funding](https://medium.com/ethereum-optimism/retroactive-public-goods-funding-33c9b7d00f0c), [VitaDAO](https://www.vitadao.com/), [UkraineDAO](https://ukrainedao.love/) or something else - is optimizing for a much more complicated purpose than profit maximization, and so an alignment solution other than shareholder profit is needed to make sure it keeps using the funds for the purpose that was intended.

DAOs are basically communities that set their operating rules on-chain, meaning that no one except the DAO members can modify these rules. It always ways tricky to allow people who are not familiar with the crypto thing to just use these powerful techniques. [Tally](tally.xyz) provides an excellent interface to monitor DAOs, and [Open Zeppelin](https://www.openzeppelin.com/) worked hard to offer a very complete set of smart contracts. Now that the missing parts are finally here, it's time to take advantage of them.

Gov includes one of the strongest voting system in existence. DAO members can vote to:

- Add a member
- Ban a member
- Edit its manifesto
- Allocate the funds of the DAO treasury

"On what do we vote?" would you ask. This depends on your own collective's objective. The **statement of intent** of your DAO can be written in the manifesto, which also includes the criteria for incoming proposals, info about the DAO members, and also some legal aspects related to your DAO. You as an independent and self-organized group of people are technically the only ones allowed to take these executive decisions. 

One member, one vote.

### Features

- DAO membership NFTS (ERC-721)
- On-chain voting system (Governor)
- Members vote to add or ban a member
- Easy to config, deploy and run
- Fully compatible with [Tally](https://www.tally.xyz/)
- Extreme composability/modularity
- Upgradeable governance settings