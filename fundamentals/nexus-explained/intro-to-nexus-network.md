---
description: Introduction to Nexus
---

# Intro to Nexus Network

## WHAT IS NEXUS NETWORK?

It is a network of computers which run the core (a software implementation of Nexus blockchain protocols) and communicates via the internet to form a single _**`canonical`**_ supercomputer called the Nexus Virtual Machine (NVM). The NVM is a _**`state machine`**_ and all the participants agree and keep a copy of the state. Any user can request for a transaction on the network and when such a  request is broadcast, other participants on the network verify, validate and carry out _(**`execute)`**_ the request. This execution causes a state change in the NVM, which is then committed and propagated throughout the entire network.

Requests for contract execution is called transaction requests; the record of all transactions and the NVM's present state gets stored on the blockchain (`ledger`), which in turn is stored and agreed upon by all nodes.

Cryptographic mechanisms ensure that once transactions are verified as valid and added to the blockchain, they can't be tampered with later. The same mechanisms also ensure that all transactions are signed and executed with appropriate "permissions" (no one should be able to log into John's account, except for John, who has the signature chain credentials).

### WHAT IS NEXUS? <a href="#what-is-ether" id="what-is-ether"></a>

**Nexus (NXS)** is the native cryptocurrency of the Nexus cosmos. Nexus has been designed for free simple transactions. The purpose of NXS is to allow for proper gamification of the network. To ensure that the active participants are compensated for the work done and prevent malicious participants from intentionally clogging the network by requesting infinite micro transactions (spamming) and name squatting. NXS is the ticker symbol of Nexus.

### WHAT ARE ADVANCED  CONTRACTS? <a href="#what-are-smart-contracts" id="what-are-smart-contracts"></a>

The 7-layered software stack architecture plays the crucial role; with its operations and register layer which command and controls the NVM.&#x20;

Register layer is the data storage system that maintains an immutable record and history, including current and previous states, therefore they can be used to record the state of applications. The register layer is the data layer which mimics the CPU cache memory which is the fastest memory on a computer.&#x20;

Operation layer contains instructions or actions that give registers context, and define more complex contract logic. A contract is an object containing: a register pre-state (the register that is being operated on that was passed upwards from the Register Layer), a primitive operation (only one primitive operation per contract), and a set of conditions (any amount of conditional operations).

At a more basic level, Advanced Contracts are comparable to real world contracts, written on paper and enforced by a court of law. It's highly advanced as its enforced by code, its binding and it makes the trusted third parties redundant.

Advanced contracts, empower developers to build and deploy arbitrarily complex user-facing apps and services such as: P2P marketplaces, decentralized financial instruments, games, etc.
