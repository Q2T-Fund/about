# Quadratic Treasury (Q2T)
Q2T combines _DIDs_, _Mutual Credit_ & _Quadratic Funding_ to allow (1) a sybil-resistant, fair mean for donors to support Public Goods - and (2) a way for projects to attract _funds_ and _non-repayable loans_ in a **permissionless** fashion, based exclusively on **the milestones achieved**.

# Repos:
- [**Smart Contracts**](https://github.com/Q2T-Fund/Q2T-Fund-contracts)
- [**Frontend**](https://github.com/Q2T-Fund/Q2T-Fund-frontend)

# Problem(s).
- Projects in the area of Public Goods struggle to attract _timely_ funds, needed in order to bring innovation openly, limiting the rate of abandonment (unsustainability) and delays (lack of resources). They either have to wait for lengthy local/governmental procedures (for grants), or rely on public donations, that may be unpredictable, and too tightly bounded to (often unviable practices such as) Marketing & Advertisement.

- Gitcoin was one of the 1st successful experiments of Quadratic Funding, and their platform was able to attract a wopping 1M+ USD in donations, distributing them to public grants. Nonetheless, with the growth of the platform and the increase in the amount of projects, issues such as **sybil-attacks** (to achieve _matching pool manipulation_) and **"popularity games"** (where the _grant position_ and the _popularity of a project_ determine their success in directing donations) started to become more and more influential, and harder to overcome.

# Solution.
Quadratic Treasury leverages on **AAVE** Native Credit Delegation & on a Mutual Credit system (**DistributedTown**) to offer a solution to these problems, by (1) letting Public Goods donors and supporters donate directly in a specific area of Public Goods (currently: _Blockchain/Open-source_; _Art&Events_; _Local Communities_), and (2) by using a 2-step quadratic distribution to match this area-specific pool of funds with the public projects that achieved the highest amount of milestones in that given range of time. It also uses (i.) a Mutual Credit system that works as an internal "score" for DAOs & Communities, and (ii.) a unique, universal Identity layer (DID) based on Skills & Contributions, rather than personal data. Making it sybil-resistant and 100% pseudonymous by design.

# Core values:
1. Self-organization and Pseudonimity.
2. Permissionless & bureaucracy-free.
3. Self-sustainability & Collective Autonomy (Inter-Independency). 

The project aims to let local and online communities & DAOs manage their projects (larger or smaller) in full autonomy - both by receiving constant inflow of grants from a pooled fund, or by pooling their funds together, accruing interest on them, and redistributing them to the most impactful projects, in a fully automated fashion.

# How it works:
## Roles:
1. On one side, Members of a DAO, a collective, or a local community can easily Stake and Pool together their funds providing liquidity to the AAVE protocol, in order to accrue returns and redistribute funds and interest to internal projects based on each project's individual milestones achieved. This allows them to organize their projects in an efficient manner ("coordination problem"), and administrate collective funds in a sustainable, fully decentralized way.

2. On the other side, individual supporters and larger donors can seamlessly and trustlessly delegate their donations to the Quadratic Treasury, for it to automatically distribute it to the projects in the area of Public Goods based on milestones achieved in each distribution _snapshot_. In just 2 steps, they can select the Area (currently: _Blockchain/Open-source_; _Art&Events_; _Local Communities_) of Public Goods they want to support, and the repayment structure (0-to-50%), in case they wish to receive back part of their investment+interest. Also, this model _allows Q2T to bring non-repayable loans/grants on the DeFi space, and spares DAOs/projects the time that they would have wasted in tiring and bureaucratic processes to attract grants and external expertise._

## Specifics:
- Each community has its own ID
- Each community member has a unique Skill-Wallet, with the credits they have earned. 
- Each community has a __“Checkup score”__ - based on the *“variety coefficient”* of the skillset available internally, and the Milestones achieved by the internal projects. 
- Milestones are efficiently validated peer-to-peer and off-chain, and verified one-by-one through a decentralized oracle integration (**Chainlink**)

# How we are building it
- AAVE Native Credit Delegation for staking, delegating & borrowing (done)
- Chainlink Oracle for off-/on-chain Milestones verification (done)
- DistributedTown for Mutual Credit system + DIDs (done)
- Solidity Contracts (done)
- Biconomy (for gasless meta-transactions - WIP) 
- Matic L2 deployment (WIP)

# First milestones
- 15/01: Join __MarketMake Hack__ and start designing the protocol
- 22/01: Start coding
- 02/02: First Prototype
- 07/02: Submission @ __MarketMake__

# Repos:
- [**Smart Contracts**](https://github.com/Q2T-Fund/Q2T-Fund-contracts)
- [**Frontend**](https://github.com/Q2T-Fund/Q2T-Fund-frontend)

# Links & Contacts:
- [MarketMake Demo](https://www.youtube.com/watch?v=Ww6GojVJeSI)
- [Website](https://q2t.fund)
- [App Prototype](https://app.q2t.fund)
- [Alex](https://t.me/jabyl)

# Contracts deployed on Kovan and verified on Etherscan:
[**Gigs Registry**](https://kovan.etherscan.io/address/0x702fD6F0eb39FA5911106C27b488771C14fa0127#code)<br />
[**Community**](https://kovan.etherscan.io/address/0xb9d61c7D119163598Ae45c2b6c01A9C4607F7984#code)<br />
[**Community Treasury**](https://kovan.etherscan.io/address/0x3CFCae3fe95f555783E13DF1ce6697602608f66D#code)<br />
[**Validator (Chainlink)**](https://kovan.etherscan.io/address/0xBe5a890Ad011709c26c31C11D24b5eCbf4cdC245#code)<br />
[**DITO Credits**](https://kovan.etherscan.io/address/0x847C0b0549bBB4c4327Fa6812cc889fbea162ee0#code)<br />
## DAO Templates
[**Blockchain/Open-source**](https://kovan.etherscan.io/address/0x912261b12Dfcb4f13c8955324870cA21676F6291#code)<br />
[**Art & Events**](https://kovan.etherscan.io/address/0x555c643cbC1119132a0736B6Fe8df2D41a09537f#code)<br />
[**Local Communities**](https://kovan.etherscan.io/address/0x98fF76Dbe4b7E931204788c676FE4D22565f825D#code)<br />
