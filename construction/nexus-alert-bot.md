---
description: Nexus Transactions Alert Bot
---

# Nexus Alert Bot

The `Nexus Alert Bot`,  a telegram bot which will list transactions on the Nexus blockchain above 1000 NXS or tokens. This bot was born from a community request to track network growth, how to value Nexus, total NXS on tritium chain vs NXS on exchanges, a way to counter or at-least be aware of pump and dumps. It is going to be a tough task to implement all these aspects in one go.

The alert bot is simple to understand, but might be confusing to some, this guide will help to understand the data provided in a better way.\
\
Nexus has the`Tritium` and `Legacy` chains, all exchanges use the Legacy chain and it is difficult to track the balance of legacy accounts and the best we can do is keep track of the transactions on the network.&#x20;

To better understand the data provided by the bot, we can segregate the transactions into:

* Tritium to Tritium Transactions
* Legacy to Tritium Transactions
* Tritium to Legacy Transactions

#### Tritium to Tritium Transactions:&#x20;

Any transaction on tritium is a _`debit`_ to the senders account and a _`credit`_ to the receivers account. This creates two transactions for a single transaction, but the bot  is designed to ignore the `debit` and show only the `credit,` as it's a single transaction and having two alerts will create more confusion.&#x20;

It is easy to distinguish as  the "`OPERATION`" field reads as `CREDIT` and the "`FOR`" field will read `DEBIT`, which implies it's a _`credit`_ contract for a corresponding _`debit`_. &#x20;

#### Legacy to Tritium Transactions

Legacy to tritium transactions are when a user withdraws NXS from the exchange into his Tritium account. This transaction will only list the `credit` to the Tritium account and can be easily recognised by checking the "`OPERATION`" field which should read `CREDIT` and "`FOR`" field reads  `LEGACY` , which implies it's a `credit` contract for an incoming `Legacy` transaction.

#### Tritium to Legacy Transactions:



Tritium to Legacy  transactions are carried out when a user send NXS to an exchange account, or  to a personal legacy account. This transaction will only list the `debit` to the Tritium account and can be easily recognised by checking the "`OPERATION`" field which should read `LEGACY` and also the "`TO`" address will start with 2 which is a Legacy address.

Now that this guide helps users to make out the type of transactions done and the amounts transferred which gives a better understanding of how NXS flows on the network.

To keep the visual differences based on amounts, the alerts have been grouped based on the transactions and named after fishes. The legend is given below:

* \>= 500,000 NXS:    Blue Whale
* \>= 250,000 NXS:    Sperm Whale
* \>= 100,000 NXS:    Humpback Whale
* \>= 80,000 NXS:      Whale Shark
* \>= 60,000 NXS:      Tiger Shark
* \>= 30,000 NXS:      Blue White Shark
* \>= 10,000 NXS:       Dolphin
* \>= 5,000 NXS:         Tuna
* \>= 1,000 NXS:         Sardine
* < 1,000 NXS:           Shrimp  - (This is not used now as its < 1000NXS)

