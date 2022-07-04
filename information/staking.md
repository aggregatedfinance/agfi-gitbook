# Staking

### Where to Stake

To stake, use the AGFI [Dashboard](https://aggregated.finance/#/dashboard).

{% embed url="https://aggregated.finance/#/dashboard" %}

### How it works

Tax channel 4 on the AGFI token contract collects a percentage of every Uniswap AGFI buy and sell. Once the tax channel is executed (every 5th Uniswap sell), it will send the collected AGFI taxes directly to the staking contract.

The staking contract will then instantly distribute those reward tokens according to the amount of tokens you have staked versus how many you’re staking in relation to everyone else. The more people that stake, the more dilution of the reward across all stakers. The fewer people that stake, the more concentrated the rewards become to all stakers.

Annual Percentage Rate (APR) is not fixed for the pool. It changes based on how many AGFI tokens are being traded on Uniswap, and how many transactions are occurring on Uniswap. The higher the volume, the more distributions to stakers. The lower the volume, the fewer distributions to stakers.

### Constraints

There are 2 constraints that are caused by staking:

1. Stakers cannot vote on proposals when their tokens are staked. When a proposal is scheduled to run they will just need to unstake, vote, and then stake again. No staking rewards would be missed in this process (unless tokens are distributed to the staking contract while they perform their vote), but they will have to pay the network fees to move in and out of the staking pool.
2. Stakers cannot collect their ETH rewards whilst staked. Their rewards are assigned to the staking contract (which cannot claim them), and then when they unstake their rewards are returned to them. Once a person unstakes, they can claim whatever ETH rewards they have pending.

### Notes

The current staking contract is a fork of the sJOE staking contract from Trader Joe with some reentrancy guards added. sJOE stakes JOE and distributes USDC to stakers. This contract stakes AGFI and distributes AGFI. This contract can support more reward tokens being added so stakers can receive multiple reward tokens at once.\
