# Quadratic Treasury (Q2T)
Q2T combines _DIDs_, _Mutual Credit_ & _Quadratic Funding_ to allow (1) a sybil-resistant, fair mean for donors to support Public Goods - and (2) a way for projects to attract _funds_ and _non-repayable loans_ in a **permissionless** fashion, based exclusively on **the milestones achieved**.

# Links & Repos:
- [**Demo**](https://www.youtube.com/watch?v=Xf__qinVamM)
- [**Functional Prototype**](https://1005agh6pbko9okg69o4n47ohkmu2b3au5acf9g9hd9248v6lpja4r8.siasky.net/)
- [**Pitch Deck**](https://tiny.cc/Q2T-pitch)
- [**Smart Contracts**](https://github.com/Q2T-Fund/Q2T-Fund-contracts-polygon)
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

2. On the other side, individual supporters and larger donors can seamlessly and trustlessly delegate their donations to the Quadratic Treasury, for it to automatically distribute it to the projects in the area of Public Goods based on milestones achieved in each distribution _snapshot_. In just 2 steps, they can select the Area (currently: _Open-source & DeFi_, _Art, Events & NFTs_, _Local Projects & DAOs_) of Public Goods they want to support, and the repayment structure (0-to-50%), in case they wish to receive back part of their investment+interest. Also, this model _allows Q2T to bring non-repayable loans/grants on the DeFi space, and spares DAOs/projects the time that they would have wasted in tiring and bureaucratic processes to attract grants and external expertise._

## Specifics:
- Contracts deployed on Polygon main net and fully functional
- Anyone can permissionlessy donate to Public Goods projects (current Templates: _Open-source & DeFi_, _Art, Events & NFTs_, _Local Projects & DAOs_)
- Donations can be made in DAIs or USDTs
- Donations go to the Q2T.sol contract (ERC1155)
- Donors can customize their Delegation Agreement leveraging on **AAVE Native CD** (repayment structure: 0 to 50%)
- Once a Project hits enough Milestones (3840 Credits), a new Quadratic Distribution is triggered. 
- A snapshot is taken, and each Community with active Milestones in that epoch, will receive a % of the Distribution. 
- Q2T.sol contract mints 2 (_burnable_) ERC721: templateTreasury and repayerTreasury
- templateTreasury stores (100% - repayment)/2 of the donation for each template, and gets destroyed after the Quadratic Distribution is completed.
- repayerTreasury stores the Repayment requested by the donor (0-to-50% of the donation). Once there is enough yield to repay the Donor, the Donor can request withdrawal, and will receive Repayment Structure + yield accumulated.
- (100% - repayment)/2 is always stored in the Q2T reserve, to (1) guarantee constant liquidity, (2) maintain a _health score_ (LTV) higher than 1.3, and (3) guarantee maximum degree of safety for donors and projects.
- 
### Validation & Sybil-resistency:
- Each community has its own ID
- Each community member has a unique SkillWallet, with the credits they have earned. 
- Each community has a __“Checkup score”__ - based on the *“variety coefficient”* of the skillset available internally, and the Milestones achieved by the internal projects. 
- Milestones are efficiently validated peer-to-peer and off-chain, and verified one-by-one through a decentralized oracle integration (**Chainlink**)

# How we are building it
- All contracts are deployed on **Polygon Main Net** for affordable micro-donations (almost gas-free), speed and improved UX.
- Leveraging on **Skynet** CI/CD flow and web deployment are decentralized and fully automated
- **AAVE _Native Credit Delegation_ and _Lending & Borrowing_** and for staking, delegating & borrowing
- **Chainlink Oracle** for _off-/on-chain Milestones verification_
- **Textile Threads & Buckets** for Decentralized, persistent cloud storage for Projects & Milestones metadata.
- [**DistributedTown**](https://github.com/distributedtown/about) for Mutual Credit system 
- [**SkillWallet**](https://github.com/SkillWallet/contracts#readme) for DIDs (done)
- Solidity Contracts (done)
- Polygon Network
- Biconomy (for gasless meta-transactions - WIP) 

# First milestones
- 15/01: Join __MarketMake Hack__ and start designing the protocol
- 22/01: Start coding
- 02/02: First Prototype
- 07/02: Submission @ __MarketMake__
- 11/02: Won AAVEngineer Award (@ __MarketMake__, Sponsor: _AAVE_)
- 11/02: Won _Best Project built with Chainlink_ (@ __MarketMake__, Sponsor: _Chainlink_)
- 25/02: Join __Encode: Hack the System__ and start re-designing the protocol for production.
- 23/03: New Frontend, Textile integration and improved contracts.
- 04/2021: Contracts deployed on **Polygon Main net**.
- 04/2021: _Web Deployment & CI/CD_ flow using **Skynet**.
- 02/05: Submission @ **Encode: Hack the System**.

# Repos:
- [**Smart Contracts**](https://github.com/Q2T-Fund/Q2T-Fund-contracts-polygon)
- [**Frontend**](https://github.com/Q2T-Fund/Q2T-Fund-frontend)

# Links & Contacts:
- [Encode Demo]()
- [MarketMake Demo](https://www.youtube.com/watch?v=Ww6GojVJeSI)
- [Website](https://q2t.fund)
- [App Working Prototype](https://1005agh6pbko9okg69o4n47ohkmu2b3au5acf9g9hd9248v6lpja4r8.siasky.net/)
- [Alex](https://t.me/jabyl)

# Contracts deployed on Polygon Main net:
[**Q2T**](https://explorer-mainnet.maticvigil.com/address/0xc015c3a36d8Fb3A8Ef118Bd1026c2cC6AA946ba7)<br />
[**DistributedTown**](https://explorer-mainnet.maticvigil.com/address/0x2B8f17CBf3854cBc4602Eb18012FE395db559dAc)<br />
[**Projects**](https://explorer-mainnet.maticvigil.com/address/0x3226E081284103D9e99727015EcAC8ba9BA6CbB3)<br />
[**SkillWallet**](https://explorer-mainnet.maticvigil.com/tokens/0x822a6A53c355B953089506bBAae4f122343Ce025/token-transfers)<br />
[**DITO Credits**](https://kovan.etherscan.io/address/0x847C0b0549bBB4c4327Fa6812cc889fbea162ee0#code)<br />
**Milestones** ([1](https://explorer-mainnet.maticvigil.com/address/0x43284D2035Fc7e2dDcC304F2eD9E9935D9b22aa0/transactions), [2](https://explorer-mainnet.maticvigil.com/address/0xcDC90447Ee654B1a90068FB41445a198E06fbA6F/transactions), [3](https://explorer-mainnet.maticvigil.com/address/0x0506bCb805ed40e7e1173ee620Be67Ab08aEEFB1/transactions)
[Projects](https://explorer-mainnet.maticvigil.com/tokens/0x3226E081284103D9e99727015EcAC8ba9BA6CbB3/token-transfers)
