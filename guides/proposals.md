---
cover: >-
  https://images.unsplash.com/photo-1529107386315-e1a2ed48a620?crop=entropy&cs=tinysrgb&fm=jpg&ixid=MnwxOTcwMjR8MHwxfHNlYXJjaHw1fHxnb3Zlcm5tZW50fGVufDB8fHx8MTY1NzE1ODk1Mg&ixlib=rb-1.2.1&q=80
coverY: 0
---

# Proposals

## Creating Proposals on GitHub

Creating proposals for the Aggregated Finance DAO is a very simple process. It all starts with GitHub, where all the proposal discussion needs to happen:

{% embed url="https://github.com/aggregatedfinance/agfi-dao" %}

If you want to be involved in the discussions on GitHub then you will need to create a GitHub account. It's a very easy process, just follow the prompts:

{% embed url="https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account#1-creating-an-account" %}

The AGFI DAO is a "repository" on GitHub. Normally repositories are used to store code, but in our case we'll just use it for discussion and information about the Proposals for the DAO.

{% hint style="info" %}
Did you know Ethereum uses GitHub for all of its proposals too? You can check out the Ethereum proposals here: [https://github.com/ethereum/EIPs](https://github.com/ethereum/EIPs)
{% endhint %}

Every Proposal is handled as an **Issue** in the DAO repository.

![](https://blog.aggregated.finance/content/images/2022/05/image-13.png)

You will see all the open proposals here when you view the Issues section. If you want to start a discussion about a new proposal, click **New Issue** on the top-right of the page:

![](https://blog.aggregated.finance/content/images/2022/05/image-14.png)

There are some templates you can use to make a new proposal. After the DAO gets set up most of these will be "Treasury Allocation" proposals. If none of these proposals meet your needs you can also choose **Open a blank issue** at the bottom.

![](https://blog.aggregated.finance/content/images/2022/05/image-15.png)

Now all you need to do is fill out the details. Give it a title that makes sense, and fill in the details about what the proposal will do and why it should be voted on. Once you've filled in all the information, click **Submit new issue**:

![](https://blog.aggregated.finance/content/images/2022/05/image-16.png)

The proposal will be open for anyone to review, comment, and discuss if it should move to a formal vote.

{% hint style="info" %}
The Proposal Managers may edit or reject your proposal if it doesn't satisfy all the information needed to move it to a formal vote. Every vote needs a justification as to why it should happen, otherwise why do it at all?
{% endhint %}

If you want to voice your opinion, you can write your own response to any proposal at the bottom by adding a comment:

![](https://blog.aggregated.finance/content/images/2022/05/image-18.png)

## Opening Proposals on Tally

On the Tally DAO interface, click **Create new proposal**.

![](<../.gitbook/assets/image (9).png>)

Connect your wallet and click **Continue**.

![](<../.gitbook/assets/image (3) (1).png>)

Fill out the description from the proposal information defined on the GitHub proposal and click **Continue**.

![](<../.gitbook/assets/image (8) (1).png>)

Depending on what actions the proposal is meant to take, you must define at least one for the proposal.

For example, transferring tokens will show the tokens held in the timelock treasury that can be transferred, and you can define who will receive the tokens and how many:

![](<../.gitbook/assets/image (7).png>)

Alternatively, you can define a custom action that the proposal will perform. This is any action that calls a smart contract function, so you can use these to modify things like the AGFI Governor contract, Timelock contract, and more.

To define a custom action, paste in a contract address to the **Target contract address**. If it's a contract that has been verified on Etherscan then the contract methods will automatically load. If it's not a verified contract you will need the contract ABI data to show the contract methods.

Once you've set the address, select the **Contract method** you want the vote to call. Then any parameters that are required for that contract method will appear, and you will need to define the values that they're changing to. In the example below the action is to call setVotingPeriod with the newVotingPeriod set to 1000.

![](<../.gitbook/assets/image (5) (1).png>)

{% hint style="warning" %}
The DAO interface won't warn you if your proposal actions are technically possible or not. Some function calls require the DAO contract to hold certain rights, like ownership over another contract. If you aren't sure what you're doing, consult the DAO Proposal Managers for advice.
{% endhint %}

If you want a proposal to not actually perform any action at all because it's a "meta" change to the project, then simple define the action as a transfer of 0 ETH to any address.

Once you've defined the actions for the proposal (you can define up to 10, so if you need to execute a sequence of contract calls that's entirely possible), click **Continue**.

You will get a preview of your proposal. Click **Submit on-chain** if you want to get it opened immediately, or click **Save Draft** if you want to save it for later.

![](<../.gitbook/assets/image (1).png>)

Once a proposal is submitted on-chain a voting delay period starts. This period is by default set to 1 day, which gives people enough time to delegate their votes if required. While this delay period is in effect the proposal will show as "Pending" on Tally.

![](<../.gitbook/assets/image (4).png>)

## Queueing Proposals on Tally

{% hint style="info" %}
Proposals can only be queued once the voting period has finished, and the vote received more FOR votes than AGAINST/ABSTAIN votes.
{% endhint %}

To queue a proposal, open **Manage Proposals** on the Tally DAO interface and click **Queue**. You will be prompted by your wallet software to confirm the transaction, which will incur a network gas cost.

![](<../.gitbook/assets/image (2).png>)

A queued proposal must wait for the timelock period to expire before it can be executed. If you hold the right to cancel proposals, you can also cancel the proposal at this point if required.

## Executing Proposals on Tally

{% hint style="info" %}
Proposals can only be executed if they've been queued in the timelock and not still waiting for the timelock period to end, which by default is 1 day from when the proposal was queued.
{% endhint %}

To execute a proposal, open **Manage Proposals** on the Tally DAO interface and click **Execute**. You will be prompted by your wallet software to confirm the transaction, which will incur a network gas cost.

![](<../.gitbook/assets/image (4) (1) (1).png>)

Once the proposal has been executed the proposal process is complete.
