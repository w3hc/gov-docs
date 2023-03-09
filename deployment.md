---
title: Deployment
layout: home
nav_order: 40
---

# Deployment

Before you deploy your DAO, you should ask yourself the following questions: 

- What is the objective of your DAO?
- What kind of proposals do you expect?
- Who are the first members? 

## Guide

A complete tutorial and a 'one-click deployment' app are both on our to-do list, but if you want to deploy your DAO right now feel very free to contact Julien directly via [Element](https://matrix.to/#/@julienbrg:matrix.org), [Telegram](https://t.me/julienbrg), [Twitter](https://twitter.com/julienbrg), [Discord](https://discord.gg/xw9dCeQ94Y), or [LinkedIn](https://www.linkedin.com/in/julienberanger/).

## Checklist

{: .warning }
For security reasons, the `votingPeriod` is denominated in **number of blocks**. By default, it's set to `300` (a few minutes) for testing purposes. The Web3 Hackers Collective has it set to 40320 (6 days on pre-Bedrock Optimism Mainnet). Two weeks is often recommended. You can calculate it using the explorer of a given network.

- Make sure the addresses of the first members are correct
- Edit the value of the `metadata` variable
- Run the `deploy-nft.ts` script
- Edit the manifesto
- In `deploy-gov.ts`, make sure the `name`, `votingDelay`, `votingPeriod`, `votingThreshold` and `quorum` variables are correctly set
- Run the `deploy-gov.ts` script
- Transfer the NFT contract ownership to Gov
- Add the DAO to Tally
- Each member can delegate to self
- You can vote a Manifesto and NFT metadata update to include the DAO contract address

## Commands

### Deploy to Goerli

```
npm run deploy
```

Alternatively, you can run: 

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network goerli
npx hardhat run scripts/deploy-gov.ts --network goerli
```

### Deploy to Optimism Goerli

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network optimism-goerli
npx hardhat run scripts/deploy-gov.ts --network optimism-goerli
```

### Deploy to Arbitrum Goerli

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network arbitrum-goerli
npx hardhat run scripts/deploy-gov.ts --network arbitrum-goerli
```

### Deploy to Optimism Mainnet

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network optimism
npx hardhat run scripts/deploy-gov.ts --network optimism
```

## Use

### Upload the NFT metadata

Edit the metadata in `upload-metadata.ts`, then:

```
npx hardhat run scripts/upload-metadata.ts
```

### Upload the manifesto

Edit the `manifesto.md` file, then:

```
npx hardhat run scripts/upload-manifesto.ts
```

Note that you can put a whole website in the manifesto directory, the result will be the same: you'll get the CID of your manifesto.

### Submit a proposal

Edit the `submit-proposal.ts` file, then:

```
npx hardhat run scripts/submit-proposal.ts --network goerli
```

Note that you can put a whole website in the manifesto directory, the result will be the same: you'll get the CID of your manifesto.