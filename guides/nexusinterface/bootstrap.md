---
description: Download Recent Database
---

# Bootstrap

Before the wallet can be used, it needs to be synchronized with the Nexus Blockchain. Bootstrap is the process of directly downloading the database and extracting in the core data folder to speed up the synchronization.

### **Manual Bootstrap:**

To download the Bootstrap independently from the wallet, [please click here](http://bootstrap.nexus.io/tritium.tar.gz).

To install the bootstrap, In the wallet go to ‘Help’ menu and click on ‘Open Core Data Folder’. This opens the core data folder. Exit the wallet and extract the bootstrap into this folder which will overwrite the existing blockchain database. The last few % of the blockchain will be synched from peers when the wallet is started.

### **Bootstrap in the wallet:**

There are two ways in which the Wallet can be synchronized:

1. Letting the wallet synchronise the database from its peers on its own by just leaving the wallet open: This will be very slow and may take a few hours to days depending on the internet connection.
2. ‘Bootstrapping’ the Wallet (downloading recent database): This is the faster option and will take approximately an hour or more depending on the internet connection. To download the recent database from within the wallet, in the top left menu bar, click on ‘File’ and then ‘Download Recent Database’.
