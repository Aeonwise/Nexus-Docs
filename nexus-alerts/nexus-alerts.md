---
description: Nexus Alert Bot
---

# Nexus Alerts

Nexus Alerts,  a telegram bot will list transactions on the Nexus blockchain above 1000 NXS or tokens. This bot was born from a community request to track network growth, way to value Nexus by tracking online transactions, total NXS on tritium chain vs NXS on exchanges and also a way to be aware of large transaction leading to pumps and dumps.&#x20;

{% hint style="info" %}
The Alerts only tracks transactions on the tritium network only.
{% endhint %}

## Data Shown in Alerts:

Each transaction taking place on the blockchain is checked for a credit and that is sent out as an alert to the Nexus Alert Bot. This data shown with the alerts is as below:

![](<../.gitbook/assets/Alert Data1.png>)

* The fish icon which shows as per the [legend](nexus-alerts.md#legend).
* `Humpback Whale found on block` : Block Height.
* `Amount` : Amount of NXS or tokens included in the transaction.
* `Token`: The token for which the `credit` is generated. NXS or Token (name or address).
* `Operation` :  The operation of the contract. Only `CREDIT` contract is shown for alerts.
* `For` : This is the notification type for which the **`Operation`** was carried out.
* `Proof` :  The register address proving the credit or the sending address for `debit` from tritium.
* `To` : The receiving address.
* `Link` : The explorer link to the block height details.

## Understanding the Alert Data:

The alert bot is simple to understand but might be confusing to some, this guide will help with understanding the data provided.\
\
Nexus has the`Tritium` and `Legacy` chains, all exchanges use the legacy chain and it is difficult to track the balance of legacy accounts and the best we can do is keep track of the transactions on the tritium network. The alerts are only limited to tracking NXS and token transactions above 1000 NXS.

To better understand the data provided by the bot, we can segregate the transactions into:

* **Tritium to Tritium Transactions**
* **Legacy to Tritium Transactions**
* **Tritium to Legacy Transactions**

### Tritium to Tritium Transactions:&#x20;

![Tritium to Tritium transaction - Operation CREDIT ,  For  DEBIT.](<../.gitbook/assets/Tritium to Tritium1.png>)

Any transaction on tritium is a `debit` __ to the senders account and a `credit` to the receivers account. This creates two transactions for a single transfer similar to double accounting, but the bot  is designed to ignore the `DEBIT` and show only the `CREDIT,` as it's a single transfer and having two alerts will create more confusion.&#x20;

It is easy to distinguish as  the "`Operation`" field reads as `CREDIT` and the "`For`" field will read `DEBIT`, which implies it's a _`credit`_ for a corresponding _`debit`_. &#x20;



### Legacy to Tritium Transactions

![Legacy to Tritium transaction - Operation CREDIT ,  For LEGACY.](<../.gitbook/assets/Legacy to Tritium1.png>)

Legacy to tritium transactions are when a user withdraws NXS from the exchange into his Tritium account. This transaction will only list the `credit` to the Tritium account and can be easily recognised by checking the "`Operation`" field which should read `CREDIT` and "`For`" field reads  `LEGACY` , which implies it's a `credit` contract for an incoming `legacy` transaction.



### Tritium to Legacy Transactions:

![Tritium to Legacy transaction - Operation LEGACY and  To starts with 2.](<../.gitbook/assets/Tritium to Legacy1.png>)

Tritium to Legacy  transactions are carried out when a user send NXS to an exchange account, or  to a personal legacy account. This transaction will only list the `debit` to the Tritium account and can be easily recognised by checking the "`Operation`" field which should reads `LEGACY` and also the "`To`" address will start with `2` which is a legacy address.

###

### Legend:

To keep the visual differences based on amounts, the alerts have been grouped based on the transaction amounts and named after fishes as per size.

&#x20;The legend is given below:

* \>= 500,000 NXS:    Blue Whale (🐳🐳🐳🐳🐳🐳)
* \>= 250,000 NXS:    Sperm Whale (🐋🐋🐋🐋🐋🐋)
* \>= 100,000 NXS:    Humpback Whale (🐋🐋🐋)
* \>= 80,000 NXS:      Whale Shark (🦈🦈🦈🦈🦈🦈)
* \>= 60,000 NXS:      Tiger Shark  (🦈🦈🦈🦈)
* \>= 30,000 NXS:      Blue White Shark (🦈🦈)
* \>= 10,000 NXS:       Dolphin (🐬🐬)
* \>= 5,000 NXS:         Tuna (🐟🐟)
* \>= 1,000 NXS:         Sardine (🐠🐠)
* < 1,000 NXS:           Shrimp  (🦐🦐 )- (This is not used now as its < 1000NXS)

