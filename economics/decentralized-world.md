# Decentralized World

### Blockchain 101

**How does a Blockchain work?**

People, known as miners, are given a monetary incentive to verify transactions. Miners use computers or specialized mining equipment to verify that the people spending cryptocurrency, indeed have the coins to spend. A record of transactions are then immutably chained together and recorded as a block, and appended to the chain. This record is stored on the computers of many different miners, creating a decentralized network.

Many blockchains use a mechanism called Proof-of-Work (PoW) exclusively that requires resource inputs such as hardware and electricity. Others use Proof-of-Stake (PoS) that requires less physical resources, however requires the miner to ‘wager’ some coins. Thus, there is an incentive to verify transactions correctly. To attempt a double-spend attack (to spend a cryptocurrency coin twice), a person would need 51% of the PoW and/or PoS power, which can be very costly to achieve. Therefore, the blockchain provides a trustworthy source of information, where all transactions are witnessed and verified by a global consensus rather than by a central trusted authority.

![](../.gitbook/assets/hash)

**What are the steps?**

1. A person sends a transaction from a wallet on their computer to the network (this transaction can be any piece of data).
2. Miners verify whether this transaction contains a valid digital signature and has no conflicts with others (double-spends). If the consensus agrees that the transaction is valid, then it is accepted into a memory pool to await confirmation.
3. This transaction is then grouped with other transactions from other people at a similar time interval (usually 1-10 minutes) into what is termed a ‘block’, which is then given a digital fingerprint through a process called ‘hashing’.
4. The block is a cryptographic structure that is unable to be altered, as the next block created includes the previous block’s hash, making it impossible to change the previous block without re-doing all the work.
5. Since the work required to change a previous block grows exponentially for every new block produced, at a certain depth (usually six blocks), it becomes computationally infeasible to rewrite, therefore the blockchain is considered immutable.
6. The chain with the most work from the first or ‘genesis’ block is considered the valid history of events and is known as the ‘main chain’. This is how a blockchain maintains consensus.

**What is Decentralization?**

![](<../.gitbook/assets/topologies (1)>)

The above diagram illustrates three different topologies. Centralized and Decentralized are concepts of authority, whereas distribution is a spatial concept, meaning it relates to the physical network topology. A network can be distributed, as well as being centralized or decentralized. An ideal network topology has a decentralized consensus process, with a distributed node topology.

A decentralized cryptocurrency network is a system of many different people using computers or mining hardware, called ‘nodes’ to verify transactions. This type of network is also known as a ‘peer-to-peer network’. None of the nodes or peers have a relative authority over any other. The higher the number of nodes, the more resilient the system is to outside attack or consensus manipulation. Therefore, the more people that contribute resources to a decentralized network, the more secure, resilient, and robust it becomes.

Many blockchains market themselves as decentralized technology. However, ICOs, Security Token Offerings (STO), venture capitalist backing, corporate partnerships, and authoritative consensus implementations, all create favourable conditions for centralization.

Likewise, challenges faced by the original blockchain protocol have also led to cryptocurrencies creating ‘off chain solutions’ that require central nodes or servers. This essentially gives control back to a third-party. Similarly, blockchains that have developed ‘Delegated Proof-of-Stake’ (DPoS) consensus mechanisms have also become more centralized.

Satoshi Nakamoto combined the architectures of B-Money and HashCash to create a peer-to-peer network in order to build a distributed ledger (a record of transactions), known as a Blockchain.

Bitcoin uses the PoW consensus, which was originally envisioned to be a decentralized system. However, the high energy costs and expensive hardware necessary to compete when mining Bitcoin, has led to the centralisation of the protocol via the formation of a few powerful mining pools. Therefore, only a small number of influential people control the future direction of Bitcoin.

