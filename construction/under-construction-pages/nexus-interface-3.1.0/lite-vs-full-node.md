---
description: All the information about Lite and Full Nodes
---

# Lite Vs Full Node

The Interface version 3.1.0 and above will be powered by the updated Tritium++ core. The first update version 5.1 has a host of upgrades, changes to the core and Interface. The most notable among them is the desktop lite mode. Before this every desktop user had to run the full node, which comes with the complete database of the Nexus chain. The Lite node database is approximately  300MB in size and this will greatly increase adoption.

The lite mode database will contain only the block headers and sig chain details of the user. This greatly reduces the complexity and disk space requirements for users. This will also have the wallets synchronising within a couple of minutes, but this is dependent on the internet speed also.&#x20;

### Difference Between Node and Mode:

**Nodes:** are computers which run the **`core`** which is an implementation of the Nexus blockchain protocols. A node can run the **`Lite`** or the **`Full`** database. A node running a lite database is called a lite node.

**`Mode:`** is used to classify if a node uses the lite or the full database. A node which runs the lite database is said to be using the Lite mode.

## Which Mode to Use?

We recommend everyone to use the Lite mode except for stakers, miners, dapp backends, seed nodes and for the community members, who want to secure the network. Users who want to interact with the legacy chain will also have to run the full node. The Lite mode will not support the legacy chain. Stakers, miners, dapp backend and full seed nodes will have to opt for the full node option only. &#x20;

{% hint style="info" %}
Staking and mining will only be possible with the full node. Dapp backend nodes will also have to use the full node option. Legacy chain users can only transact using full node.
{% endhint %}



## How to change between Lite and Full Mode

At first start the user will get a popup asking if he wants to run the Interface in the Lite mode and make it the default setting. If the user selects the Lite mode, it will clear the old database in the core data folder and download the lite database.





The user can manually change between the two modes, for that the user has to click on the Settings module at the bottom of the Overview page. Under Settings, click on the core tab and under Embedded core the first option with a toggle button is for enabling /disabling the Lite mode

![Manual Lite mode settings](<../../../.gitbook/assets/LIte Mode.png>)

