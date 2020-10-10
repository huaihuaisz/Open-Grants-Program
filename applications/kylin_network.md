# Open Grant Proposal

* **Project:** Kylin Network
* **Proposer:** [Kylin Labs](https://github.com/Kylin-network)
* **Payment Address:** 3FmU9VRXhnMkgBbQVx1cooYUAuDEajdibm

## Project Overview :page_facing_up:

### Overview

#### Introduction
**Kylin Network aims to Build a Cross-chain Platform Empowering the Data Economy on Polkadot.** It offers any applications and blockchains (such as parachains and parathreads) instantaneous but reliable and valid on/off-chain market data and social data sources by leveraging the power of Polkadot. Kylin Network represents an extensibility and synergetic increase to the off-chain workers capability as it will provide not only access, management, coordination to a greater array of data sources, but bolster validity and decentralization of the data sources themselves. Kylin Network therefore hopes to achieve complementarity and synergy with [Substrate](https://github.com/paritytech/substrate) Framework while providing valid, reliable, and easily-coordinated data sourcing.
![img](https://lh5.googleusercontent.com/T22rYBCvtyDbo7HI5Hs9LUdCzzEWStcR2b2xs8h2kvEUdP2QjpdlRgAf1lhKw1TOhlmfWWf1btNPMwIszcRMIq8iWPBAG_1zFx-iFdwEOd8j61TK9rCOlpr4T2ToHhanvkM7IAg2)

### Team Interest
The Kylin team comprises talents from different fields of the digital world, ranging from traditional marketing, project operation, full-stack development to cryptocurrency early adopters and evangelists. This team believes it is a group of strong exponents of reforming the status-quo and making substantial contributions that can propel us into the next stage of data exchange and sharing.

Although the market has witnessed a preponderance of projects that try to unravel the oracle problems, most of them were, unfortunately, defeated by the data streams dilemma, which is the inability to funnel the real and instantaneous data onto the blockchain to create greater social value. After learning the developments of Polkadot network expansion and the Substrate 2.0 Framework upgrade, we believe Kylin Network can serve as a competent facilitator between the supply and demand equation.

### Project Details

#### Existing Problem and Our Solution

1. DeFi is the most successful application in blockchain, but we don't want this to be the only one because of lack of valid external data. In a mature web 3.0 world, the number of data sources will be diverse and many, and will not be limited to price feeds alone Indeed, proper middleware will also have as its focus things such as stock price, twitter feeds, real-time election results. The need for an array of validated data resources has never been higher.
2. Due to the previous lack of [off-chain workers](https://www.parity.io/substrate-2-0-is-here/) (OCW), many off-chain data cannot efficiently get connected to the blockchain. Substrate 2.0 framework provides OCWs as a default solution to [integrate real-world data](https://github.com/open-web3-stack/open-runtime-module-library/tree/master/oracle) safely and securely onto the blockchain via oracles without the need to get opt-in by each validator - in other words, it's a default unlocking of oracle validation across all of substrate.
3. There are many weaknesses of Ethereum, especially high transaction cost and low scalability. Thus, implementation based on the Polkadot network and its cross-chain interoperability is a better solution for the blockchain ecosystem. Thus, our choice to build within Substrate/Polkadot.
4. While OCWs are excellent at performing the basic functions of oracles, etc., they do rely on a 'manual' request (low-level TCP API request not available in WASM). Kylin Network would also provide the means to integrate into OCW functionalities and (Dapp builders' capabilities) what would be essentially tantamount to a single, easy-to-use request library (no need to make some sort of wrapper in WASM).
5. There is an exigent need to coordinate and validate data sourcing and also make more efficient the process of requesting via OCW functionalities. Our work would extend both.

Therefore, we need a state-of-art solution to solve the above problems. The architecture of Kylin Network includes below main components:
* **Kylin Data Oracle** is a decentralized oracle network powered by Polkadot offering multiple, real-time data sources. In addition to the complementarity and synergy to off-chain workers (OCW), Kylin seeks to extend the data provisional resources of the Polkadot network across all possible data types/sources including, but not limited to things like social media posts, flight information, exchange rates, weather reporting, etc.
* **Kylin Data Marketplace** is an open platform for the data economy. Dapps built on Polkadot can access this platform to easily and efficiently collect both off-chain and on-chain data only paying a very competitive fee.
* **Kylin Data Analytics** is a combination of analyzing tools designed for data warehouses. It extracts meaningful data findings, patterns, interpretation, and finally implements low-cost commercialization functionalities for the public.
* **Kylin Token $KYL** is the native token of Kylin Network which will play the role of governance and other utilities. $KYL is necessary to secure and power the decentralized oracle network.
![img](https://lh6.googleusercontent.com/ErkoMCbuwptc5xTYadvjINwl2x9Tvviu7ekpo4WbnYx2a0QAVia2ADiH2ADLjLD8105aUZ2ZrmeImDIbDgyOkWGNC10kbXWBsj9FNy-i2awIqWvNRhE-_-CT8v91Y8gMfpBaH8Oo)

### Project Architecture

#### Oracle Network

Kylin Oracle provides a reliable, efficient and trustless solution for off-chain data. The protocol runs in a purely decentralized and scalable manner. Kylin Oracle, which is built on Substrate, will be connected to the Polkadot ecosystem as a parachain, sharing the underlying consensus of Polkadot. The security and network performance will be guaranteed by Polkadot and Substrate.
![img](https://lh4.googleusercontent.com/vjzbdu7qXgXJLrA8b38lgZeod9PyZCYn0_IPapsdN_s2YrPZp84baKJcUhiqeRpHDXe473rxMB-5gJB9ejuzUeCvp_sGB_zheLRYdSNH4MZ4sWcNvYY3MHuIAZv7TpTx2kgEeLkS)
In the schematic diagram above, [Kylin Oracle](https://kylin.network/Kylin-whitepaperV1.0.pdf?4) encompasses five entities, including Data Consumer, Data Warehouse, Oracle Node, Arbitration Node and Blockchain Node. These five entities represent the major components of Kylin's architecture. The details and the interrelated relationships of the components are as the following:
* **Data Consumer (Requester):** Data consumers may represent smart contracts, APIs, blockchains, protocols, applications or any data repository that calls up the Kylin Oracle and pays the fee by the native token $KYL.
* **Data Warehouse (DW):** Data Warehouse in Kylin Protocol is a decentralised on-chain repository of integrated data. Data Warehouse stores the query queue and historically validated data/value that contracts or any other Data Consumers can read from.
* **Oracle Node (Miner):** Oracle Node handles all the data requests such as social data and market data from separate off-chain data sources, and signing the transactions of the Kylin parachain.
* **Arbitration Node (Arbitrator):** The Arbitration Node guarantees the security and accuracy of external data by verifying the data integrity and the validity that Oracle Node provided. The Arbitration Node has the right to challenge the validity of a mined value or data by Oracle Node in the challenge time by paying a challenge fee.
* **Blockchain Node (Validator):** The bottom layer of Kylin Oracle is mainly built on a specialized blockchain network established by Substrate. It allows the oracle node to broadcast the mined value and the proof of calculation, then support the arbitration node to verify the validity of mined value. All the nodes including the oracle node and the arbitration node need to subscribe to the blockchain node in order to read on-chain events and send back the responses.

The basic flow of Kylin Requester Model for adding and retrieving data is as follows:
1. When the Data Consumer creates a data request, a data query will be submitted to the Data Warehouse by sending an on-chain transaction to the Data Warehouse to incentivize the miners to process this query over other submissions. The queries for the same data will further incentivize the miners to handle the submission first.
2. The Data Warehouse tracks the on-chain transaction from the requesters and broadcasts the message over the off-chain oracle network when it receives the service fee in native token, $KYL. Miners (the oracle nodes) will monitor the blockchain for these messages and will begin processing the requests.
3. Miners submit their mined data/value and the proof of calculation to the Arbitrator's network. If the validity of the mined data has not been challenged, the mined data will be submitted to the Data Warehouse, saved on-chain with 9 more mined data. Then the Data Warehouse will update the balance of native token to pay the miner who submitted the reliable and valid value.

#### Substrate/Polkadot Integration

Polkadot ecosystem and the newly-updated Substrate 2.0 are essential to what Kylin Network is trying to achieve. Kylin Oracle will be connected to the Polkadot ecosystem acting as a parachain, sharing the Polkadot underlying consensus, and protected by the network performance of Polkadot and Substrate. Polkadot/Kusama is the important foundation, on which Kylin Network and its components are built.

The pallets that come with the Substrate 2.0 upgrade can offer Kylin Network the tools and maps to navigate through our vision, which is to build a decentralized oracle that offers on/off-chain data with built-in interoperability. Off-chain worker (OCW) is a substrate subsystem which can process off-chain data in an asynchronous way. It is a new feature in Substrate 2.0 that allows to integrate data onto the blockchain. It can make off-chain data integration secure and more efficient, which is ideal for real-world data inputs via oracles. The off-chain worker subsystem allows execution of longer running and possibly non-deterministic tasks (e.g. web requests, encryption/decryption and signing of data, random number generation, CPU-intensive computations, enumeration/aggregation of on-chain data, etc.) leveraging on-chain data and access. Thus, we have the Data Warehouse in the system which will deal with Date Feeds and Data Requests sent by the user in a local data store or even a decentralized data storage such as IPFS.
![img](https://lh6.googleusercontent.com/km4l2pyVhLBg5qT_inXBwcIao1YDCLHWzd55SILF4XA10VAMAOiijoehDMkuBB1BvVaW-ngBdt8B07zjqwmsFmo5-foCaQR5jIln0aV92r390tyvuNwwCwxBF1ooJSP_nJIc01Tc)

The Kylin team will utilize the off-chain workers modular to incentivize users to provide verified out-of-blockchain data to the Kylin Marketplace and Kylin Analytics will provide any party with the tools to make sense of the data uploaded. The marketplace is built for data collection and data exchange. The analyzing toolkit will include raw data collector, data preparation, data editor/coding and quantitative data trend generator, with more future features to be developed.

The Kylin team is a strong exponent of reforming the status-quo and making contributions that propel us into the next phase. Although there has been a wave of projects trying to solve the oracle problems, most of them failed due to the not-effectively-verified or easily-manipulated data streams. We believe, standing between the supply and demand equation, Kylin Network can serve as a competent facilitator particularly when powered by Polkadot and Substrate 2.0. It will benefit the Polkadot ecosystem.

#### Data Marketplace

Data marketplace is one of the trillion dollar businesses around the world. The data marketplace will function as the next logical extension of Kylin Network's ability to warehouse validated real-world data to flow unobstructed with the kind of throughput necessary for comprehensive oracle solutions. Validated data can be coordinated and managed such that the targeting of premium data feeds becomes possible. Specifications surrounding access to data via data feeders can be set up autonomously by the data provider in addition to cost of access in KYL. Furthermore, capturing and coordinating all this data allows a 'one-stop shop' for DApp developers to inform and ease the process of building. Using the hosted server only as a caching layer, it's ensured that all info is on-chain, and only interacting directly with our parachain and IPFS.

The process flow for a data feeder would go as follows: register and connect and then publish specifications and offers for their feed (this will include things like API request 'library', pertinent addresses, reward/payment scheme, like subscription or pay-per-use). To reduce friction further, an SDK will be enabled for premium data feeders.

A use case scenario could operate as such:
* Data feeder is registered and provides pay-per-use information on a premium data feed (pork belly futures from CME Group, Inc., for example); data consumers would search for 'pork belly futures' from the marketplace contracts and pick whatever result seems the most suitable.
* CME Group provides their data on a monthly subscription basis to the consumer.
* If the data consumer should not find a result, then they can request a bounty be approved for getting the data provider initialized and/or integrating them.
![img](https://lh6.googleusercontent.com/F0iC9QG1o444sEGysIoF-L_wpGGIXmEOfRnrIyW20Ur044pbgO1skIrBeLhIFPp1Ss4lau8J9xnAx1Po91kTC6DtH7Muq2HQqJaEdXoxiz1o5yC4BTUax9oAeHzbE_xz_HuCLSU-)

Besides, user contracts calling for a specific category of off-chain premium data would simply search for existing ones from marketplace contracts and pick the most suitable one. If there's no such premium data feed available on-chain yet, developers could start a bounty using $KYL tokens and the community would reach out to corresponding data providers to help integrate their service on-chain.

#### Privacy and Security

As Kylin Network will provide real-world data to on-chain transactions, security will be placed as a top priority since cyber security issues are quickly becoming a regular occurrence and exposing confidential business information.

We will employ a novel approach to user identity management in blockchain services. We implement identity-based end-to-end security which extends from the blockchain client to the blockchain fabric. This approach allows for nodes-based network segmentation and traffic separation, which enables multiple entities to securely share the same blockchain infrastructure, reduces the risk of DDoS attacks, and enables automated regulatory compliance audits. The solution is based on Kylin Oracle Transport Access Control (KTAC) technologies, implemented using software application library endpoints. This approach can easily be generalized to protect many different types of commercial applications. KTAC features include permission control, confidentiality, un-linkable identity privacy for blockchain participants, a modular and easily auditable consensus protocol, and improved scalability. KTAC extends the blockchain in several important ways.

We will employ the Kylin Oracle Real-time Transport Protocol (KRTP), a profile of the Real-time Transport Protocol (RTP), which provides confidentiality, message and data authentication, and replay protection to the RTP traffic and to the control traffic for RTP, the Real-time Transport Control Protocol (RTCP). KRTP provides a framework for encryption and data authentication of RTP and RTCP streams. KRTP defines a set of cryptographic transforms, and it allows new transforms to be introduced in the future. With appropriate key management, KRTP is secure for unicast and multicast RTP applications.
![img](https://lh6.googleusercontent.com/k_YavNHdtkRolT2bry5e3QQHqVofGsfWnyljY_vJxDkxLa2pPYdI3xpt9BgAyANeaFGl2aeMC3SBjZBj1pcs82oZMykwW2Ce1Wn_yvXsZvSq6yrC3Zkunz1uZEXo5xFOAQHrOfcL)
Kylin Oracle Network will also apply Verifiable Random Function (VRF) and Threshold Cryptography to drive the secure, unpredictable and verifiable random group selection. Different oracle requests will be handled by randomly selected worker groups. Threshold cryptography will then be applied in the worker group to collectively generate a proof to demonstrate data integrity. Finally, the proof along with the data will be sent back together to the system contracts within one transaction for on-chain verification.

#### Token Economics

\$KYL is necessary to secure and power the decentralized network. The use-cases and utility of $KYL include:
* **Stake to be Oracle Node and Arbitrator Node:** All miners are required to stake $KYL with a higher stake equating in a high probability of being selected to fulfill data requests. Underperforming or malicious actors will result in having their tokens and thus value slashed.
* **Intermediary of Exchange:** $KYL tokens will be used to pay as a transaction, query fee, and also for data access behind paywall (private APIs).
* **On-chain Governance:** $KYL Token holders are able to vote for the protocol upgrades and parameter changes on Kylin Network. The governance process allows the token holders to have decision making power in shaping a truly decentralized oracle network.

### The Purpose of this Grant
In terms of the system architecture of Kylin Network, the purpose of this grant is to verify features with limited users and launch the testnet for production of concepts. Besides, the implementation of off-chain workers of Substrate 2.0 Framework will be built and validated in a lean way. As we mentioned above, the whole project has four main components, the development roadmap will take at least one year to deliver the platform. At that time, we believe Kylin Network will empower the data economy effectively.

### Ecosystem Fits

There are some existing projects which can support and work with the Kylin Network.
* [Ocean Protocol](https://oceanprotocol.com/): Ocean Protocol helps developers build marketplaces and other apps to privately & securely publish, exchange, and consume data.
* [Plasm](https://www.plasmnet.io/): Plasm Network is a scaling dApps platform on Substrate.
* [Moonbeam](https://moonbeam.network/): Moonbeam is a new Polkadot smart contract platform that makes it easy to build natively interoperable blockchain applications.

### Application Scenarios

The application scenarios include but not limited to:
* **Decentralized insurance automatic payment:** Through the Kylin Network to obtain timely and reliable events outside the insured chain, blockchain-based decentralized insurance can realize automatic payment of insurance such as flight delay insurance.
* **Stable coins and crypto derivatives:** Stablecoins and encrypted derivatives need to frequently obtain off-chain real-time price data. Kylin Network can obtain reliable data in multiple scenarios in real time and efficiently.
* **Crypto asset lending platform:** Kylin Network can provide real-time and reliable currency prices and borrower's social media information, providing strong support for the dynamic determination of loan interest rates.
* **Cross-chain decentralized exchange:** The lightweight Kylin Network interface that can be deployed on multiple chains provides the possibility for decentralized exchanges to realize cross-chain atomic transactions.
* **Decentralized casinos and games:** On-chain decentralized casinos and games often require safe and reliable random injection. Kylin Network random number engine provides unpredictable and verifiable random number generation.
* **Blockchain computing market:** Commercial computing such as machine learning training models and 3D rendering needs to complete a variety of complex computing tasks. The off-chain computing market provides verifiable and unlimited off-chain computing capabilities.

## Team :busts_in_silhouette:

### Team Members

* Dylan Dewdney - CEO/Project Leader
* Beni Issembert - CMO/Head of Advisory Board
* Kyn Chaturvedi - Strategy Advisor
* Kevin Hsu - Data Scientist
* Aaron Po - Full-stack Developer
* Andy Zhuang - System Architect/Substrate Developer
* Jerry Shen - Back-end Software Engineer
* Bob Ma - Front-end Software Engineer

### Team Website

- https://kylin.network

### Legal Structure

Digital Asset FOF Ltd. is a company registered in Cayman Islands.

#### Team experience

**Dylan Dewdney**  
   &emsp;\-   Longtime (2011/12) crypto enthusiast, miner, investor  
   &emsp;\-   Co-founded Harbour DAO 2017  
   &emsp;\-   GTM for Beam.mw + Chief Evangelist  
   &emsp;\-   Head of Growth, AdEx  
   &emsp;\-   Investor and Advisor to Ramp and other projects  

**Beni Issembert**  
   &emsp;\-   15 years of proven experience as entrepreneur and global marketer within the scientific and technology sectors: Founder, Titan Poker; Founder, JJF Media Ltd., External CMO, ConnectJob  
   &emsp;\-   GTM for BEAM.mw + Chief Marketing Officer  
   &emsp;\-   Current CMO for Concordium  
   &emsp;\-   Published Author; PhD John Hopkins  
   &emsp;\-   Member of the Open Source Initiative 

**Kyn Chaturvedi**  
   &emsp;\-   Experienced Strategist across multiple verticals in digital technology with a demonstrated history of working in the gaming industry. Skilled in developing and implementing Go-to-Market strategies, Partnership Development, and Product Management.
   &emsp;\-   Current CBDO of Tomochain  
   &emsp;\-   Wharton Grad (2011)  

**Kevin Hsu**  
   &emsp;\-   MSc in Computational Statistics and Machine Learning from UCL and supervised by David Silver, the senior engineer of AlphaGO.  
   &emsp;\-   Served as data scientist in Credit Suisse, senior machine learning Engineer in WeCash.  
   &emsp;\-   Prescient and consistent track-record in investment and has invested over 160 blockchain projects around the world.  

**Aaron Po**  
   &emsp;\-   7-year experience in full-stack development.  
   &emsp;\-   Deep knowledge in building scalable systems and blockchain solutions.  
   &emsp;\-   Stack: C#, Java, Rust, Go, Javascript, AWS, Kubernetes, Hadoop, HBase, etc.  

**Andy Zhuang**  
   &emsp;\-   Seasoned development experience in Hyperledger, Ethereum and EOS.  
   &emsp;\-   Expert in the architecture design of DeFi and token economics.  
   &emsp;\-   Senior Software Developer and Data Scientist in Baidu.  

### Team Code Repos

* Kylin Network: https://github.com/Kylin-Network

### Team Linkedin Profiles

* [www.linkedin.com/in/dylan-dewdney](http://www.linkedin.com/in/dylan-dewdney)
* [www.linkedin.com/in/beniissembert](http://www.linkedin.com/in/beniissembert)
* [www.linkedin.com/in/yingkaixu](http://www.linkedin.com/in/yingkaixu)
* [www.linkedin.com/in/kynchaturvedi](http://www.linkedin.com/in/kynchaturvedi)

## Development Roadmap :nut_and_bolt:

### Overview

* **Total Estimated Duration:** 2 months
* **Total Costs:** 1.3 BTC

### Milestone 1

In this milestone, we will verify the concept and technology path of Kylin Network and start to implement basic features.
* **Estimated Duration:** 1 month
* **Full-time Equivalent (FTE)**: 2
* **Costs:** 0.3 BTC  

| **Number** | **Deliverable** | **Specification** |
| ------------- | ------------- | ------------- |
| 1. | License                        | Apache License 2.0                                           |
| 2. | Kylin Network Oracle Node Repo | Oracle node built on top of Substrate 2.0, connected to Polkadot network as a parachain, having the simplest schema of oracle market. |
| 3. |Documentation                  | Documents containing the description of whole architecture design for Kylin Network. |

### Milestone 2

In this milestone, we will verify features with limited users and launch the testnet for production of concepts. The implementation of off-chain workers of substrate 2.0| framework will be built and validated.
* **Estimated Duration:** 1 month
* **Full-time Equivalent (FTE):** 3
* **Costs:** 1 BTC  

| **Number** | **Deliverable** | **Specification** |
| ------------- | ------------- | ------------- |
| 1. | Kylin Network Oracle Node Repo       | Oracle node implemented with Substrate 2.0, integrates off-chain worker. |
| 2. |Kylin Network Datasource Sample Repo | Sample datasource working with off-chain worker, interactive with Kylin Network oracle node. |
| 3. |Docker Image                         | The Kylin Network docker image contains the POC version which can be running anywhere to verify the idea of Kylin Network. |

### Community Engagement

Kylin's current community engagement strategies include:
* **Exposure on Leading Media Channels:** We will release additional articles on Forbes, The Block, CoinDesk, CoinTelegraph and many other leading media channels.
* **Ecosystem Development Lead Program:** We will launch an Ecosystem Development Lead Program to recruit and get more technology and development contributors involved into our project.
* **Promotion of Online and Offline Events:** We will publish an article on medium upon the progress of this project. Meanwhile, we will join Polkadot related off-line events and do online AMA sessions to promote the project to the Polkadot community.

Kylin's future community engagement strategies include:
* **Bounty Program for General Community:** We will reward users who contribute positively in community building, content creation and evangelizing Band Protocol through an Ambassador Program. The community management team will be available 24/7 to answer questions and facilitate discussions in community channels.
* **Incentive Program for Dapp Developers:** Kylin Network focuses on giving developer support through both offline and online channels. Developers can integrate the data with only a few lines of code. The simplicity of integrating this project makes it easy for any developer to experiment.
* **Mining Program for Node Runners:** Kylin Network is targeting a global pool of 100 nodes upon the completed rollout of Kylin Network to achieve the highest degree of decentralization as possible. Gradually, reputable and trusted public nodes will be onboard onto this project to ensure the stability of the network.
* **Incentive Program for Data Providers:** After the main functions are completed, we will set up an incentive program to encourage more market data and social data sources as premium data providers for Kylin Network.
* **Potential IPO during parachain auction for community members:** Kylin Network may hold an Initial Parachain Offering and reward users for helping our auction with $KYL tokens.

## Future Plans

* The Kylin Network plans to become a parachain for the Polkadot network. We have some preparations for auction and we may design a possible community-wide IPO.
* Continuance of Substrate Builder's Program.
* We will hire 5-6 more devs in the next two months. Meanwhile, we will complete advisory support and complete the composition core team functions.
* In phase 1, our goal is to achieve all the basic functions of current oracle solutions, in addition we will begin to build our array of 'non-traditional' data sourcing options for dapp builders to utilize and the functionality of a one-stop shop for data sourcing needs without manually calling each http.
* In phase 2, our goal is a mature data marketplace where Dapp builders and users can easily and effectively coordinate and manage their data needs for a very competitive fee.
* In phase 3, as the maturity, stability and reach of the data marketplace begins to create opportunities for analytics, we will engineer analytics tools to extract meaningful data findings, patterns, interpretations, while implementing low-cost commercialization functionalities for the public.
* Finally, our goal is to fully empower the data economy on Polkadot.

## Additional Information :heavy_plus_sign:

* Website: https://kylin.network/
* Twitter: https://twitter.com/Kylin_Network
* Medium: https://medium.com/@kylinNetwork
* Telegram: https://t.me/KylinOfficial
* Github: https://github.com/Kylin-Network