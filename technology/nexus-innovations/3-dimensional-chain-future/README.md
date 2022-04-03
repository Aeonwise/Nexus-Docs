---
description: 3DC scaling solution for Nexus
---

# 3 Dimensional Chain (Future)

The Three-Dimensional Chain (3DC) is designed to solve the 'Blockchain Trilemma'. It will transform the ledger into a multi-layered processing system, in order to scale securely and with a high degree of decentralization. The Blockchain Trilemma is an opinion that only two of the three qualities, Security, Decentralization and Scalability, are achievable concurrently.

The 3DC chains together cryptographic primitives into a three dimensional immutable object (a 3D block), and has three core dimensions: reputation channels (X), immutability or authenticity (Y), and time (Z). This architecture is being deployed through the [TAO framework](broken-reference).

## Scalability

The architecture of legacy blockchains is comparable to driving a car on a single lane highway – as the volume of cars increases, traffic occurs. Nexus views ‘scalability’ as a requirement, not a feature. Therefore, we design protocols that scale as more nodes join the network, processing unhindered even with the increase of resource requirements.

Using ‘Signature Chains’, ‘Aggregation’ and ‘Computational Sharding’, the 3DC creates parallel lanes of transaction processing to produce the L1 layer, the base layer of the 3DC. Data is then stored between many nodes using what we term ‘Data Sharding’, that eliminates the need for synchronizing and storing the entire blockchain. [LISP](broken-reference) (Location Identifier Separation Protocol) and the ‘LLL’ (Lower Level Library) together form the common interface for this, that results in an increase of distributed data storage as more nodes join the network providing longer term scaling potential.

## Signature Chains

Nexus transactions no longer use the UTXO (Unspent Tx Outputs) architecture, where you have outputs from one transaction being inputs to another, resulting in a large amount of expensive signature verifications for even small transactions. Though UTXO was an important cornerstone of the Bitcoin architecture, it has proven to be outdated and vulnerable to many different types of attacks and scaling limitations.

