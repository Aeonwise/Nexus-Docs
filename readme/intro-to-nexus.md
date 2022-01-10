# Intro to Nexus

## WHAT IS NEXUS?

In the Nexus universe, there is a single, canonical computer (called the Nexus Virtual Machine, or NVM) whose state everyone on the Nexus network agrees on. Everyone who participates in the Nexus network (every Nexus node) keeps a copy of the state of this computer. Additionally, any participant can broadcast a request for this computer to perform arbitrary computation. Whenever such a request is broadcast, other participants on the network verify, validate, and carry out ("execute") the computation. This execution causes a state change in the NVM, which is committed and propagated throughout the entire network.

Requests for computation are called transaction requests; the record of all transactions and the NVM's present state gets stored on the blockchain, which in turn is stored and agreed upon by all nodes.

Cryptographic mechanisms ensure that once transactions are verified as valid and added to the blockchain, they can't be tampered with later. The same mechanisms also ensure that all transactions are signed and executed with appropriate "permissions" (no one should be able to send digital assets from Alice's account, except for Alice herself).

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

### Blockchain <a href="#blockchain" id="blockchain"></a>

The sequence of all blocks that have been committed to the Nexus network in the history of the network. So-named because each block contains a reference to the previous block, which helps us maintain an ordering over all blocks (and thus over the precise history).

### NXS <a href="#eth" id="eth"></a>

The native cryptocurrency of Nexus. Users pay NXS to other users to have their contract execution requests fulfilled.

### EVM <a href="#evm" id="evm"></a>

The Nexus Virtual Machine is the global virtual computer whose state every participant node on the Nexus network stores and agrees on. Any participant can request the execution of contracts on the NVM; contract execution changes the state of the NVM.

### Nodes <a href="#nodes" id="nodes"></a>

The computers which are storing the NVM state. Nodes communicate with each other to propagate information about the NVM state and new state changes. Any user can also request the execution of transactions by broadcasting a contract execution request from a node. The Nexus network itself is the aggregate of all Nexus nodes and their communications.

[More on nodes](https://ethereum.org/en/developers/docs/nodes-and-clients/)

### User account or Signature chain <a href="#accounts" id="accounts"></a>

A unique  user-space on the Nexus network for every user, which records the users account balances, assets and state.

### Accounts

Where NXS and tokens is stored. Users can initialize accounts, deposit NXS into the accounts, and transfer NXS from their accounts to other users. Accounts and account balances are stored in the register layer in the NVM; they are a part of the overall NVM state.

[More on accounts](https://ethereum.org/en/developers/docs/accounts/)

### Transactions <a href="#transactions" id="transactions"></a>

A "transaction request" is the formal term for a request for contract execution on the NVM, and a "transaction" is a fulfilled transaction request and the associated change in the NVM state. Any user can broadcast a transaction request to the network from a node. For the transaction request to affect the agreed-upon NVM state, it must be validated, executed, and "committed to the network" by another node. Execution of any code causes a state change in the NVM; upon commitment, this state change is broadcast to all nodes in the network. Some examples of transactions:

* Send 10 NXS from my account to John's account.
* <mark style="color:green;">Publish some smart contract code into EVM memory.</mark>
* <mark style="color:green;">Execute the code of the smart contract at address X in the EVM, with arguments Y.</mark>

[More on transactions](https://ethereum.org/en/developers/docs/transactions/)

### Blocks <a href="#blocks" id="blocks"></a>

The volume of transactions is very high, so transactions are "committed" in batches, or blocks. Blocks generally contain dozens to hundreds of transactions.

[More on blocks](https://ethereum.org/en/developers/docs/blocks/)

### Smart contracts <a href="#smart-contracts" id="smart-contracts"></a>

A reusable snippet of code (a program) which a developer publishes into EVM memory. Anyone can request that the smart contract code be executed by making a transaction request. Because developers can write arbitrary executable applications into the EVM (games, marketplaces, financial instruments, etc.) by publishing smart contracts, these are often also called [dapps, or Decentralized Apps](https://ethereum.org/en/developers/docs/dapps/).

[More on smart contracts](https://ethereum.org/en/developers/docs/smart-contracts/)

\
