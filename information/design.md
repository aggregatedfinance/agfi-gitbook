---
cover: >-
  https://images.unsplash.com/photo-1523726491678-bf852e717f6a?crop=entropy&cs=tinysrgb&fm=jpg&ixid=MnwxOTcwMjR8MHwxfHNlYXJjaHw0fHxkZXNpZ258ZW58MHx8fHwxNjU3MTU5MDY2&ixlib=rb-1.2.1&q=80
coverY: 0
---

# Design

## Introduction

Aggregated Finance (AGFI) is a DAO-based platform for community funds management. The DAO votes to delegate its treasury to one or more traders, and the traders. The AGFI contract collects fees on each Uniswap AGFI token swap, and distributes the fees according to various purposes defined as "Tax Channels".

The AGFI DAO also votes to control the token contract parameters, adjusting tax channel functions and rates.

## Contract

The AGFI contact is a derivative of the Reimagined Finance (ReFi) token contract. This contract was chosen as it met most of the needs of the AGFI V3 contract, with the extensions made to increase the number of tax channels.

The AGFI contract additionally incorporates ERC20Votes and ERC20Snapshot, allowing for it to be bound to Governor contracts for DAO management.

{% hint style="info" %}
The ReFi project was subject to an attack that resulted in contract ownership being stolen. This attack was the result of weak cryptography used in the contract deployer keys and is not applicable to the AGFI contracts.
{% endhint %}

## Tokenomics

AGFI V3 is a 1-for-1 relaunch of the original AGFI, launching with a token supply of 1 Trillion (1,000,000,000,000) tokens. 1-for-1 tokens were airdropped to all V1 and V2 token holders to replace AGFI V1. After the airdrop, 100 billion AGFI were sent to the timelock treasury and the remainder burned.

## Governance

AGFI uses Compound Finance's Governor and Timelock contracts with no modifications (version 4.6.0).

### Proposal Management

The AGFI governance is managed using Tally, a service designed for interaction with DAO contracts. Tally has no control over the DAO contracts or AGFI, it just

Should the Tally service become unavailable for some reason, the AGFI project can develop an alternative interface for interacting with the underlying DAO contracts.

## Custodianship

Ownership of some contracts and the treasury requires custodianship to be provided by a trusted third party.

Congruent Labs provide contract custodianship to the AGFI community for assurance and security.
