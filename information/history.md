---
cover: >-
  https://images.unsplash.com/photo-1505664194779-8beaceb93744?crop=entropy&cs=tinysrgb&fm=jpg&ixid=MnwxOTcwMjR8MHwxfHNlYXJjaHw4fHxoaXN0b3J5fGVufDB8fHx8MTY1Njk0MjQ1Ng&ixlib=rb-1.2.1&q=80
coverY: 0
---

# History

## Version 1

Aggregated Finance (AGFI) was launched on November 29, 2021. The token contract was based on a project called "Vari-Stable Capital" (which dissolved shortly thereafter), which itself was derived from the first version of Multi-Chain Capital (MCC). The original MCC project was a pioneer of "Farming-as-a-Service" or "DeFi 3.0" projects, which aimed to tax trades of the token on Uniswap and then use the taxes to farm yield. A plethora of similar projects launched around the same time, and Aggregated Finance was intended to be an abstraction layer that invested in these projects.

Most of the first-generation Farming-as-a-Service (FaaS) projects inherited a supply inflation bug from the original Multi-Chain Capital (MCC) project. The token contracts were not minting new supply, but they were mathematically "reflecting" a greater balance to all holders. This bug occurred because the contracts were not subtracting one of the collected fees during transfers, resulting in all token holder balances increasing at a rate corresponding to the transfer volume. AGFI was launched when this bug was known, but it attempted to counter the bug by burning 60% of the supply after launch. This reduced the supply inflation to a manageable level, but it also introduced other issues. Some of these issues were inherited from the forked token contracts:

* The 0xdead address had an ever-increasing balance of AGFI, which was confusing to holders because it exceeded the total launch supply.
* The fluctuating balances caused caching issues on tracking websites.
* The yield rates were unpredictable because they were impacted by both transaction volume and size.
* The token contract collected taxes for wallet-to-wallet transactions, causing people moving their tokens to cold storage to lose 10% of their balance.
* The tax rate configuration was limited, limiting the ability to fine-tune the taxes for the community.

## Version 2 & 3

Recognising the faults of the first version of AGFI, a transition plan to a replacement contract was enacted.

The replacement contract expanded the treasury taxation system to a channel-based tax system with 5 configurable tax channels, allowing for more granular control over the diversion of swap taxes for certain purposes. In addition to this, the project recognised that AGFI should transition to a DAO to move to a community-led protocol.

The new 5 channel-based system and DAO iintegration was introduced as AGFI Version 2, however shortly after launch it became apparent one of the tax channels swap executions was driving up transaction gas fees and causing swap failures.

As the contract was already deployed to mainnet and not an upgradeable contract, the only necessary solution was to deploy a 3rd contract version. To reduce gas required for executing each tax channel swap, the 3rd contract version was modified to round-robin each tax channel execution instead. As a result, the newer contract allowed the contract to run in a far more gas efficient way and still retain all its configurability for 5 tax channels.&#x20;
