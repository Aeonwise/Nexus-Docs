# Nexus Alert Bot

`Nexus Alert Bot,` a telegram bot which will list transactions above 500 NXS or tokens. This bot was born from a community request to track network growth, how to value Nexus, total NXS on tritium chain vs NXS on exchanges, a way to counter or at-least be aware of pump and dumps. It is going to be a tough task to implement all these aspects in one go.



The alert bot may looks simple, but might be confusing to some, this guide will help to understand the data provided in a better way.\
\
Nexus has `Tritium` and `Legacy` chains and all exchanges use the Legacy chain and it is difficult to track the balance of legacy accounts and the best we can do is keep track of the transactions on the network

We can segregate the transactions into

* Tritium to Tritium Transactions
* Legacy to Tritium Transactions
* Tritium to Legacy Transactions

#### Tritium to Tritium Transactions:&#x20;

Tritium being the main chain transactions on this chain. Any transaction on tritium is a DEBIT to the senders account and a CREDIT to the receivers account. This creates two alerts on the bot with the same AMOUNT, but is is easy to distinguish if you see the "`Operation`" field which lists if its a DEBIT or CREDIT.  The two operations might not be shown next to each other, as the receiving wallet has to be online and logged into the user account.

#### Legacy to Tritium Transactions

Legacy to tritium transactions, when a user withdraws from the exchange into his Tritium account. This transaction will only list the CREDIT to the Tritium account and can be easily recognised by checking the "Operation" field which will say.

#### Tritium to Legacy Transactions

Tritium to Legacy  transactions are carried out when a user send NXS to an exchange account. This can also be sent to a personal account also. This transaction will only list the CREDIT to the Tritium account and can be easily recognised by checking the "Operation" field which will show "LEGACY" and also the "TO address will start from 2.