[Blockstream’s](https://bitcoinexchangeguide.com/why-did-blockstream-become-a-bitcoin-focal-point-at-the-core-of-btc-vs-bch-consensus-split/) influence over Bitcoin is perhaps the best example of how centralization can destroy the integrity of a system. Blockstream agreed to increase the block size to 2MB in return for community support in activating Segregated Witness (a prerequisite to the Lightning Network). Ultimately, this decision resulted in the division of Bitcoin and Bitcoin Cash, due to a violation of the ‘[Segwit2x](https://www.coindesk.com/explainer-what-is-segwit2x-and-what-does-it-mean-for-bitcoin)’ agreement. Not surprisingly, once Segwit was activated, Blockstream dropped their side of the agreement, and refused to increase the block size to 2 MB.

One of the fundamental reasons behind the creation of Bitcoin (BTC), is to protect against the irresponsible creation of currency (inflation), by use of consensus-based and mathematical regulation. Bitcoin’s final supply will reach 20999999.9769 BTC, or approximately 21,000,000 by the year 2140, as outlined here. Currently, Bitcoin miners are paid partly by inflation (a fixed amount of BTC is available as a reward for miners in every block) and partly by transaction fees. However, every four years the inflation of BTC reduces by 50%, this is known as the ‘halving’ event, which occurs every four years. This makes the model of BTC deflationary, and the viability of BTC mining inherently dependent on an ever increasing price, that post 2140 relies solely on transaction fees to maintain network security.

Often proponents of Bitcoin will tell you that Bitcoin is becoming more scarce (as if it had a diminishing supply, which it does not) and therefore it is becoming more valuable. All ‘BTC halvings’ are predictable events, rather than unexpected shocks in supply.

Bitcoin may serve well as a store of value or a commodity, such as gold. However, how well will it function as a currency over time? An important question for new buyers to ask is: is a deflationary model an ideal choice for a functional currency? At the moment, many countries have negative interest rates (paying people to take loans) to try to incentivise them to spend and not hoard. Some economists would argue that there is a healthy level of inflation or ‘sweet spot’ that drives innovation, as entrepreneurs are unlikely to borrow money for investments if overall prices are falling.

Read about Nexus Economics here.

Currentlty, a Proof-of-Work (PoW) coin exclusively, ETH accomplished a pre-mine, Initial Coin Offering (ICO), and suffered major controversy by reversing transactions relating to a Decentralized Autonomous Organization (DAO) attack. This situation also resulted in a divisive conclusion with a fork that led to the creation of Ethereum Classic without the blockchain reversal.

Additionally, they have numerous influential financial backers with the Ethereum Alliance Board Members and several third party solutions seeking to capitalize on the scalability crux and potentially governance decisions.

Despite all of the decentralization detractors and unreasonable costs, they have managed to enable one of the first blockchain deployments of citizen identity for Zug, Switzerland. Considering their previous actions, there is a high probability of tampering with the data-set to freeze, revoke or even sell your identity data based on health policy infraction, or other violation deemed necessary by the influencers.

Today’s societies are organized by centralized databases, with a ‘trusted’ authority in the form of governments, institutions and third parties. Trusted authorities authenticate and process information of these databases in order to determine ownership, legal agreements, and to settle disputes. Centralized databases have provided many useful technologies including government ledgers (e.g. titles and deeds, voting rolls, licenses, customs records, and digital I.Ds), and corporate ledgers (e.g. bank deposits, and stock wealth). Though these databases provide many benefits to society as a whole, they often result in the selling of data to other organizations without the consent of the people.

Other notable issues with centralized databases are the rising number of data breach cases, that at times have affected millions of people. Blockchain can improve database security as there is no central authorization point to hack. Essentially, a decentralized system is difficult to compromise as there is no central point of failure.

The implementation of the world’s monetary systems, some of the oldest centralized systems of today, have become the source of one of today’s biggest challenges. This is due to the many global policies designed to create Fiat currency ($, £, €) out of debt, which is paid back with interest to central reserve banks.

There are many instances of central banks who have misused this enormous power, knowingly or unknowingly, resulting in hyperinflation. Hyperinflation is the rapid increase of prices, and is a result of excessive money creation. When more and more money is released, the money drives up the prices of goods, resulting in the reduction of the purchasing power of the currency.

In post-World War I Germany, hyperinflation reached 30,000% per month (the price of goods doubled every two days), during the Great Recession in Zimbabwe, hyperinflation reached 79,600,000,000% per month (the price of goods doubled every 24.7 hours), and in post-World War II Hungary, hyperinflation reached 41,900,000,000,000,000% per month (the price of goods doubled every 15.6 hours).

It is often thought that banks lend out the deposits of savers. However, banks do not simply act as middlemen or intermediaries between savers and borrowers. Banks are the creators of money (bank notes and digital deposits) also known as Fiat currency. Central Banks create money by issuing loans and by purchasing government bonds.

However, bank lending is only backed by a small fraction of deposits, by a process called ‘Fractional Reserve Banking’. Thus, savers’ deposits only account for a fraction of lending, which always results in the production of new debt that ultimately is required to be paid back to the central bank with interest.

Together, banks only hold approximately 10% of the entire money supply that exists, as actual reserves. The other 90%, called ‘Bank Credits’, is synonymous with an IOU. Consequently, if people began to withdraw their deposits all at once, known as a ‘run on the banks’, the banks would only be able to honour 10% of withdrawals.

Today’s debt-based monetary system is structured in a way that the creation of money also encourages cycles of boom and bust, increasing wealth inequality, resulting in an ever increasing amount of money and resources being transferred to a few people. In contrast, the Nexus Economic Model rewards NXS to stakers and miners, and is designed to create a more equal distribution of NXS to the community, whilst mitigating the possibility of unhealthy levels of inflation.

Read about Nexus Economics here.

Due to its scarcity, gold is an asset which has often been favored in times of economic crisis as a hedge against the inflation of fiat currencies. One of the reasons we as a global economy moved away from the use of physical gold as a currency, is that it was very hard to divide and difficult to move between banks to settle merchant’s balances.

In 14th century Italy, people began to accept paper IOUs backed by reputable merchants. A similar system developed later in 17th century England, where goldsmiths (who held merchant’s gold in vaults for them) realized that the merchants didn’t redeem all their IOUs at any one time. Thus, the goldsmiths began to lend out paper certificates to people. However, they didn’t hold enough gold to back every paper certificate in circulation, they only held a fraction of it. This was the beginning of Fractional Reserve Banking.

Some people are now buying gold and other precious metals as an inflation hedge, though unless you hold the metals yourself, you have to ‘trust’ a third party to store the gold for you. Trusting of any third parties is what decentralized cryptocurrencies or blockchain technology are designed to replace.

Some governments have created or are creating gold-backed currencies. People who opt to use these currencies will have to trust that the governments do indeed hold sufficient gold in reserve, and are not simply continuing the tradition of Fractional Reserve Banking.

Read about Nexus Economics here.

Classical computing uses an array of transistors. These transistors form the heart of your computer (the CPU). Each transistor is capable of being either on or off, and these states are used to represent the numerical values 1 and 0. Binary digits’ (bits) number of states depends on the number of transistors available, according to the formula (2^n) + 1, with n being the number of transistors. Classical computers can only be in one of these states at any one time, so the speed of your computer is limited to how fast it can change state.

Quantum computers on the other hand, use what are termed quantum bits or ‘qubits’ which are represented by the quantum spin of electrons or photons. These particles are placed into a state called superposition, allowing the qubit to assume a value of 1 and 0 simultaneously, generally resulting in an exponential increase in computational power over their classical counterparts.

With the rise in the power of classical computers and the emergence of quantum computers, public keys are becoming increasingly vulnerable. Most cryptocurrency addresses are created by hashing or obscuring the public key, however, once a user transfers funds from this address, the public key is then revealed on the blockchain. In the realm of classical computing there is little risk with this method. However, a Quantum Computer running Shor’s algorithm could break most public key cryptography in little to no time at all, resultingin funds being stolen.Though most conjectures range from five to ten years before security could begin to break, Nexus has prepared by integrating a number of cryptographic innovations that support increased levels of quantum resistance.

Learn more about Nexus' Quantum Resistance here.

Today the Internet relies on both large cables that run across the ocean floor, and geosynchronous satellites. The main drawbacks resulting from the state of the current Internet infrastructure are as follows:

* 4 billion people are without Internet connection.
* Unreliability in some areas due to natural disasters.
* Intercontinental cables and geosynchronous satellites cost millions of dollars to build, deploy and maintain, and are therefore owned and managed by governments and large corporations.
* ‘Command and Control’ operation and telemetry systems rely on centralized organizations for satellite management.
* ISPs usually have a monopoly over a particular service area, leading to higher service fees and lack of incentive for quality.
* Increased c ensorship and the ‘throttling’ of information due to lack of ‘Net Neutrality’.

Learn more about Nexus' Decentralized Internet plan here.
