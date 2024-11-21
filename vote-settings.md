---
title: Vote settings
layout: home
nav_order: 35
---

# Vote settings

Gov includes an on-chain voting system where only the owner of a given NFT is allowed to vote. 

One person, one vote.

## Default settings

- Voting delay: `0` (0 second)
- Voting period: `1296000` (15 days)
- Quorum: `20` (20%)
- Proposal threshold: `1` (1 NFT)

The **voting delay** is the delay since proposal is created until voting starts. It allows members to move their tokens (if relevant) before the snapshot. It's usually set to 0.

The **voting period** is the length of the period during which people can cast their vote.

The **quorum** is the minimum required number of votes in proportion to the total voting power. 

The **proposal threshold** is the minimum number of votes an account must have to create a proposal. If set to `1`, it means that you must own a membership NFT to submit a proposal. If set to `0` anyone can submit proposals, exposing the DAO to spam proposals. 

## Guide

### Voting delay

It is recommended to set it to `0` so that the members can vote right after the proposal is submitted.

### Voting period

It's important to give people enough time to vote. 15 days (`1296000` seconds) can be an acceptable timeframe. 

### Quorum

If the participation rate on a given proposal is below the quorum, the proposal can't pass. Most of DAOs' quorum is pretty low (often 4%). That said, the delegation system we have in place can help improve the participation rate: once a member delegated their voting power to a delegate, he/she just don't need to vote.

### Proposal threshold

Set it to `1` if you want only the members to be allowed to submit a proposal. Set it to `0` if you want to allow anyone (including non-members) to submit a proposal. Keep it mind that if anyone can submit a proposal it exposes the DAO to spam proposals, which can be an issue. 

## Delegation

You can delegate your voting power to another member. This can be changed at any time, so if you're not happy with your delegate vote you can delegate to yourself or to another member.

## Resources

You can learn more about Open Zeppelin's Governor contract and how to set it up here: [How to set up on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance). You can also browse [Tally docs](https://docs.tally.xyz/user-guides/deploying-daos/deploy-a-dao-with-token-voting). 
