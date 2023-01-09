---
description: Information about the Decentralized Autonomous Organization (DAO) of AGFI
cover: >-
  https://images.unsplash.com/photo-1523292562811-8fa7962a78c8?crop=entropy&cs=tinysrgb&fm=jpg&ixid=MnwxOTcwMjR8MHwxfHNlYXJjaHwxfHxnb3Zlcm5tZW50fGVufDB8fHx8MTY1Njk0MjQ4Mw&ixlib=rb-1.2.1&q=80
coverY: 0
---

# DAO

The AGFI project uses a decentralized autonomous organization (DAO) to manage its operations. This means that instead of having a traditional development team, the project is managed by a group of decentralized participants who come together to make decisions about the direction of the project.

One of the key benefits of using a DAO is that it removes the need for a central authority to make decisions about the project. Instead, all decisions are made through a democratic process, with the community having the ability to vote on proposals and determine the direction of the project.

In addition to managing the project, the AGFI DAO also controls the treasury assets of the project. This includes any funds raised through fundraising efforts, as well as any assets that are generated through the project's operations. All decisions related to the treasury assets are made through the same democratic process as other decisions, ensuring that the community has complete control over how these assets are used.

Overall, the use of a DAO allows the AGFI project to be completely decentralized and community-controlled. This ensures that all decisions are made transparently and democratically, with the community having full control over the direction of the project and the management of its treasury assets.

AGFI Decentralized Governance is currently managed on GitHub using a dedicated repository using Issues to track each proposal.

## Guides

{% content-ref url="../guides/proposals.md" %}
[proposals.md](../guides/proposals.md)
{% endcontent-ref %}

{% content-ref url="../guides/voting.md" %}
[voting.md](../guides/voting.md)
{% endcontent-ref %}

## Interface

All AGFI V3 contracts are implementations of OpenZeppelin standards, and so Tally has been used for DAO management:

{% embed url="https://www.tally.xyz/governance/eip155:1:0xD243F9aAfCf32e60b2e9D0FF016cf7f1552d5952" %}

Snapshot is also used for some DAO votes:

{% embed url="https://snapshot.org/#/aggregatedfinance.eth" %}

## Timelock

Derived from OpenZeppelin Contracts (last updated v4.6.0) (governance/TimelockController.sol)

{% embed url="https://github.com/aggregatedfinance/agfi-contracts/blob/main/contracts/Timelock.sol" %}

{% embed url="https://etherscan.io/address/0x97eee9c5b9a4b089813365ccf0315c4e9aa6f516#code" %}

## Governor

Derived from OpenZeppelin Contracts (last updated v4.6.0) (governance/Governor.sol)

Implements Governor, GovernorSettings, GovernorCompatibilityBravo, GovernorVotes, GovernorVotesQuorumFraction, and GovernorTimelockControl.

{% embed url="https://github.com/aggregatedfinance/agfi-contracts/blob/main/contracts/Governor.sol" %}

{% embed url="https://etherscan.io/address/0xd243f9aafcf32e60b2e9d0ff016cf7f1552d5952#code" %}
