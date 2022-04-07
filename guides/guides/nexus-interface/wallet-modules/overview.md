---
description: Overview Module
---

# Overview

The "`Overview` module is the homepage of the wallet. The purpose of the globe is to show the location of nodes the wallet is connected to.

### Below is an explanation of the attributes on the left hand side of the Overview module:

* **Balance (NXS):** Total NXS balance across all accounts in the signature chain.
* **Balance (USD):** The USD value of all NXS balances - calculated by multiplying _Balance (NXS) x Market Price (USD)_. The wallet comes with USD as the default currency. The base currency can be changed at the following location: _Settings -> Application -> Base Currency._
* **Incoming Balances (NXS):** This value shows the value of NXS that is coming into the wallet and has not yet been confirmed and fully received.
* **Market Price (USD):** The value of 1 NXS in the chosen default base currency (in this case USD).
* **Market Cap (USD):** This is calculated by multiplying the _Market Price (USD) x Total NXS Circulating Supply._
* **24HR Change (USD %):** The market value change in NXS over the last 24 hours.



### Following is an explanation of the attributes on the right hand side of the Overview module:

* **Connections:** This refers to the amount of random “nodes” which are connected. By default your node is limited to make up to 16 outgoing connections and 84 incoming (100 total). If you are behind a router at home then incoming connections will only be able to be made if you enable UPnP in the wallet (and your router supports it) or if you manually set up port forwarding on port 9888. You can change the configuration to have more than 16 outgoing (with maxoutgoing=xx) but it's not necessary, 16 is adequate.
* **Block Count:** The block count is the “height” of the blockchain. This number reflects the local node block count that can be verified against a Nexus Explorer’s current block height (meaning the wallet is up-to-date). If the block value on the wallet does not match that of a Nexus Explorer, then it is not in sync with the public blockchain. Use the ‘Download the Recent Database’ option (File -> Download Recent Database) to bootstrap the most recent version. Another method to validate synchronization is to look at the left icon in the top right-hand corner of the wallet. If it says “Synchronizing,” that means it is not up to date. On the other hand, if it says “Synchronized,” that means it is up to date.
* **Stake Rate:** This value represents the current rate used to calculate the reward for mining a Proof of Stake block, stated in the form of an annual NXS rate of return (%). The rate starts at 0.5%, and can increase to 3.0% after 12 months of continual staking.
* **Block Weight:** Upon receipt of a genesis transaction, this value will begin increasing slowly, reaching 100% in 3 days time. Every time you receive a staking transaction, the block weight resets.
* **Trust Weight:** An indication of how much the network trusts the node. It starts at 1.11% and increases in a nonlinear manner like stake rate does. The level of trust increases the stake weight (below), thus increasing overall chances of miningblocks and receiving staking rewards. It becomes easier to maintain trust as this value increases.
* **Stake Weight:** The higher a wallet’s stake weight, the greater chances of receiving a trust transaction. The exact value is derived from the trust weight and block weight.



To read more about staking terms, please refer to the [FAQs & GLOSSARY](https://nexus.io/ResourceHub/general-FAQ).
