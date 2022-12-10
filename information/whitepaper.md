# Whitepaper

{% hint style="info" %}
This page is undegoing changes as the protocol changes. Some sections may have out of date information.
{% endhint %}

## Abstract

In just a few short years, cryptocurrency-based financial systems have undergone a rapid transformation, adapting to the emergence of blockchain technology. Early financial services built on blockchain technology have evolved from simple transactional systems into complex ecosystems that mirror the societies and organizations we create. Despite being largely unknown to the general public, decentralized finance (DeFi) has already given rise to a new generation of tokenomic and governance structures. DeFi offers holders access to unique investment opportunities and a multitude of other benefits.

This document explores how the Aggregated Finance (AGFI) project will use a Decentralized Autonomous Organization (DAO) structure to create a truly decentralized investment vehicle. It covers the definition of a DAO, its role in AGFI, its mechanisms for implementation, and custodianship of the DAO for long-term growth. By harnessing the power of the DAO, AGFI is able to create a self-governing and transparent investment platform that is controlled by its community.

#### Introduction

On November 29, 2021, Aggregated Finance (AGFI) launched its token with the goal of providing holders with access to community-powered investments. Initially, these investments were primarily focused on yield farming and projects investing in yield farming-related opportunities. These collective investment vehicles were pioneers of the "DeFi 3.0" or "Farming-as-a-Service" (FaaS) segment of decentralized finance. FaaS provides token holders with passive rewards from the project's treasury. As the project's assets grow in value, holders are rewarded. The AGFI DAO allows holders to vote on how to manage the treasury and its profits.

At launch, AGFI's strategy was to maintain a balanced treasury with 50% allocated to lower-risk yield farms and 50% allocated to higher-risk DaaS project investments. This strategy focused on preserving capital and controlled exposure to risk. However, the AGFI treasury will ultimately be managed by the community through the AGFI DAO, which will decide how the assets are selected and managed.

#### Tokenomics

To ensure a fair distribution of tokens, 40% of the total supply (400,000,000,000 tokens) was provided as liquidity on a decentralized exchange (DEX) to establish the token price and trading capabilities. No tokens were provided to any addresses prior to launch on the DEX, and no tokens can be minted by the contract after launch. The remaining 60% of the supply (600,000,000,000 tokens) was sent to the Ethereum null address, effectively "burning" the tokens and making them unusable. This was done to offset the inflation bug inherited from earlier reflection token contracts.

The token contract extends the ERC20 standard transfer function, and it inspects the sender address to determine if it is the Uniswap V2 router contract address. If it is, it will extract the defined fee rate from the transaction, sell it against the Uniswap V2 router contract, and split the resulting ETH evenly between a "treasury" wallet and a "marketing" wallet. If the sender is not the V2 router contract, it will extract the defined reflection rate from the transaction to make it available for all current token holders. The null address will receive any reflected tokens extracted during transfers, capturing excess tokens created by the inflation bug.

#### Decentralized Autonomous Organizations

A Decentralized Autonomous Organization (DAO) is a type of organization that operates without a central, controlling entity. While traditional organizations have decision-making power concentrated in the hands of a few individuals or groups, a DAO distributes power and responsibility among its token holders.

The AGFI DAO will require regular decision-making and execution to be successful. The Aggregated Finance project will leverage this decentralized mechanism to create a truly community-owned and operated organization. To participate in a DAO vote, users will need to interact with the DAO contract using the mechanisms provided on the AGFI website. In cases where a vote requires manual intervention, a DAO custodian will be responsible for carrying out the outcome of the proposal. This ensures that the AGFI DAO remains decentralized and transparent, while also providing a mechanism for executing important decisions.

**DAO Custodianship**

Before one can understand DAO Custodianship, they need to understand and clearly define “ownership” in the context of a smart contract. Smart contracts are commonly deployed with very rudimentary, role-based access control. The Owner role is identified for contract functions. An Owner is typically the entity that possesses a private key – the key that was used to sign the transaction that deployed the contract to a blockchain network.

Certain administrative endpoints on the contract can only be executed by the Owner. For some smart contracts, the Owner can exert absolute control over core functionality. For other contracts – the Owner may hold no control over the core functions whatsoever.

Typically, smart contracts are written with some capabilities reserved for the Owner, such as denying or allowing specific addresses to transfer fungible and non-fungible tokens, modifying tax rates on buys/sells/transfers, or permitting/forbidding transfers altogether.

There are three approaches utilized for control/ownership of smart contracts:

1. Renouncement – The “Owner” role is transferred to the null address, and thus nobody retains ownership of the contract. No further modifications can be made. This is a popular and simple mechanism to cryptographically prove that the contract can never be modified again, however it is irreversible and future modifications of the contract become impossible.
2. Multi-Signature (Multisig) – The “Owner” role is delegated to an “M-of-N” multiple-signature configuration. Any execution of “Owner”-only contract functions must be approved by all (or some minimum number of) delegated owners of the smart contract. This resolves any concern of centralized control, however signing parties must be genuinely separate individuals that can be trusted to not collude.
3. Custodianship – The “Owner” role is retained by the deployer, or to another address controlled by the deployer, or is designated to an address held by a ‘Trusted Individual’. If the ‘Trusted Individual’ is a fully vetted, impartial, 3rd party (Custodian) that can be trusted to not make unexpected modifications to the smart contract, multiple signatories do not need to bechosen. The 3rd party can still theoretically be a bad actor or incompetent, but this can be mitigated through selecting a custodian that is not financially invested in the project and retains liability should malpractice occur.

