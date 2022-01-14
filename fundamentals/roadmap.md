# Roadmap

{% embed url="https://nexus.io/roadmap" %}

### Roadmap

**Trust System - (Released 09/16/2018)**\
This milestone marks the introduction of the new trust key decay rate, with trust decreasing 3 times faster than it accrues. Replacing the hard 24-hour time limit in September 2018, the new decay rate gives staking wallets greater ability to retain trust and more accurately reflects the effort invested in securing the blockchain.

**Legacy Mode - (Released 06/26/2019)**\
Full update to Nexus Core software supporting Legacy blockchain operation. This mode features fast sync times, instant loading, and a small memory and disk footprint.

**API / SDK - (Released 11/05/2019)**\
Our API gives developers access to a wide set of features available through a simple HTTP interface. This provides easy access to smart contracts that can be embedded directly into web applications and existing login systems.

**LISP - (Released 01/31/2019)**\
The Locator/ID Separation Protocol is an important network protocol that allows one to control their IP addressing, without relying on ISPs for allocation.

**Interface / Wallet - (Released 06/26/2019)**\
The Nexus interface supports full wallet function. Modular functionality allows custom themes and addon modules such as Binance trading, multi-coin storage, a block explorer, Tritium features, and anything module developers might dream up.

**Mobile Wallet - 95% Completed**\
Our official mobile wallet will be developed using most of the software that runs the desktop wallet, with changes to the interface to be more mobile friendly, and daemon packages that incrementally will be improved over time to enable more contract functionality and staking. The Mobile Wallet will still have the modular design of the Nexus Wallet, so that developers can extend it with their DApps by simply deploying new modules to the Wallet.

**Pooled Staking - 90% Completed**\
As more people continue to join the staking process, the network becomes more secure through the increase in the Trust channel difficulty. Though this provides benefits to the network as a whole, it constantly drives up the required amount of coins to maintain a Trust key. Pooled Staking solves this by giving smaller balances the ability to collaborate with peers, ultimately resulting in increased staking access to the regular user, and higher network security. This approach does not require a central service, since it will work as a sub network inside Nexus, that itself comes to consensus on the Trust keys to be included. This is a pure, decentralized, staking protocol that will benefit the entire network as a whole.

**The P2P Market API - 80% Completed**\
The Decentralized Exchange will sit mainly in the Logical / Interface layers, with the exchange itself being facilitated by a conditional contract on the Operations layer. The DEX will be able to be used to trade tokens and assets listed on Nexus, promoting the development of decentralized marketplaces where any type of asset can be traded in a truly free, peer to peer manner without a need for a custodian service. There is no authority that designates the process of listing, and there are no other parties involved in the exchange other than the buyer and the seller.

**Augmented Contracts - 30% Completed**\
Augmented Contracts are the second type of contracts that will be available in the Tritium Protocol. These types of contracts extend the Conditional VM (Virtual Machine that processes Conditional Statements) to provide additional benefits including, but not limited to, methods, functions, operation overloading, and encapsulation. Augmented contracts add a layer of complexity and processing, so will carry a higher fee to execute. This will require more on-chain processing, but overall makes our Contract Engine much more powerful.

**Hybrid Mode - 90% Completed**\
An important feature, hybrid mode is capable of forming an individual network out of the box, making it a highly useful tool for businesses that wish to utilize our blockchain technology, while retaining high levels of privacy.

**Object Modeling - 80% Completed**\
Object Modeling is a new feature that will extend the API layer allowing developers to model their Object Registers in languages such as XML (EXtensible Markup Language). This will also contain modeling languages that will make it possible for advanced developers to work with lower level object operations. These could include using specific data types and specifiers, developing more complex object behavior through Augmented Contracts, or creating extra conditions that regulate the object’s overall behavior.

**Protected Assets - 0% Completed**\
Protected Assets are a type of asset with the addition that a ‘Master’ owner retains the right to revoke access to the asset. This essentially allows the asset creator to have permanent access to an asset, which is necessary for securities, collateralized loans (DeFi), non-transferable assets (Tickets, Educational/Professional Awards and Certificates, Certificates of Insurance, Licenses etc.). They are also useful for protecting the asset from being transferred to unqualified parties, or in other words, parties that do not fulfill the requirements set out by asset creator.

**LLD Global File System — 20% Completed**\
The LLD global file system will support secondary files that record assets to be stored and retrieved through network operations, providing a seamless interface for managing assets and data.

**Contract Domain Specific Languages — 20% Completed**\
Contract-specific programming languages will be provided that will include internal safety mechanisms such as catching overflows to allow more complex contract development, while remaining less prone to error.

**pBFT + Reputation Channels (L1) - 0% Completed**\
This new architectural component will process transactions in parallel, using reputation as an additional weight to provide higher security. The transaction speed of L1 channels will vary based on the risk that a merchant wishes to assume, ranging from sub-second speeds to 5 seconds. For higher value transactions, it will be recommended that they receive additional weight from validation on the next consensus layer: L2, reducing transaction speed to 15 seconds plus.

**pBFT + PoS Trust Network (L2) — 0% Completed**\
As an extension to the existing Proof of Stake system, L2 will form the second layer of consensus above the L1. The L2 layer ensures safety and liveness, cross-shard communication, and resolves conflicts from the L1 layer. It represents the horizontal chaining of the L1 channels, and is a major step towards a truly decentralized and scalable ledger.

**Network Data Sharding — 0% Completed**\
Data sharding is an essential facet of our ledger design in order to achieve long-term scalability. Amine will provide the opportunity for nodes to run in “shard” mode, which will lower their disk and memory usage, even when the network is under high load.

**LISP Multicast Links for (L1) and (L2) — 20% Completed**\
Using LISP, the L1 and L2 layers will have their own Multicast links, therefore packets and transactions will route in constant time no matter how many nodes are part of the system.

**Application Store — 20% Completed**\
Here applications and modules will be able to be shared and sold in a decentralized marketplace. Modules will provide developers the building blocks to create applications.

**Extended Network Data Sharding — 0% Completed**\
Data sharding in Obsidian will extend to critical network functions, resulting in nodes being required to store only a portion of the overall chain. Note, this is **data** sharding, not computational sharding, which means once data has been processed, it can be partitioned and stored between nodes. The result will be an increase of data storage as more nodes join the network.

**Decentralized Mining & Merkle Share Pool (L3) — 0% Completed**\
This component will use Proof of Work based mining shares computed from the work performed by the nodes of L2. Consensus will be determined by the largest value of shares + trust, in order to reach the final agreement on the most valid 3D block.

**DAO: L1 Voting Group (Implement)— 0% Completed**\
The L1 voting group will provide voting rights to validators who are new to the network, and therefore do not have enough resources to participate in the L2 consensus. Voting weight is based on reputation.

**DAO: L2 Voting Group (Extend)— 0% Completed**\
The L2 voting group will extend Tritium’s “Ambassador DAO” and provide voting rights to validators who have reached a reputation threshold. Voting weight is based on reputation multiplied by stake.

**DAO: L3 Voting Group — 20% Completed**\
The L3 voting group will provide voting rights to miners. Voting weight is based on mining power (average weight of mined shares over time) multiplied by reputation.

**LISP Multicast Links for L3 - 0% Completed**\
Shares on L3 will use LISP Multicast links allowing the efficient broadcasting of mined shares, and the acceptance of L2 hashes for computation by L3 nodes.

**Click here to view the roadmap progress bars.**

**Updated December 2021**
