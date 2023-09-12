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

[Deploy your own DAO](https://gov-deployer.on.fleek.co/){: .btn .btn-purple }

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

### Deploy to Optimism Mainnet

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network optimism
npx hardhat run scripts/deploy-gov.ts --network optimism
```

### Deploy to Optimism Goerli Testnet

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network optimism-goerli
npx hardhat run scripts/deploy-gov.ts --network optimism-goerli
```

### Deploy to Arbitrum Goerli Testnet

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network arbitrum-goerli
npx hardhat run scripts/deploy-gov.ts --network arbitrum-goerli
```

### Deploy to Celo Mainnet

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network celo
npx hardhat run scripts/deploy-gov.ts --network celo
```

### Deploy to Celo Alfajores Testnet

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network alfajores
npx hardhat run scripts/deploy-gov.ts --network alfajores
```

### Deploy to Gnosis Mainnet

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network gnosis
npx hardhat run scripts/deploy-gov.ts --network gnosis
```

### Deploy to Gnosis Chiado Testnet

```
npx hardhat run scripts/deploy-nft.ts --network chiado
npx hardhat run scripts/deploy-gov.ts --network chiado
```

### Deploy to Base Goerli Testnet

```
npx hardhat run scripts/deploy-nft.ts --network base-goerli
npx hardhat run scripts/deploy-gov.ts --network base-goerli
```

### Deploy to Mantle Testnet

```
npx hardhat run scripts/clear.ts
npx hardhat run scripts/deploy-nft.ts --network mantle-testnet
npx hardhat run scripts/deploy-gov.ts --network mantle-testnet
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