AGFI’s governance mechanisms will require the execution of actions that fall far outside the realm of straight forward parameter adjustments in the smart contract (such as modification of the token contract tax rates). Providing a Delegated Trader with access to a Treasury wallet or liquidating a Treasury asset are examples of the types of actions the AGFI DAO will often require. Because the AGFI project does not have the necessary disperse team to establish a true multi-sig treasury, the AGFI DAO’s custodianship will be entrusted to a 3rd party, for all DAO and token contracts after the establishment of the DAO.

#### Governance Mechanisms

The primary function of the AGFI DAO is to serve as a community-controlled body for investing into other cryptocurrency projects. Pursuant to this end, there are a host of secondary functions that the community will control – which include AGFI and DAO Contract Modification Proposals as well as Freetext Proposals discussed below.

**Contract Modification Proposals**

TODO: Update for the V3 tax models

**Contract Role Proposals**

TODO

**Treasury Proposals**

**Governance Management**

1. Each Proposal is required to be submitted for review via the DAO Management Platform.
2. The Proposal Criteria (information required to be submitted with a given Proposal type) will differ based on the Governance Mechanism the Proposal falls under

Proposals that fail to meet their respective required Proposal Criteria will be subsequently rejected. Proposals that are rejected due to missing criteria may be corrected and resubmitted for review. The maximum number of “operations” within any given Proposal shall be ten (10).

The Proposal Management Platform will provide the following “core” features:

1. A methodology for rejecting malicious, incomplete, or duplicate Proposals
2. A methodology for enforcing a minimum quality standard for all Proposals
3. A methodology for removing bad/malicious actors that attempt to attack the DAO

The Proposal Management Platform shall be operated by a team of individuals who will fill the role of Proposal Manager(s):

* Individuals who wish to become Proposal Managers must submit a ‘Modify DAO Proposal Manager Proposal to the DAO
* The first “series” of these Proposals will be reviewed/approved by the DAO Custodian
* Future ‘Modify DAO Proposal Managers’ Proposals will be assessed by the established/existing Proposal Managers
* A quorum of 75% of DAO Proposal Managers is required to accept a ‘Modify DAO Proposal Manager’
* Proposal Manager approval/rejection decisions are logged for historical records
* Upon receiving a Proposal approval, the Proposal will be moved to the DAO contract on the DAO Management Platform and put to a vote. All DAO participants are welcome to vote on all approved Proposals

**Proposal Criteria**

**Treasury Allocation Proposals**

Each Treasury Allocation Proposal requires the following Proposal Criteria to be provided: Each Treasury Allocation Proposal requires the following Proposal Criteria to be provided:

1. The name of the asset(s) being requested to transfer
2. The amount of the asset(s) being requested to transfer
3. The recipient(s) of the transfer (Each additional recipient shall receive the specific amount in the Proposal)
4. The purpose of the transfer, such as (but not limited to): The allocation of funds to a Delegated Trader/Farmer, The purchasing of specific assets, A token ‘Buyback’, The payment to a third party for services rendered
5. The justification of the transfer, especially if one or more of the recipient addresses are unknown by the Proposal Managers, Community, or Team Treasury Allocation Proposals

Each Treasury Allocation Proposal will undergo rigorous scrutiny by the Proposal Managers, to ensure that all provided information meets the Proposal Criteria outlined above. This analysis/vetting process is a prerequisite before the Proposal can be sent to the DAO contract and moved to a vote on the DAO Management Platform. This process is put in place to protect the DAO from malicious attacks, whereby bad actors might otherwise bring forward malevolent Proposals with no impedance and thus, place the Treasury at risk of theft or being put in a compromising position.

Treasury Allocation Proposals that seek to transfer funds to/from a Delegated Trader/Farmer are anticipated to be required less frequently (monthly) and will be triggered by changes in Performance metrics. The AGFI DAO shall only measure the performance of Delegated Traders month- to-month.

**Contract Modification Proposals**

TODO

#### Voting Parameters & Constraints

TODO

#### Time Lock Constraints

TODO

#### Conclusion

This paper explored the AGFI DAO – its mechanisms for operation, its limitations, and its rules of engagement within the AGFI Community. The paper covered the DAO Custodian/Guardian, and how it will be utilized to launch the AGFI DAO and establish a decentralized investment vehicle, owned and operated by the AGFI Holders & Community. AGFI’s fundamentals position it to become the powerhouse in the nascent DeFi 3.0 space. The formidable combination of a Fair-Launched Token and DAO-controlled Treasury coupled with the ability to support delegated trading capabilities to trusted 3rd positions AGFI as a unique, decentralized DeFi 3.0 protocol. In short, it will reflect a core crypto fund investment functionality – all without a single, centrally located entity being involved.
