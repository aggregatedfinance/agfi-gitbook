---
description: Information about the Decentralized Autonomous Organization (DAO) of AGFI
cover: >-
  https://images.unsplash.com/photo-1523292562811-8fa7962a78c8?crop=entropy&cs=tinysrgb&fm=jpg&ixid=MnwxOTcwMjR8MHwxfHNlYXJjaHwxfHxnb3Zlcm5tZW50fGVufDB8fHx8MTY1Njk0MjQ4Mw&ixlib=rb-1.2.1&q=80
coverY: 0
---

# DAO

AGFI Decentralized Governance is currently managed on GitHub using a dedicated repository using Issues to track each proposal.

### Interface

All AGFI V3 contracts are implementations of OpenZeppelin standards, and so Tally has been used for DAO management.

{% embed url="https://www.tally.xyz/governance/eip155:1:0xD243F9aAfCf32e60b2e9D0FF016cf7f1552d5952" %}

### Timelock

Derived from OpenZeppelin Contracts (last updated v4.6.0) (governance/TimelockController.sol)

{% embed url="https://github.com/aggregatedfinance/agfi-contracts/blob/main/contracts/Timelock.sol" %}

{% embed url="https://etherscan.io/address/0x97eee9c5b9a4b089813365ccf0315c4e9aa6f516#code" %}

### Governor

Derived from OpenZeppelin Contracts (last updated v4.6.0) (governance/Governor.sol)

Implements Governor, GovernorSettings, GovernorCompatibilityBravo, GovernorVotes, GovernorVotesQuorumFraction, and GovernorTimelockControl.

{% embed url="https://github.com/aggregatedfinance/agfi-contracts/blob/main/contracts/Governor.sol" %}

{% embed url="https://etherscan.io/address/0xd243f9aafcf32e60b2e9d0ff016cf7f1552d5952#code" %}
