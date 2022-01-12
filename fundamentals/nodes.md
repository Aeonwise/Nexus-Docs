# Nodes

Nexus is a distributed network of computers running software (known as nodes) that can verify blocks and transaction data. You need an application, known as core, on your computer to "run" a node.

## WHAT ARE NODES AND CORE?

## NODE TYPES

The Nexus core can be configured to run as different types of nodes that consume data differently. The Nexus core can run two different types of nodes - full and light.&#x20;

### Full Node

* Stores full blockchain data.
* Participates in block validation, verifies all blocks and states.
* All states can be derived from a full node.
* Serves the network and provides data on request.

### Lite Node

* Stores the block headers and sig chain data and requests everything else.
* Can verify the validity of the data against the state roots in the block headers.
* Useful for low capacity devices, such as embedded devices, IoT and mobile phones, which can't afford to store gigabytes of blockchain data.

## CORE <a href="#evm" id="evm"></a>

Core is the software implementation of the Nexus protocols which power the Nexus network. Network participants run the core on the computer which connects and communicates to other computers running the core via the intenet to form a single entity which is the Nexus network&#x20;

\
