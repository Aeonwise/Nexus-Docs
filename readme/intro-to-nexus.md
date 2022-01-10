# Intro to Nexus

## WHAT IS NEXUS?

In the Nexus universe, there is a single, canonical computer (called the Nexus Virtual Machine, or NVM) whose state everyone on the Nexus network agrees on. Everyone who participates in the Nexus network (every Nexus node) keeps a copy of the state of this computer. Additionally, any participant can broadcast a request for this computer to perform arbitrary computation. Whenever such a request is broadcast, other participants on the network verify, validate, and carry out ("execute") the computation. This execution causes a state change in the NVM, which is committed and propagated throughout the entire network.

Requests for computation are called transaction requests; the record of all transactions and the NVM's present state gets stored on the blockchain, which in turn is stored and agreed upon by all nodes.

Cryptographic mechanisms ensure that once transactions are verified as valid and added to the blockchain, they can't be tampered with later. The same mechanisms also ensure that all transactions are signed and executed with appropriate "permissions" (no one should be able to send digital assets from John's account, except for John).

### WHAT IS NXS? <a href="#what-is-ether" id="what-is-ether"></a>

**Nexus (NXS)** is the native cryptocurrency of Nexus. The purpose of NXS is to allow for a market for computation. Such a market provides an economic incentive for participants to verify and execute transaction requests and provide computational resources to the network.

Any participant who broadcasts a contract execution request must also offer some amount of NXS to the network as a bounty. This bounty will be awarded to whoever eventually does the work of verifying the transaction, executing it, committing it to the blockchain, and broadcasting it to the network.

<mark style="color:green;">The amount of NXS paid corresponds to the time required to do the computation. These bounties also prevent malicious participants from intentionally clogging the network by requesting the execution of infinite computation or other resource-intensive scripts, as these participants must pay for computation time.</mark>

### WHAT ARE ADVANCED  CONTRACTS? <a href="#what-are-smart-contracts" id="what-are-smart-contracts"></a>

<mark style="color:green;">In practice, participants don't write new code every time they want to request a computation on the EVM. Rather, application developers upload programs (reusable snippets of code) into EVM storage, and users make requests to execute these code snippets with varying parameters. We call the programs uploaded to and executed by the network smart contracts.</mark>

<mark style="color:green;">At a very basic level, you can think of a smart contract like a sort of vending machine: a script that, when called with certain parameters, performs some actions or computation if certain conditions are satisfied. For example, a simple vendor smart contract could create and assign ownership of a digital asset if the caller sends ether to a specific recipient.</mark>

<mark style="color:green;">Any developer can create a smart contract and make it public to the network, using the blockchain as its data layer, for a fee paid to the network. Any user can then call the smart contract to execute its code, again for a fee paid to the network.</mark>

<mark style="color:green;">Thus, with smart contracts, developers can build and deploy arbitrarily complex user-facing apps and services such as: marketplaces, financial instruments, games, etc.</mark>

### TERMINOLOGY <a href="#terminology" id="terminology"></a>

### &#x20;<a href="#blockchain" id="blockchain"></a>

\