Why is this important to avoid? [50% of Litecoin’s UTXO is unspendable.](https://www.reddit.com/r/litecoin/comments/9ncqse/what\_should\_we\_do\_about\_the\_50\_of\_litecoins\_utxo/)

As a move away from legacy blockchain architecture, Nexus has designed and implemented an architecture named Signature Chains, that act as personal user-level blockchains containing all of your data in one unique chain. This architecture provides higher scaling characteristics, as only one signature needs to be verified per transaction. Conversely, a single UTXO transaction could contain 1000’s of inputs (and therefore require 1000’s of signature verifications), in order to transact even a small amount of coins (less than 0.00001). Additionally, Signature Chains don’t require wallet.dat files, as they are accessible by login credentials (username, password and PIN). This verifies authenticity and identity of individuals utilizing reputation on the network, without sacrificing privacy.

## Aggregation

Transactions in legacy blockchains are not only referenced in a block, they are also transported with it. Though this does contain some positive characteristics for processing, it limits scale as transactions require transport twice, once when created, and again when the block itself is broadcast. In order to combat this inefficiency, the Tritium protocol stores the transaction object separately from the block object, and references the txid inside the block. This is the first form of ‘Aggregation’, that means that a single reference can represent the entire transaction, thus reducing the data that is transported in blocks. This results in enhanced levels of scaling, and improved security by lowering the probability of successful Finney attacks on the network.

What’s a Finney Attack? [Hal Finney Discovered it in 2011.](https://bitcointalk.org/index.php?topic=3441.msg48384#msg48384)

### Computational Sharding

Computational Sharding is necessary for the division of work between specific types of nodes, to create ‘lanes’ that process data in parallel comparable to multiple lanes of a highway. Though computational sharding is powerful, it can be less secure if implemented incorrectly. The reason is that a ‘shard’ will be easier to dominate than an entire network, as it is smaller. The way to resolve this is through the use of a multi-layered ledger (explained in Security) inherent in the 3DC. Layers of consensus allow the shards below to be smaller in size than those above, safeguarding conflicts from attacks.

### Data Sharding

Data Sharding is the division of data to be stored between many nodes. This can be thought of as having many warehouses to store packages (data) after they have been processed and transported. Due to every object being ‘verifiable’ by its index hash, the 3DC can provide Data Sharding with limited trust in remote nodes.

The difficulty is, how the state of so many objects and shards is managed? The use of [LISP](broken-reference) solves this problem. The method by which the 3DC performs Data Sharding, a ‘network’ is created that exists everywhere, where instead of ‘IP’ addresses, you have ‘hashes’. This could be compared to typing in a txid in your web browser, and receiving that transaction. Using LISP in this manner, we would enable the browser (or LLP in network terms) to open a connection to a hash, which points to the group of nodes that holds a particular piece of data.

The end result of this is, a user can login to their node that has never communicated with the network before, generate a ‘genesis-id’ using their credentials and open a connection to the hash, utilizing the existing internet to route to the node that contains this particular piece of data. The beauty of this is that the network itself doesn’t need to add superfluous data synchronization across nodes to know where data is held. Nodes use the overlay to route remote node requests, resulting in IP addresses as hashes of data that exists in the wonderful world of Nexus.

Data sharding is an essential facet of the 3DC in order to achieve long-term scalability. Amine will provide the opportunity for nodes to run in ‘shard mode’, lowering their disk and memory usage even when the network is experiencing high load. Data sharding in Obsidian will extend to critical network functions, resulting in nodes being required to store only a portion of the entire chain.

## Multicast

Additional to the cryptographic structure challenges described in Data Sharding, the Internet, must be capable of routing efficiently. We utilize what is termed ‘IP Multicast’ that enables a single broadcast of a message to be initiated by a node, rather than every node needing to replicate the message as it is verified. This can be likened to a public speaker broadcasting a message to an audience (multicast), rather than having a one-on-one conversation (unicast), where the message is then gossiped from one person to the next. You can imagine how this would not only improve the scalability, but also the integrity of the message (as gossip often fails to reflect the original conversation). Packets and transactions will route in constant time no matter how many nodes are part of the system.

## Lower Level Library (LLL)

The Lower Level Library (LLL) is the foundation of the TAO framework, enabling support for other web technologies with high reliability, performance, and extensibility. The LLL is a high-performance ‘Template Library’ designed to power emerging-web technologies. Most web technology today is clunky, centralized, and over-engineered as a result of decades of development. The LLL is simple, powerful, and lightweight; made with modularity in mind.

It contains three main components: Cryptography (LLC), Database (LLD), and Protocol (LLP). The Cryptography component contains [Quantum Resistant](broken-reference) cryptography, the Database component out performs Google’s LevelDB by orders of magnitude, and the Protocol component handles well over 450k requests per second.

The Lower Level Database (LLD) is Nexus’ fast and modular storage engine, which to the best of our knowledge, is capable of outperforming most existing embedded database engines. Our average results are around 0.33 seconds for 100k writes and reads to disk (one then the other). This rivals other storage engines such as Google’s LevelDB.

The Lower Level Protocol (LLP) is a fundamental component of the Network Layer, a light and fast protocol that allows a developer to customize their packet design and message interpretation. It gains scalability through simplicity, and is capable of managing a large number of concurrent connections.

The Lower Level Cryptography (LLC) is a light and efficient library that contains many useful cryptographic functions such as post-quantum cryptography, AES and Argon2. The library provides an easily accessible set of high performance cryptographic functions to ensure maximum scaling potential. An example would be our benchmarks of FALCON (used in the TAO) that verified 150k signatures on a consumer grade apple laptop, where ECDSA (Elliptic Curve Digital Signature Algorithm; used in Bitcoin, Ethereum, etc.) performed only 4k signatures.

## Security

Nexus employs multiple consensus systems that ‘check and balance’ one another. Diversity strengthens the gene pool of the human species, likewise it is an equally important property for the security of a decentralized system. The 3DC is designed as multiple layers of transaction processing or ‘consensus’, and each of the layers aggregate data from the layer below. The nodes performing work on L2, resolve any conflicts in L1 shards, using ‘stake’ and ‘trust’ as the ‘weight’ to determine consensus. In the event that there is a conflict, it is resolved through the validity of data, which is defined as (trust + weight). The L3 layer will consolidate hashes from L2 to create the final 3D block.

Nexus considers the use of cryptography very seriously, as a flaw in these functions could compromise the security of the entire network. We only employ well tested and thoroughly peer reviewed cryptography to support increased levels of Quantum Resistance.

## Trust & Weight

Trust is defined as the total time a specific user (Signature Chain) has been contributing to the network. This time is measured by the consistency and availability of a node to validate transaction data.

Weight is defined as the real time resource contribution that a given node has provided for a one time transaction process. This can be measured in computing cycles through Proof-of-Work (PoW) or other resources such as ‘stake’ that incurs a cost to provide.

## pBFT + Reputation Channels (L1)

As transactions are received by the network, nodes start verifying them immediately. The transaction speed of L1 channels will vary based on the risk that a merchant wishes to assume, ranging from sub-second speeds to five seconds. For higher value transactions, it will be recommended that they receive additional weight from validation on the next consensus layer: L2, reducing transaction speed to 15 seconds plus.

## pBFT + PoS TRUST Network (L2)

As an extension to the existing Proof-of-Stake system, L2 will form the second layer of consensus above L1. The L2 layer ensures safety and liveness, cross-shard communication, and resolves conflicts from the L1 layer. It represents the horizontal chaining of L1 channels, and is a major step towards a truly decentralized and scalable ledger.

## Checking and Balancing

In order to have the highest degree of security, decisions cannot be concentrated in one form, as this creates the ability for ‘coercion’. If there is only one form of cost that provides security, the system can be easily dominated due to limited ‘checking and balancing’. Bitcoin is a prime example of a victim that is suffering from resource domination or ‘centralization’.

Four organizations control more than 51% of Bitcoin’s hashrate, meaning, that the entire security of Bitcoin is reliant on them and the decisions that they make. This situation is an example of centralization resulting from resource domination, which has lead to proposed solutions such as UASF (User Activated Soft Fork) and multiple Bitcoin forks such as Bitcoin Cash, Bitcoin SV, Bitcoin Gold, etc.

![graph](../../../.gitbook/assets/3dcgraph)

Though promising, UASF was unable to reach a level where it could be effective, as the required percentage of miner’s consent was too high.

## Decentralization

Many protocols have moved away from PoW due its large energy requirements. The extremely competitive nature also leads to an increasing amount of resources in order to search for a block, as the traditional model of PoW only rewards the winning miner of each block, incentivizing miners to pool resources.

Delegated Proof of Stake (DPoS), a consensus mechanism used by EOS, TRON, LISK and others primarily to achieve scaling enhancements, relies on a limited number of select block producers, yields a low degree of decentralization. There are several solutions that have been proposed for the scaling of a blockchain: Bitcoin’s Segregated Witness combined with Lightning Network, and Ethereum’s Plasma for example. Though promising, both essentially depend on off-chain solutions to provide scaling (a more centralized approach). They create payment channels or ‘side chains’, that rely on a small group of verifiers to recommit updated balances. Younger protocols have proposed multilayered systems, though we are unaware of any designs that place as much emphasis on decentralization as the 3DC.

The 3DC aims to achieve decentralization through many methods that include; L1 reputation channels, decentralized pools on the L2 and L3 layers, reputation incentive structures, and peer discovery.

## L1 Reputation Channels

L1 Reputation channels are designed to require a low amount of resources in comparison to the L2 and L3 layers. This is to enable the use of smaller mobile devices which in turn will provide higher levels of decentralization. This is possible as the L2 consensus layer above adds weight to ensure the security of the channels below. Reputation is the final ingredient that the 3DC employs to maintain security while achieving high levels of decentralization. It is aggregated through all three layers of the 3DC, to quantify the ‘validity’ of the 3D block.

## Decentralized Staking Pools (L2)

The L2 layer is the core of the 3DC that manages data aggregation and contract processing. This layer also receives shares from the miners on the L3 layer above, in order to accumulate their work and reward the miners collectively. The more shares that are included from the L3 layer, the greater the accumulated weight and trust will be for the given 3D block. Therefore, the 3DC incentivises L2 validators to include as many shares as possible to ensure that their 3D block is accepted as the most valid in the 3D chain.

The L2 layer is driven by a ‘Proof-of-Stake’ weighting, that identifies all nodes in the consensus process as contributors, and therefore produces a higher degree of decentralization compared to existing Proof-of-Stake (PoS) protocols. The 3DC will require a lower minimum balance in order to stake with than the current PoS protocol.

## Decentralized Mining Pools (L3)

This layer will use PoW based mining shares computed from the work performed by the nodes of L2. Consensus will be determined by the largest value of shares + Trust, in order to reach a final agreement on the most valid 3D block.

Instead of miners having the authority to determine the next block by finding the winning hash, mining will become a group-wide activity forming the L3 layer of the 3DC. Miners who submit hashes to the network perform work that locks the L2 cross links. This provides the infrastructure for a more decentralized consensus process, while also inheriting the positive properties that mining offers.

## Peer Discovery

Blockchains typically rely on the ability of nodes to connect directly (peer-to-peer) to maintain a decentralized and evenly distributed topology. Nodes must be discoverable by their peers, by being able to accept connection requests. This is seldom achieved, and has resulted in Bitcoin only having a meager 10% of nodes that are discoverable.

Alternatively, Nexus uses the [LISP](broken-reference) Overlay in order to traverse ‘NATs’ (Network Address Translators) to maintain a higher degree of node availability. LISP uses static Endpoint Identifiers (EIDs) that can even be reached when roaming between different networks (WiFi, cell towers, etc.). This gives nodes significantly increased mobility, allowing them to be located anywhere on the internet, behind NATs in residential environments, in cloud providers, and behind mobile carriers while still being discoverable.

## Reputation Incentive Structure

Reputation is an important requirement for the functioning of decentralized systems, in order to create a healthy global network. We will implement reputation on all three layers of the 3DC, as a secondary component to weight, improving the overall pBFT. Of equal importance, reputation can improve the decentralization through incentive structures facilitated through variable rewards to nodes that have earned a higher reputation. Longer term contributors to a system can be awarded a higher reputation, and therefore a higher return for their contribution, giving rise to a long standing view of Nexus that:

_Not everyone has money, but everyone has time_
