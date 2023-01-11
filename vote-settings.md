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
The current voting period is set to 150 blocks (around 45 minutes) for testing purposes. It's important to give people enough time to vote. 

- Voting delay: `1` (1 block)
- Voting period: `150` (150 blocks)
- Quorum: `20` (20%)
- Proposal threshold: `1` (1 NFT)

The **voting delay** is the delay since proposal is created until voting starts.

The **voting period** is the length of the period during which people can cast their vote.

The **quorum** is the minimum number of votes an account must have to create a proposal.

The **proposal threshold** is the minimum number of votes an account must have to create a proposal.

## Resources

To learn more about Open Zeppelin's Governor contract and how to set it up: [How to set up on-chain governance](https://docs.openzeppelin.com/contracts/4.x/governance)
