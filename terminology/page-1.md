# Page 1

### Blockchain <a href="#blockchain" id="blockchain"></a>

The sequence of all blocks that have been committed to the Nexus network in the history of the network. So-named because each block contains a reference to the previous block, which helps us maintain an ordering over all blocks (and thus over the precise history).

### NXS <a href="#eth" id="eth"></a>

The native cryptocurrency of Nexus. Users pay NXS to other users to have their contract execution requests fulfilled.

### NVM <a href="#evm" id="evm"></a>

The Nexus Virtual Machine (NVM) is the global virtual computer whose state every participant node on the Nexus network stores and agrees on. Any participant can request the execution of contracts on the NVM; contract execution changes the state of the NVM.

### Nodes <a href="#nodes" id="nodes"></a>

The computers which are storing the NVM state. Nodes communicate with each other to propagate information about the NVM state and new state changes. Any user can also request the execution of transactions by broadcasting a contract execution request from a node. The Nexus network itself is the aggregate of all Nexus nodes and their communications.

[More on nodes](https://ethereum.org/en/developers/docs/nodes-and-clients/)

### User account or Signature chain <a href="#accounts" id="accounts"></a>

A unique user space for users on the Nexus network; records the account balances, assets and state. User's access their user account using username, password and PIN similar to email. The user account also serves as a native secure digital identity.&#x20;

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
