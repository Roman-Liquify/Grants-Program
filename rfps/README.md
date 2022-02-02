<p align="center">
  <img src="../src/rfp-header.png" style="width:1300px";>
</p>

- [:grey_question: What is an RFP?](#grey_question-what-is-an-rfp)
- [:scroll: List of current RFPs](#scroll-list-of-current-rfps)
  - [Availability and Validity - Network Topology](#availability-and-validity---network-topology)
  - [e-Passport ZK Validation](#e-passport-zk-validation)
  - [RFP: Substrate Identity Directory](#rfp-substrate-identity-directory)
  - [ink!/pallet/solidity performance benchmarking](#inkpalletsolidity-performance-benchmarking)
  - [DOT & KSM mixer](#dot--ksm-mixer)
  - [Multi-chain Block Explorer](#multi-chain-block-explorer)
  - [On-chain Quadratic Funding](#on-chain-quadratic-funding)
  - [PHP Substrate API](#php-substrate-api)
  - [Polkadot Collator Setup](#polkadot-collator-setup)
  - [Privacy Enhancement for Polkadot Extension](#privacy-enhancement-for-polkadot-extension)
  - [High-availability validator setup](#high-availability-validator-setup)
  - [Summary](#summary)
  - [SCALE Codec Comparator](#scale-codec-comparator)
  - [Social Recovery Wallet](#social-recovery-wallet)
  - [Uncollateralized Stablecoin](#uncollateralized-stablecoin)
  - [polkadot-validator-setup maintenance](#polkadot-validator-setup-maintenance)
  - [XCM library & tools](#xcm-library--tools)
- [:mailbox_with_mail: Suggest an RFP](#mailbox_with_mail-suggest-an-rfp)


## :grey_question: What is an RFP?

An RFP (Request for Proposals) is a declaration of interest for others to submit a grant application regarding a specific project. They usually revolve around issues that the author (often someone from our team, but [anyone can suggest one](/README.md#mailbox_with_mail-suggest-a-project)) deems useful and missing or unsolved in our ecosystem.

If you find an open RFP here that you think you can address, feel free to [submit a grant application](../README.md#1-application). There is a [section in our application template](../applications/application-template.md#project-overview-page_facing_up) where you can reference the RFP you are addressing.


## :scroll: List of current RFPs

### Availability and Validity - Network Topology


- Published: 2021-11-19


- [:arrow_right: a-and-v-topology.md](./a-and-v-topology.md)


- **Proposer:** @infinity0, @skalman, @mmagician


#### Project Description :page_facing_up:

A part of the promise of Polkadot is to bring scalability to the blockchains. The way it achieves it is via delegating application-specific logic from layer 0 (the relay chain) to layer 1 chains (parachains). In order to achieve this efficiently yet securely, each parachain has its own block production mechanism (achieving efficient block production), but the finalisation of candidate parachain blocks still happens with the involvement of the relay chain validators.

The full mechanism is described in [the host specification](https://github.com/w3f/polkadot-spec/blob/main/host-spec/c07-anv.tm). In short, it is split in two parts: first, a publicly known subset of validators attests that the parachain block data is available to them (i.e. they must have it in their local storage); second, once 2/3+ of the first group have published their availability votes, a "secret" (VRF-based assignment) subset of validators checks the validitiy of the candidate, by checking its state transition against that parachain runtime, which is available on-(the relay)chain. ...


#### Deliverables :nut_and_bolt:

- **Total Estimated Duration:** 14 weeks
- **Total Costs:** 90,000 DAI



----



### e-Passport ZK Validation


- Published: 2021-11-23


- [:arrow_right: epassport-zk-validation.md](./epassport-zk-validation.md)


- **Proposer:** [burges](https://github.com/burges), [FlorianFranzen](https://github.com/FlorianFranzen)


#### Project Description :page_facing_up:

The issue of verifying identities on-chain and providing Proof-of-personhood is a challenging one.

One idea to authenticate users is to ask them to submit the details from their e-passports. While it would provide authentication, it forgoes the aspect of privacy. ...



----


### RFP: Substrate Identity Directory


- Published: 2021-07-20


- [:arrow_right: identity-directory.md](./identity-directory.md)


- **Proposer:** swader


#### Project Description :page_facing_up:

In Substrate-based chains which implement the [Identity pallet](https://github.com/paritytech/substrate/tree/master/frame/identity), users can register on-chain information about themselves. It is currently difficult to search by any of the identity fields. There is also no way to link directly to an on-chain account and see human-readable reports of its interactions with the chain, let alone quickly send tokens to it or otherwise interact directly with that account.

The Identity Directory is a **fully client-side web application** which makes this possible. ...



----


### ink!/pallet/solidity performance benchmarking


- Published: 2021-07-20


- [:arrow_right: implementation-benchmarking.md](./implementation-benchmarking.md)


- **Proposer:** [mmagician](https://github.com/mmagician)


#### Project Description :page_facing_up:

When a new team comes to the ecosystem, they are faced with a decision on how to best implement the logic that they need.
Traditionally in substrate, this has been a choice between a smart contract vs. runtime module (a.k.a. pallet) and elaborated on [in this StackOverflow question](https://stackoverflow.com/questions/56040779/when-should-i-build-a-substrate-runtime-module-versus-a-substrate-smart-contract) or [this entry in Substrate Developer Hub](https://substrate.dev/docs/en/knowledgebase/smart-contracts/#smart-contracts-vs-runtime-development). The choice has since been augmented by the possibility to deploy solidity contracts to an EVM-compatible chain, or even writing solidity code and compiling it to WASM with the help of a [solang](https://solang.readthedocs.io/en/latest) compiler.
 ...


#### Deliverables :nut_and_bolt:

- **Total Estimated Duration:** 4 weeks
- **Full-time equivalent (FTE):** 1
- **Total Costs:** 10,000 DAI


----


### DOT & KSM mixer


- Published: 2021-11-23


- [:arrow_right: mixer.md](./mixer.md)


Polkadot uses an account-based Tx model, which easily enables linking activity between accounts.
To preserve on-chain anonymity, the options available to the user at the moment are limited to using centralised exchanges.
It requires transferring their funds to an exchange-controlled account and withdrawing them at a later point in time, to a different account. ...






----


### Multi-chain Block Explorer


- Published: 2021-11-23


- [:arrow_right: multi-chain-block-explorer.md](./multi-chain-block-explorer.md)




#### Project Description :page_facing_up:

As parachains become an integral part of the Polkadot and Kusama ecosystems, a cross-chain block & accounts explorer becomes all the more useful.

Some of the functionality that should be covered as part of the development: ...




----


### On-chain Quadratic Funding


- Published: 2021-07-20


- [:arrow_right: on-chain-quadratic-funding.md](./on-chain-quadratic-funding.md)


- **Proposer:** [Noc2](https://github.com/Noc2)


#### Project Description :page_facing_up:

CLR, short for [Constrained Liberal Radicalism algorithm](https://blogchains.org/wp-content/uploads/sites/4/2019/04/SSRN-id3243656.pdf), commonly called quadratic funding (QF), is a way to efficiently fund projects in the Web3 ecosystem. The way it works is that users contribute directly to projects which they value and in doing so, help the projects earn a share of a matching pool of funds. The *number* and amount of each contribution influences the total amount allocated to a project. This means even a small contribution is valuable and can result in a high matched amount.

[Gitcoin](https://gitcoin.co/) is currently using this mechanism to successfully fund and support public goods. However, Gitcoin is centralized. The goal of this RFP is to develop a decentralized solution on top of [Substrate](https://github.com/paritytech/substrate), which can potentially be integrated into Kusama, Polkadot or any other Substrate-based chain as a pallet. The on-chain treasury could potentially sustainably fund the matching pool in the long-run. However, the Web3 Foundation would also be committed to fund a matching pool of the solution for initial test rounds.  ...


----


### PHP Substrate API


- Published: 2021-07-20


- [:arrow_right: php-api.md](./php-api.md)


- **Proposer:** [swader](https://github.com/api)


#### Project Description :page_facing_up:

The Substrate API is currently most developed in TypeScript and Rust. This RFP is looking for teams willing to implement a PHP version, perhaps in tandem with the PHP SCALE Coded (see relevant RFP).

The PHP API should: ...


#### Deliverables :nut_and_bolt:

The basic deliverable of this project is an API package hosted on Packagist which can instantiate a connection to a Substrate node and talk to constants, chain storage, and RPC endpoints. For inspiration, see the JS version: https://polkadot.js.org/docs


----


### Polkadot Collator Setup


- Published: 2021-11-23


- [:arrow_right: polkadot-collator-setup.md](./polkadot-collator-setup.md)


- **Proposer:** [mmagician](https://github.com/mmagician)


#### Project Description :page_facing_up:

This is meant as a companion repository to [polkadot-validator-setup](https://github.com/w3f/polkadot-validator-setup), which allows anyone to launch a validator node in an automated and secure fashion.

I would like to standardize (as much as possible) the process of spinning up new collator nodes for different parachains. ...


#### Deliverables :nut_and_bolt:

Ideally the PoC would
Please list the deliverables of the project in as much detail as possible. Please also estimate the amount of work required and try to divide the project into meaningful milestones.



----


### Privacy Enhancement for Polkadot Extension


- Published: 2021-11-26


- [:arrow_right: privacy-enhancement-polkadot-extension.md](./privacy-enhancement-polkadot-extension.md)


- **Proposer:** jonasW3F


#### Project Description :page_facing_up:

An increasing number of websites require access to the Polkadot extension with a growing ecosystem. By allowing access to the extension, websites (naturally) can see the addresses that are contained in the extension. This imposes a big risk to privacy, because malicious actors could create lists about which addresses belong to one entity and, in the worst case, even link it to real-world identities (if at least one address is linked to an on-chain identity). A feature to prevent this is currently the "hide" button on single addresses, which prevent websites from seeing that address. However, it is currently cumbersome to handle that feature. The idea of this RFP is to extend on that feature and include a few QOL functionalities to make it easier for users to protect their privacy.


#### Deliverables :nut_and_bolt:

As outlined [here](https://github.com/polkadot-js/extension/issues/893), the deliverable should include five features to the extension and a successful completion of this RFP includes a merge of a PR to the main polkadot-js/extension repo. **It is of great importance to generate clean code that follows best-practices**.

- **Total Estimated Duration:** 1 month


----


### High-availability validator setup


- Published: 2021-07-20


- [:arrow_right: raft-validators.md](./raft-validators.md)


- **Proposer:** [mmagician](https://github.com/mmagician)


#### Project Description :page_facing_up:

### Summary

Validator leader selection via Raft consensus. Inspired by internal discussions & [certus.one active-active validator setup](https://kb.certus.one/validator_ha.html#active-active-validator). ...


#### Deliverables :nut_and_bolt:

- **Total Estimated Duration:** 3 months
- **Full-time equivalent (FTE):** 1
- **Total Costs:** 30,000 DAI


----


### SCALE Codec Comparator


- Published: 2021-07-20


- [:arrow_right: scale-codec-comparator.md](./scale-codec-comparator.md)


- **Proposer:** [Marcin Górny](https://github.com/mmagician/)


#### Project Description :page_facing_up:

To date, there are [9 published](https://substrate.dev/docs/en/knowledgebase/advanced/codec#implementations) implementations of the SCALE Codec. Since each is implemented by a different team & [the reference implementation](https://github.com/paritytech/parity-scale-codec) still introduces small fixes, it would be beneficial to compile a table of feature-completeness.
This would provide (some) assurance that the implementation in a given language is safe & sound to use.
 ...


#### Deliverables :nut_and_bolt:

- **Total Estimated Duration:** 2+ months
- **Full-time equivalent (FTE):**  1
- **Total Costs:** ~ 12,000 DAI


----


### Social Recovery Wallet


- Published: 2021-08-02


- [:arrow_right: social-recovery-wallet.md](./social-recovery-wallet.md)


- **Proposer:** [Noc2](https://github.com/Noc2)


#### Project Description :page_facing_up:

Managing your own private keys is a difficult task. The average person doesn’t want to spend multiple hours to ensure the security of their keys. This leads to people having difficulties to join the blockchain space or even worse leads to the loss of funds. One solution to this problem is the implementation of a social recovery system. It allows users to recover their accounts if their key or other authentication mechanism has been lost. Therefore you usually set up at least 3 "guardians" (e.g. other devices, friends or family or institutions), of which a majority can cooperate to change the key of the account (often after some delay). Kusama has for this purpose currently the [social recovery pallet implemented](https://github.com/paritytech/substrate/blob/master/frame/recovery).

The goal of this RFP is to find teams that are willing to leverage this or similar mechanism to create wallet solutions (desktop, web, mobile, extensions, etc.) which are as easy to use as possible and at the same time offer a high security for the average user.  ...


#### Deliverables :nut_and_bolt:

The deliverables highly depend on the exact wallet implementation and therefore aren’t further described as part of this RFP. For the grant application you should take a look at the [application template](https://github.com/w3f/Grants-Program/blob/master/applications/application-template.md#overview-1) and try to specify the deliverables as detailed as possible.


----


### Uncollateralized Stablecoin


- Published: 2021-07-30


- [:arrow_right: uncollateralized-stablecoin.md](./uncollateralized-stablecoin.md)


- **Proposer:** [Noc2](https://github.com/Noc2)


#### Project Description :page_facing_up:

Stablecoins are cryptocurrencies where the price is designed to be pegged (=fixed exchange rate) to a cryptocurrency, fiat money, or to exchange-traded commodities. Seigniorage-style, uncollateralized or algo stablecoin is a token that uses algorithms to control the circulating supply to get a stable value of the asset. In general the price volatility of cryptocurrencies is one of the biggest barriers to widespread adoption. Stablecoins therefore have become a key component of DeFi applications. However, all successful existing stable coins (e.g. DAI, USDT, USDC, etc) are asset backed. Therefore they are subject to the same volatility and risk associated with the backing asset and the underlying process. Some of the potentially issues based on this are:

- Additional trust assumptions (e.g. USDT)  
- Scalability issues (restricted by the underlying asset)  ...


#### Deliverables :nut_and_bolt:

The milestones below are just an initial draft. The milestones can be structured completely differently and the implementation can also leverage other tools and infrastructure as long as the overall goal of the RFP is met.

- **Total Estimated Duration:** 2 month


----


### polkadot-validator-setup maintenance


- Published: 2021-11-23


- [:arrow_right: validator-setup-maintenance.md](./validator-setup-maintenance.md)




#### Project Description :page_facing_up:

One of the more accessible ways of spinning up validator nodes is by using the [`polkadot-validator-setup`](https://github.com/w3f/polkadot-validator-setup) repository, which uses a mix of terraform and ansible tools to create a server, adjust its configuration and install the necessary packages needed for running a substrate node.

This RFP aims at providing maintenance to that repository and add some small features. ...


#### Deliverables :nut_and_bolt:

A list of possible tasks to work on:

- fixing issues and improving documentation
- updating any libraries/deps needed


----


### XCM library & tools


- Published: 2021-07-20


- [:arrow_right: xcm-tool.md](./xcm-tool.md)


- **Proposer:** [Bryan Chen](https://github.com/xlc)


#### Project Description :page_facing_up:

XCM is the crosschain communication standard that will be used by all the parachains. Currently XCM is still in early stage but already supports some main use cases such as crosschain transfer of fungible tokens.

There are currently two major areas of XCM that still awaiting to be improves: ...

----

## :mailbox_with_mail: Suggest an RFP

If you think that we should support the development of certain tools or projects (related to **Polkadot, Kusama or Substrate**) that aren't in the Polkadot/Kusama [tech stack](docs/polkadot_stack.md), please submit a suggestion using the process described in our [Grants program README](../README.md#mailbox_with_mail-suggest-a-project). We are particularly interested in supporting projects that could be leveraged by other builders in our ecosystem.