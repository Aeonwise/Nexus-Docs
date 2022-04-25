---
description: Consensus on Nexus
---

# Consensus on Nexus

### What is consensus?

A blockchain, or distributed ledger, is spread across nodes whose job it is to verify transactions on the network. This is one of the key ideas about blockchain, and gives it its unique decentralized flavor.

As a result, anyone can submit information to be stored onto a blockchain and therefore it is important that there are processes in place that can ensure everyone agrees on what information to add and what to discard. These rules are essentially known as consensus protocols. They verify transactions and help keep the network safe.&#x20;

### How do Consensus Protocols work?

The consensus protocol at the heart of a blockchain network gives a specific method for verifying whether a transaction is true or not. It provides a method of review and confirmation of what data should be added to a blockchain's record. Because blockchain networks typically don't have a centralized authority dictating who is right or wrong, nodes on a blockchain all must agree on the state of the network, following the predefined rules, or protocol.

For Bitcoin, the consensus protocol is Proof-of work (PoW), the block mining process which confirms each transaction. Other types of consensus protocol include Proof-of-Stake (PoS) and Proof-of-Authority (PoA).

## What do consensus protocols do?

### **Prevent a single entity taking control**

If a network has consensus then all participating nodes agree on the state of a blockchain. Thus, data is recorded as the “truth” and the blockchain is able to function with more and more data added as transactions take place or smart contracts are executed.

Allows users on a decentralized to trust users without a controlling third-party.&#x20;

A consensus protocol prevents a single entity from controlling a blockchain or distorting the “truth” of what should be recorded.

Double spending is an example of what could happen if one entity tried to take control of the entire network by creating its own version of the blockchain. For example, an attacker could spend some Bitcoin, then alter the block due to be recorded on the blockchain so it doesn’t show the spend. The attacker could broadcast their version of the blockchain, less the spend record. The attacker would have used some Bitcoin, but the coins would not be recorded as spent on the chain and could be spent again.

Bitcoin’s consensus protocol, PoW, prevents this from happening because when that version of the blockchain is compared to other versions held on other nodes, it will be slightly different from everyone else's, and that version will be rejected by the other nodes. &#x20;

### **What are some of the most common types of consensus protocol?**

**Proof-of-Work (PoW):** The first blockchain, Bitcoin, uses PoW. To validate transactions to the Bitcoin blockchain “miners,” who are the nodes solve cryptographic, or mathematical problems, using their computers. Miners who solve a problem and validate and enable a block record are rewarded with bitcoin.

**Proof-Of-Stake (PoS):**&#x20;

In PoS there are “forgers” instead of miners. These forgers stake an amount of cryptocurrency which allows them a chance, based on probability, to be a block validator. The successful forger receives the relevant block transaction fees as a reward. Staking their own cryptocurrency on a block provides a disincentive for a forger to try and trick the network as they'll lose the stake if they're proven to be incorrectly adding transactions to the network.&#x20;

**Delegated Proof-of-Stake (DPoS):**

This method functions in a similar way to PoS. But, instead of using probability, cryptocurrency holders are able to cast votes apportioned to their stake in order to appoint witnesses. These witnesses secure and validate the blockchain, they do not need their own cryptocurrency, but they do need votes.  This consensus protocol is more centralized than others. DPoS is used by BNB**,** BitShares, Steem, and EOS.

**Proof-of-Authority (PoA):**

Arguably more centralized again, PoA has predetermined block validators. New blocks on a blockchain are only created when the validators are in majority. The protocol is similar to PoS. The validators are publicly known and accountable for determining their role and eligibility for PoS validation. A newer blockchain, Elysian, uses PoA as well as some Ethereum testnets, or test blockchains.

## Nexus Consensus:

Unless you are brand new to crypto, you are likely aware of the ongoing debate between Proof of Work (PoW) and Proof of Stake (PoS) as to which is a better consensus mechanism for securing a blockchain. At Nexus, we see the benefits of both and believe diversity is a strength. This is why Nexus incorporates both, leveraging multiple consensus channels to secure the state of the ledger. By diversifying the nature of our consensus structure, we avoid dependence on any one mechanism, improving our overall security.

So what does this look like? Nexus consists of three channels, two PoW and one PoS. The first PoW channel utilizes a hashing algorithm (similar to many other blockchains) for its proof of work, while the prime channel employs an algorithm where miners are required to search for clusters of very large prime numbers, offering a unique variation of the PoW principle. Finally, the PoS channel adopts an energy efficient, simple function where the users’ mining “power” is determined by their staked balance and trust score.&#x20;

Why did Nexus choose to adopt a multifaceted consensus model? There are a number of advantages to this approach, but in short, it is more secure, more equitable, and provides a greater opportunity for us to adapt to future requirements. Maximalists will be quick to point out that for the time being, Bitcoin is the unquestionable king of blockchain security, and since it utilizes a PoW consensus model, many assume that means PoW is also the king of consensus. However, there are some [glaring concerns](https://hackernoon.com/proof-of-work-or-proof-of-waste-9c1710b7f025) with relying exclusively on PoW, without even including the common argument highlighting unsustainable energy consumption, as it will be rendered moot by breakthroughs in renewable energy.

Proof of Stake was first introduced by PeerCoin and quickly gained popularity among emerging blockchain platforms. Though heavily criticized by PoW maximalists, PoS consensus gained instant credibility when Ethereum, the second largest cryptocurrency by both market cap and network, announced plans to convert from a PoW to a PoS consensus model. However, PoS is not without flaws either and over the years has evolved into multiple variations, most notably, delegated PoS, but each variation has its own [pros and cons](https://coincodex.com/article/7142/what-is-proof-of-stake/).

Instead of being caught in the middle of the PoW vs PoS debate and hindered by either’s limitations, Nexus developers chose to implement both in order to benefit from the combined strengths, while simultaneously minimizing the flaws of each individual mechanism. In addition, Nexus implements reputation as a value, which is related to how much time a staker consistently contributes resources to the network. A mechanism called ‘[Trust](https://tech.nexus.io/trust)’ records past work to create a weighted reputation system, significantly improving overall security of the Nexus PoS (nPoS) channel,

The Nexus team is transforming these three separate consensus channels into one multi-layered processing system capable of computational data sharding. The Tritium Protocol is the first upgrade of the [Three-Dimensional Chain (3DC)](https://tech.nexus.io/3dc) which is being deployed through the[ TAO framework](https://tech.nexus.io/roadmap).
