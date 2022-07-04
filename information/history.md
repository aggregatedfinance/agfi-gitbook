---
cover: >-
  https://images.unsplash.com/photo-1505664194779-8beaceb93744?crop=entropy&cs=tinysrgb&fm=jpg&ixid=MnwxOTcwMjR8MHwxfHNlYXJjaHw4fHxoaXN0b3J5fGVufDB8fHx8MTY1Njk0MjQ1Ng&ixlib=rb-1.2.1&q=80
coverY: 0
---

# History

## Version 1

Aggregated Finance (AGFI) was launched on November 29, 2021. The token contract was a fork of a project called “Vari-Stable Capital” (which dissolved not long afterwards), which itself was a derivative of the first version of Multi-Chain Capital (MCC). The original MCC project started a new wave of “Farming-as-a-Service” or “DeFi 3.0”, projects designed to tax trades of the token on Uniswap to then farm those taxes on yield farms. A myriad of projects launched at the same time attempting to target specific market segments, or just copying others, and Aggregated Finance was intending on investing in those projects as an abstraction layer above all of them.

Almost all of these first generation FaaS projects inherited a supply inflation bug from MCC. The token contracts were not minting new supply, but they mathematically “reflect” a greater balance to all holders. The bug was not subtracting a collected fee during transfers, and as a result all token holder balances were increasing at a rate corresponding to the transfer volume. AGFI was launched when this bug was known, but attempted to counter the bug through a 60% supply burn event after launch so that 60% of reflections would be correspondingly burned on every trade. Whilst this brought the supply inflation into a manageable state, it introduced other issues (and some other issues were inherited from the forked token contracts):

* The 0xdead address was showing an ever increasing balance of AGFI, confusing holders as it exceeded the total launch supply.
* Balances were not static and caused caching issues on tracking websites.
* Yield rates were not predictable as the rate of reflected tokens was impacted by both transaction volume and transaction size.
* The token contract would collect taxes for wallet-to-wallet transactions, causing people moving to cold storage to lose 10% of their wallet balance.
* Tax rate configuration was extremely limited, reducing the ability to fine tune the taxes for the community.

## Version 2 & 3

