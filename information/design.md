# Design

## Introduction



## Contract



## Tokenomics

AGFI V3 is a 1-for-1 relaunch of the original AGFI, launching with a token supply of 1 Trillion (1,000,000,000,000) tokens. 1-for-1 tokens were airdropped to all V1 and V2 token holders to replace AGFI V1. After the airdrop, 100 billion AGFI were sent to the timelock treasury and the remainder burned.



## Governance



### Proposal Management



### Timelock



## Custodianship







####

#### Abstract

Cryptocurrency-based financial systems have evolved in a shockingly short span of time when compared to traditional financial systems. Structures that have existed to serve the public for hundreds of years have had to undergo rapid metamorphosis as they’re adapted to blockchain technology. Early financial services built on blockchain technology have developed from simple transactional systems into nuanced ecosystems replicating the society and the organizations we build within it. Decentralized Finance has yet to be so much as noticed by even a minority of the world’s population, and already it has birthed an entire generation of new paradigms - for tokenomic and governance structures alike. DeFi offers the Holder access to unique investment mechanisms and a multitude of other opportunities.

This document explores the Aggregated Finance (AGFI) project, Decentralized Autonomous Organizations (DAO), and how AGFI will utilize a DAO structure to establish a truly decentralized investment vehicle. The document will discuss the definition of a DAO, its role for AGFI, its mechanisms for application, and custodianship of the DAO for long term growth.

#### Introduction

On the 29th of November 2021, the Aggregated Finance (AGFI) token was launched with the goal of providing Holders with access to the world of community-powered investments. These investments were (at the time) primarily focused almost exclusively on Yield Farming and/or Projects investing in Yield Farming-related opportunities. These collective investment vehicles served as “Pioneers” for the segment of Decentralized Finance that has since adopted the moniker of “DeFi 3.0”, or “DeFi-as-a Service” (DaaS). At its core, DaaS provide token holders with passive rewards from the Project’s ‘Treasury’. As the Project’s assets grow in value, Holders are rewarded in different ways. Through the DAO – Holders decide (or vote on) how best to handle the Treasury – its principal as well as its profits.

Originally, and as alluded to above, AGFI’s mission was to maintain a Treasury of assets with an even allocation of Risk:

* 50% Yield Farms (LowerRisk)
* 50% DaaS Project Investments (HigherRisk)

The strategy focused on ‘Treasury Capital Preservation’ with controlled exposure to ‘Risk-On Opportunity’. While this was the initial strategy at the AGFI token launch, the AGFI Treasury will ultimately be managed by the community via the AGFI DAO. The DAO will therefore decide how the Treasury assets are selected and managed.

#### Tokenomics

To ensure fair distribution of all tokens to holders, 40% (or 400,000,000,000 tokens) were provided as Decentralized Exchange¹ liquidity against 5 ETH tokens to instantiate the token price and trading capability for the market. No tokens were provided to any addresses prior to launch on the Decentralized Exchange. No tokens can be minted by the contract after launch.

The remaining 60% of launch supply (600,000,000,000 tokens) were sent to the Ethereum null address² to “burn” the supply – that is, to render the tokens unusable. This was intentional to offset an inflation bug present in the AGFI token contract derived from earlier versions of reflection token contracts. Reflected tokens are not minted (in the context of ERC20 token minting functions), however if the calculation for appending tokens to the reflection pool is not correct an excess of tokens will become available for holders to transact with. An inflation bug has been inherited from the contract that AGFI was forked from, but with over 60% of the supply sent to the burn wallet the inflation rate is drastically reduced and will deflate progressively from token buybacks and burns whilst reflections remain active.

The token contract extends the ERC20 standard transfer function, and additionally inspects the sender address to determine if it is the Uniswap V2 router contract address¹. If it is the contract address, it will extract the defined fee rate² from the transaction. This fee rate will be subtracted from the transaction and sold against the Uniswap V2 router contract, and the ETH received from that sale will be split evenly between a “treasury” wallet and a “marketing” wallet. If the V2 router contract address is not the sender, it will extract the defined reflection rate³ from the transaction to become available for all current token holders.

The null address will receive reflected tokens extracted during transfers. This is to capture all excess tokens created by the inflation bug discussed earlier.

#### Decentralized Autonomous Organizations

A Decentralized Autonomous Organization or ‘DAO’, is a body, firm, or organization that operates without a single, centralized controlling entity. While most organizations place decision making power in the hands of individuals (such as the president of a company) or select groups of individuals (such as a board of directors), a DAO parses and distributes power and responsibility amongst its token holders.

Like any organization, the AGFI DAO will routinely require decisions to be made (and then executed) if it is to become successful. The Aggregated Finance project will leverage this decentralized mechanism to establish a truly community-owned and operated organization.

Participation in a DAO vote will require interaction with a DAO contract using mechanisms provided on the AGFI website. In the case of DAO vote outcomes requiring manual intervention, a DAO custodian will be required to complete the outcomes completed after proposals have been completed.

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
