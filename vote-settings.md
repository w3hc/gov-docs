---
title: Vote settings
layout: home
nav_order: 35
---

# Vote settings

Gov includes an on-chain voting system where only the owner of a given NFT is allowed to vote. 

One member, one vote.

## Default settings

{: .warning }
The current voting period is set to 100 blocks (only a few minutes) for testing purposes. It's important to give people enough time to vote. 

- Voting delay: `1` (1 block)
- Voting period: `100` (100 blocks)
- Quorum: `20` (20%)
- Proposal threshold: `1` (1 NFT)

The **voting delay** is the delay since proposal is created until voting starts.

The **voting period** is the length of the period during which people can cast their vote.

The **quorum** is the minimum required number of votes in proportion to the total voting power. 

The **proposal threshold** is the minimum number of votes an account must have to create a proposal.

## Guide

### Voting delay

It is recommended to set it to `1` so that the members can vote right after the proposal is submitted.

### Voting period

[content required]

### Quorum

If the participation rate on a given proposal is below the quorum, the proposal can't pass. Most of DAOs' quorum is pretty low (often 4%). That said, the delegation system we have in place can help improve the participation rate: once a member delegated their voting power to a delegate, he/she just don't need to vote.

### Proposal threshold

Set it to `1` if you want only the members to be allowed to submit a proposal. Set it to `0` if you want to allow anyone (including non-members) to submit a proposal. Keep it mind that if anyone can submit a proposal it exposes the DAO to spam proposals, which can be an issue. 

## Delegation

You can delegate your voting power to another member. This can be changed at any time, so if you're not happy with your delegate vote you can delegate to yourself or to another member. DAOs make it easy to practice [liquid democracy](https://en.wikipedia.org/wiki/Liquid_democracy#:~:text=The%20concept%20of%20liquid%20democracy,a%20trusted%20person%20or%20party.), it was hardly feasible before. 

## Resources

To learn more about Open Zeppelin's Governor contract and how to set it up: [How to set up on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance)
