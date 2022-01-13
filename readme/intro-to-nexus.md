---
description: Introduction to Nexus
---

# Intro to Nexus

## WHAT IS NEXUS?

Nexus is a network of computers which run the core (a software implementation of Nexus protocols) and communicate via the internet to form a single _`authorised`_ supercomputer called the Nexus Virtual Machine (NVM). The NVM is a _`state machine`_ and all the participants agree and keep a copy of the state. Any user can request for a transaction on the network and when such a  request is broadcast, other participants on the network verify, validate and carry out (`execute")` the request. This execution causes a state change in the NVM, which is then committed and propagated throughout the entire network.

Requests for contract execution is called transaction requests; the record of all transactions and the NVM's present state gets stored on the blockchain (`ledger`), which in turn is stored and agreed upon by all nodes.

Cryptographic mechanisms ensure that once transactions are verified as valid and added to the blockchain, they can't be tampered with later. The same mechanisms also ensure that all transactions are signed and executed with appropriate "permissions" (no one should be able to send digital assets from John's account, except for John).

### WHAT IS NXS? <a href="#what-is-ether" id="what-is-ether"></a>

**Nexus (NXS)** is the native cryptocurrency of Nexus cosmos. Nexus has free simple transactions. The purpose of NXS is to allow for proper gamification of the network. To ensure that the active participants are compensated for the work done and prevent malicious participants from intentionally clogging the network by requesting infinite micro transaction (spamming) and name squatting. Such a market provides an economic incentive for participants to verify and execute transaction requests and provide computational resources to the network.

Any participant who broadcasts a contract execution request must also offer some amount of NXS to the network as a bounty. This bounty will be awarded to whoever eventually does the work of verifying the transaction, executing it, committing it to the blockchain, and broadcasting it to the network.

<mark style="color:green;">The amount of NXS paid corresponds to the time required to do the computation. These bounties also prevent malicious participants from intentionally clogging the network by requesting the execution of infinite computation or other resource-intensive scripts, as these participants must pay for computation time.</mark>

{% embed url="https://nexus.io/roadmap" %}

### WHAT ARE ADVANCED  CONTRACTS? <a href="#what-are-smart-contracts" id="what-are-smart-contracts"></a>

The 7 layered software stack architecture plays the crucial role; with its operations and register layer which command and controls the NVM.&#x20;

Register layer is the data storage system that maintain an immutable record and history, including current and previous states, therefore they can be used to record the state of applications. The register layer is the data layer which mimics the CPU cache memory which is the fastest memory on a computer.&#x20;

Operation layer contains instructions or actions that give registers context, and define more complex contract logic. A contract is an object containing: a register pre-state (the register that is being operated on that was passed upwards from the Register Layer), a primitive operation (only one primitive operation per contract), and a set of conditions (any amount of conditional operations)

At a more basic level, Advanced Contracts are comparable to real world contracts, written on paper and enforced by a court of law. It's highly advanced as its enforced by code, its binding and it makes the trusted third parties redundant.

Advanced contracts, empower developers to build and deploy arbitrarily complex user-facing apps and services such as: P2P marketplaces,  decentralized financial instruments, games, etc.

\




<mark style="color:green;"></mark>

<mark style="color:green;"></mark>

<mark style="color:green;">In practice, participants don't write new code every time they want to request a computation on the EVM. Rather, application developers upload programs (reusable snippets of code) into EVM storage, and users make requests to execute these code snippets with varying parameters. We call the programs uploaded to and executed by the network smart contracts.</mark>

<mark style="color:green;">At a very basic level, you can think of a smart contract like a sort of vending machine: a script that, when called with certain parameters, performs some actions or computation if certain conditions are satisfied. For example, a simple vendor smart contract could create and assign ownership of a digital asset if the caller sends ether to a specific recipient.</mark>

<mark style="color:green;">Any developer can create a smart contract and make it public to the network, using the blockchain as its data layer, for a fee paid to the network. Any user can then call the smart contract to execute its code, again for a fee paid to the network.</mark>

<mark style="color:green;">Thus, with smart contracts, developers can build and deploy arbitrarily complex user-facing apps and services such as: marketplaces, financial instruments, games, etc.</mark>

\
