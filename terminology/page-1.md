# Page 1

### Blockchain <a href="#blockchain" id="blockchain"></a>

On the Nexus network transactions are verified and written in batches of approximately 50sec. This creates a sequence of all blocks that have been committed to the Nexus network in the history of the network and each block contains a reference to the previous block to maintain an ordering over all blocks. This looks like blocks chained together and thus the name _Blockchain_

Blockchain is a common name used to refer distributed ledger systems

### Nexus Network

It is the network of computers which run the Nexus core implementation and communicate via the internet to form the network which power the Nexus ecosystem. All computers on this network store the distributed ledger

### Nexus <a href="#eth" id="eth"></a>

The native cryptocurrency of the Nexus cosmos, used to pay for various operations on the network, like contract execution, creating tokens, assets etc. This is the only accepted form of payment on the network.

### NXS

The ticker symbol for the Nexus cryptocurrency.&#x20;

### CORE <a href="#evm" id="evm"></a>

Core is the software implementation of protocols, which powers the Nexus network and protocols. Community members run the core on the computer and the software detects peers and runs like a single entity communicating via the intenet which is the backbone of the Nexus network&#x20;

### NVM <a href="#evm" id="evm"></a>

The Nexus Virtual Machine (NVM) is the global virtual computer whose state every participant node on the Nexus network stores and agrees on. Any participant can request the execution of contracts on the NVM; contract execution changes the state of the NVM.

### NODE <a href="#nodes" id="nodes"></a>

Node is a computer which run the Nexus core, is connected to other computers running the Nexus core via the internet to form the Nexus network. Nodes store the NVM state, communicate with each other and propagate information about the NVM state and new state changes. Any participant can request the execution of transactions by broadcasting request from a node

### SIGNATURE CHAINS / USER ACCOUNTS <a href="#accounts" id="accounts"></a>

A unique user space for users on the Nexus network; records the account balances, assets and state. User's access their user account using username, password and PIN similar to email. The user account also serves as a native secure digital identity.&#x20;

### Accounts

Where NXS and tokens is stored. Users can initialize accounts, deposit NXS into the accounts, and transfer NXS from their accounts to other users. Accounts and account balances are stored in the register layer in the NVM; they are a part of the overall NVM state.

### Transactions <a href="#transactions" id="transactions"></a>

A "transaction request" is the formal term for a request for contract execution on the NVM, and a "transaction" is a fulfilled transaction request and the associated change in the NVM state. Any user can broadcast a transaction request to the network from a node. For the transaction request to affect the agreed-upon NVM state, it must be validated, executed, and "committed to the network" by another node. Execution of any code causes a state change in the NVM; upon commitment, this state change is broadcast to all nodes in the network. Some examples of transactions:

* Send 10 NXS from my account to John's account.
* Create an Asset and tokenize it.
* Create an invoice.

### Blocks <a href="#blocks" id="blocks"></a>

The volume of transactions is very high, so transactions are "committed" in batches, or blocks. Blocks generally contain dozens to hundreds of transactions.

### Smart contracts <a href="#smart-contracts" id="smart-contracts"></a>

Any user  can request a contract execution by making a transaction request. Because developers can write arbitrary executable applications into the NVM (games, marketplaces, financial instruments, etc.) by publishing smart contracts, these are often also called dapps or Decentralized Apps

### TAO NAMING SYSTEM (TNS)

TNS is the native naming or domain name available on Nexus network
