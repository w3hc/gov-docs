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

## Deploy from UI

No tech required. 

[Deploy your own DAO](https://gov-deployer.on.fleek.co/){: .btn .btn-purple }

## Deploy from repository

- Clone [Gov repository](https://github.com/w3hc/gov) locally
- Make sure the addresses of the first members are correct
- Edit and upload the membership NFT `metadata`
- Edit and upload the manifesto
- Edit the `dao.config.ts` file
- Run this command: `pnpm deploy:sepolia` 
- Add the DAO to Tally
- Each member can delegate to self

