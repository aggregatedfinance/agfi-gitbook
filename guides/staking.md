---
coverY: 0
---

# Staking

Staking is an optional feature in the AGFI ecosystem. It operates separately to the ETH rewards option.

Staking rewards currently distributes AGFI sent from the AGFI token contract. The contract is a fork from the Trader Joe sJOE staking contract which supports distributing multiple tokens at once, so if there are additional tokens added into the AGFI ecosystem later they can be distributed as rewards through the same staking contract.

## Deposit

To stake your AGFI, use the dashboard and scroll down to the Staking section. If you have any unstaked AGFI it will show up as _Your Unstaked Balance_. If you click **ALL**, your balance will be copied into _Amount to Stake_.

You can choose to modify the amount you want to stake, but if you set an amount higher than your balance it will reset to your balance. If you set a negative number, it will reset to 0.

![](<../.gitbook/assets/image (3).png>)

Once you've chosen how many tokens to stake, click **APPROVE**. This will require a transaction on the network. Once that transaction is completed, you can then click **STAKE**.

{% hint style="info" %}
Approval is needed to allow the Staking contract to deposit your tokens from your wallet. Approvals are always set to a specific amount, and so if you've used up your approved amount you may need to approve again.
{% endhint %}

## Withdrawal

You can unstake your tokens at any time just in the same manner as staking them. You must define how many tokens you want to withdraw, and then click **UNSTAKE**.

![](<../.gitbook/assets/image (8).png>)

As you earn tokens whilst staked, you will receive _Pending Rewards_. If you withdraw any staked tokens your pending rewards will be withdrawn as well. If you click **HARVEST REWARDS** you will just withdraw only your pending rewards.

Just like the ETH rewards feature, it's always best to check that the gas fees for the network won't exceed the value of the rewards you're claiming.
