# Introduction

### Desktop Wallet Guide

****

The following guides below walk you through the Nexus Desktop Wallet, from initial installation to the use of its core modules. Alternatively, there is an introductory video available below.

The videos below are brought to you by [The Digital Future!](https://www.youtube.com/channel/UC1lMk6jKYv4lg6gs1oS\_OYw)

An introduction to the Nexus Tritium Wallet:

Installing the Nexus wallet on a Linux device:

Bootstrap and Synchronize:

Creating a Recovery Phrase:

**Disclaimer and Loss of Password**

NXS is a peer-to-peer cryptocurrency that provides fast, low-cost, borderless, and secure transactions without the requirement of a bank or third-party intermediary. You personally own your NXS and Nexus Wallet, they are not owned or governed by a central authority. This is in direct contrast to a bank, in which the money held inside an account is legal property of the bank rather than the account holder. Nexus provides individuals with economic freedom, and with this freedom comes true responsibility for the safety of your own finances.

The Nexus Wallet is the safest place to store NXS. If coins are stored on a centralized exchange or a mining pool, then that entity has full custody. Third party custody comes with a multitude of risks. To ensure you maintain ownership, we recommend that NXS is held in the new Tritium Wallet. Nexus is a decentralized organization and our software is licensed under an MIT/X11 open source license. You are the sole custodian of your coins, we can not help you if you lose or forget your username, password or PIN. The wallet also provides a recovery phrase in case of lost password and PIN. It is the users responsibility to create the recovery phrase and keep it safe as a backup. In case of compromised password, PIN or recovery phrase the wallet has the option to change these as per your convenience. **Please make sure to keep your username, password, PIN and recovery phrase extremely safe**.

**Wallet Setup**

Nexus provides installers for Mac, Windows and Linux. Installation is as simple as downloading and installing any desktop application. The minimum system requirements are as follows:

**Operating System Requirements:**

* Mac OS X Yosemite 10.10 or later
* Windows 7 or later (Windows 10 Recommended)
* Any Linux 64 Bit distribution (Ubuntu LTS recommended for CLI users)

**X64 Systems:**

* Intel core i3 / Ryzen 3 processors
* 4 GB of RAM
* 200 GB of disk space HDD/ SSD (The wallet & database will use around 15 GB and will keep increasing slowly with time. To install and run any other applications on the same computer increase the memory and disk space accordingly)

**ARM / IOT:**

* Raspberry Pi 4, 4GB or equivalent Single Board Computer (Core only on Linux)

**Download:**

The Nexus Desktop Wallet can be downloaded from the wallets page on Nexus.io.

****

**Install:**

Follow the instructions on the pop up box to install.

Mac -> Drag the Nexus logo into the Application file.

If you see a dialog indicating that the developer cannot be verified, you will need to click the Open Anyway button.

Go to your applications folder and double click on the Nexus Wallet logo.

Click Open

Windows -> In Windows Explorer, find the wallet installation package you downloaded, and double-click on it. If running Windows 10 and receiving a Windows Defender screen indicating that the file should not be run, click on More Actions, then Run Anyway. Acknowledge the license agreement by clicking the “I Agree” button. Click the “Next”, “Install”, and “Finish” buttons on their respective screens.

Linux -> Check out the [video tutorials](broken-reference) for instructions on how to install the Nexus wallet on a Linux system.

The Nexus Wallet terms are under an MIT/X11 licence. They constitute a legally binding agreement and govern the use of the Nexus Wallet. These terms and conditions must be accepted prior to use:

The MIT License (MIT)

Copyright 2019 Nexus

Permission is hereby granted, free of charge, to any person

obtaining a copy of this software and associated documentation files

(the "Software"), to deal in the Software without restriction,

including without limitation the rights to use, copy, modify, merge,

publish, distribute, sublicense, and/or sell copies of the Software,

and to permit persons to whom the Software is furnished to do so,

subject to the following conditions:

The above copyright notice and this permission notice shall be

included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,

EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF

MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND

NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT

HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,

WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,

OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER

DEALINGS IN THE SOFTWARE.

IMPROPER USE OF THIS SOFTWARE COULD LEAD TO PERMANENT LOSS OF COIN.

Before the Wallet can be used, it needs to be synchronized with the Nexus Blockchain. Bootstrap is the process of directly downloading the database and extracting in the core data folder to speed up the synchronization.

**Manual Bootstrap:**

To download the Bootstrap independently from the wallet, [please click here](http://bootstrap.nexus.io/tritium.tar.gz).

To install the bootstrap, In the wallet go to ‘Help’ menu and click on ‘Open Core Data Folder’. This opens the core data folder. Exit the wallet and extract the bootstrap into this folder which will overwrite the existing blockchain database. The last few % of the blockchain will be synched from peers when the wallet is started.

**Bootstrap in the wallet:**

There are two ways in which the Wallet can be synchronized:

1. Letting the wallet synchronise the database from its peers on its own by just leaving the wallet open: This will be very slow and may take a few hours to days depending on the internet connection.
2. ‘Bootstrapping’ the Wallet (downloading recent database): This is the faster option and will take approximately an hour or more depending on the internet connection. To download the recent database from within the wallet, in the top left menu bar, click on ‘File’ and then ‘Download Recent Database’.

**Core Modules**

The Overview module is the homepage of the wallet. The purpose of the globe is to show a selection of nodes the wallet is connected to.

Below is an explanation of the figures on the left hand side of the Overview module:

* **Balance (NXS):** Total NXS balance across all accounts in the signature chain.
* **Balance (USD):** The USD value of all NXS balances - calculated by multiplying _Balance (NXS) x Market Price (USD)_. The wallet comes with USD as the default currency. The base currency can be changed at the following location: _Settings -> Application -> Base Currency._
* **Incoming Balances (NXS):** This value shows the value of NXS that is coming into the wallet and has not yet been confirmed and fully received.
* **Market Price (USD):** The value of 1 NXS in the chosen default base currency (in this case USD).
* **Market Cap (USD):** This is calculated by multiplying the _Market Price (USD) x Total NXS Circulating Supply._
* **24HR Change (USD %):** The market value change in NXS over the last 24 hours.

Following is an explanation of the figures on the right hand side of the Overview module:

* **Connections:** This refers to the amount of random “nodes” which are connected. By default your node is limited to make up to 16 outgoing connections and 84 incoming (100 total). If you are behind a router at home then incoming connections will only be able to be made if you enable UPnP in the wallet (and your router supports it) or if you manually set up port forwarding on port 9888. You can change the configuration to have more than 16 outgoing (with maxoutgoing=xx) but it's not necessary, 16 is adequate.
* **Block Count:** The block count is the “height” of the blockchain. This number reflects the local node block count that can be verified against a Nexus Explorer’s current block height (meaning the wallet is up-to-date). If the block value on the wallet does not match that of a Nexus Explorer, then it is not in sync with the public blockchain. Use the ‘Download the Recent Database’ option (File -> Download Recent Database) to bootstrap the most recent version. Another method to validate synchronization is to look at the left icon in the top right-hand corner of the wallet. If it says “Synchronizing,” that means it is not up to date. On the other hand, if it says “Synchronized,” that means it is up to date.
* **Stake Rate:** This value represents the current rate used to calculate the reward for mining a Proof of Stake block, stated in the form of an annual NXS rate of return (%). The rate starts at 0.5%, and can increase to 3.0% after 12 months of continual staking.
* **Block Weight:** Upon receipt of a genesis transaction, this value will begin increasing slowly, reaching 100% in 3 days time. Every time you receive a staking transaction, the block weight resets.
* **Trust Weight:** An indication of how much the network trusts the node. It starts at 1.11% and increases in a nonlinear manner like stake rate does. The level of trust increases the stake weight (below), thus increasing overall chances of miningblocks and receiving staking rewards. It becomes easier to maintain trust as this value increases.
* **Stake Weight:** The higher a wallet’s stake weight, the greater chances of receiving a trust transaction. The exact value is derived from the trust weight and block weight.

To read more about staking terms, please refer to the [FAQs & GLOSSARY](broken-reference).

The User module displays the signature chain’s (SigChain) username, and user ID, which is the address hash of the SigChain.

* **Accounts:** Displays the accounts belonging to this SigChain.
*
  * **Details:** These links associated with each account display the details of the account, shown in the screenshot below. The screenshot shows an account named _trust_, one of the two default accounts created when a SigChain is created. The other default account is named _default_. The _trust_ account is for staking NXS. Please refer to the [Staking guide](broken-reference) section for more information.
  * **History:** These links display the transaction history for the associated account.

To create a new account on this SigChain for NXS or a token on the Nexus blockchain, click the _Create new account_ button at the top of the Accounts tab of the User screen.

* **Staking:** Displays this SigChain’s staking metrics.
*
  * **Stake amount:** Displays the amount of NXS in this SigChain’s trust account that has been assigned to stake. _Stake Rate, Trust Weight, Block Weight,_ and _Stake Weight_ are all explained in the [Overview module](broken-reference) section.
  * **Unstaked Amount:** Displays the amount of NXS in this SigChain’s trust account that is unassigned and not staking. This is where stake rewards for this SigChain will appear.
  * **Adjust stake amount:** Click to change the amount of NXS assigned to stake. When adjusting the staking amount, note that the change will not take effect until the wallet mines its next block. Please refer to the [Staking guide](broken-reference) for more information.
* **Tokens:** Please refer to the [Tokens guide](broken-reference) for a detailed discussion of what tokens are and how they are created.
*
  * Use the below button to search for a token.
*
* **Names and Namespaces:** Please refer to the Namespaces guide for detailed coverage of the process of creating names and namespaces.
* **Assets:** Please refer to the [Assets guide](broken-reference) for detailed coverage of the process of creating assets, otherwise known as NFTs.

To send NXS or a Token to another address, or to move NXS between your personal accounts, go to the Send module, and please follow the below instructions:

1. _**Send From:**_ Select the account to send from using the drop down list which contains all available accounts.
2. _**Send To**_: Select one of your personal accounts using the drop down list, contacts saved in your address book, or copy and paste a new payee address. Tritium enables the use of the receivers username:account (case sensitive) like in the image below Zin:default (ZIN is the username and default is the account), this makes it easy for new users to transact and also avoids mistakes when copying the hex address.
3. _**Amount:**_ Enter the NXS or Token quantity you would like to send.
4. _**Reference Number:**_ Add an optional reference, invoice or order number.

To send tokens, select the token account in the Send From field using the drop down list. This changes the Amount label to the selected token.

The Transactions module displays all of the transactions on the currently logged in signature chain (SigChain).

Transactions can be filtered by any of the following criteria:

* **Address:** Specify an address on the SigChain previously used to send or receive NXS or tokens.
* **Name:** Specify “NXS” or the name of a token which was previously involved in transactions on this SigChain.
* **Time Span:** Using one of the time periods in the image below, specify the time period of transactions to filter.
* **Operation:** Using one of the operation names in the image below, specify the operation of transactions to filter.
* **Write:** Used to write raw data to a register.
* **Append:** Additional data applied to an append-only register.
* **Create:** Used create new object registers (e.g. accounts, assets, tokens, names).
* **Transfer:** Transfer ownership of a register (e.g. asset) to another signature chain.
* **Claim:** Claim ownership of a register that has been transferred to you.
* **Coinbase:** Miner reward transactions.
* **Trust:** Stake reward transactions.
* **Genesis:** The first stake transaction initializing the staking process.
* **Debit:** NXS/tokens sent from an account.
* **Credit:** NXS/tokens received to an account.
* **Migrate:** One-time migration of legacy trust keys to tritium staking.
* **Fee:** Associated costs for transaction.
* **Legacy:** Transactions made from or received to a legacy address.

Click on any transaction to see more details, such as the account addresses, transaction ID, hash, number of confirmations, token name, and amount of the transaction.

Here you can save your addresses by Contact name, by clicking on the ‘New Contact’ button, which will open up a dialog shown in the image below. Addresses saved to your Address Book will appear in the ‘Send To’ section of the Send module.

At the top of the page the first icon will also open up the above dialog to add a new contact.

The second icon allows you to export your contacts in a .csv file.

There is also a search function to search for a contact in your address book.

There are 4 pages within settings: Application, Core, Style, Modules.

**Application**

**Language:** Select your language of choice. The default language is English.

**Minimize on close:** With this enabled, even though the Wallet disappears, it is still open in the background. To re-open your Nexus Wallet do the following:

* Mac: Click on the Nexus logo in the top right hand corner, and then click ‘Show Nexus Wallet’
* Windows: Double click on the Nexus logo in the bottom right hand corner menu.

With this enabled, your Wallet (node) will still be online; this is therefore advisable. If your Wallet application is closed fully (Minimize on Close setting Disabled), then you will not be in sync with the Nexus Blockchain when you next open the application, and will therefore need to catch up to the current block.

**Auto update:** Rather than having to manually download a new Wallet each time a new update is released, which is a common necessity with many cryptocurrency Wallets, the Nexus Wallet notifies you of an update to be accepted, comparable to regular computer software updates.

Nexus strongly recommend that this setting remains enabled. This setting enabled will automatically check for new versions and notify you if a new version is available. If automatic updates are not enabled, you will be required to manually download the new Wallet version either from github.com/Nexusoft/NexusInterface or our website.

Any Wallet updates will show in a pop up box. These updates must be installed as soon as possible. Not having your Wallet on the newest version update will put your coins at risk, and could mean you are no longer synchronised with the Nexus Blockchain. **Please ensure you update your Wallet as soon as you are notified of an update.**

**Send anonymous usage data:** Send anonymous data usage to allow the Nexus developers to improve the Wallet.

**Base Currency:** The option selected will be the currency in which the Balance, Market Price, Market Cap & 24hr is displayed in. The default currency is USD.

**Minimum Confirmations:** Minimum amount of confirmations before a block is accepted. The minimum number of confirmations is 1, but you can customize how many you require to wait before your Wallet sees the transaction as valid. 3 to 6 confirmations are recommended to maintain high levels of security.

**Backup Directory:** This is where your Nexus Wallet Backups are stored. When you click ‘Backup Wallet’, you are prompted with a dialogue box that allows you to select a custom directory other than the default ‘Nexus Backups’ directory.

**Developer Mode:** Development mode enables advanced features to aid in development. After enabling, the Wallet must be closed and reopened to enable those features

**Core**

**Enable Mining:** When mining is enabled, your Wallet will run a special server called the ‘Mining LLP’, which will allow you to connect an external miner to your Wallet for producing blocks on the Prime or Hash channels.

**Enable Staking:** When Staking is enabled (the default), your Wallet is enabled for Staking and will stake your Trust Account whenever you log in. You must also have ‘Staking Enabled’ in order for your Wallet to receive Trust payments. This is to prevent people from unintentionally Staking coins.

**Verbose Level:** Verbose level for logs shows more under the hood data on the network. We recommend that you run verbose level 0 if you don’t need to see a lot of logging information. If you experience Wallet troubles though, more debug data is important for the developers to use to find bugs and push new releases. Use this setting at your own discretion.

**Style**

**Render Globe:** Turn the globe on or off.

**Overview Display:** Customize the Wallet Display. The options are:

* Standard: The Wallet comes with the globe.
* Miner: Displays Mining metrics, such as Prime, Hash and Stake difficulty.
* Hidden Balance: Hide your NXS, USD, and incoming balances.
* None: Display only the modules and twinkling stars.

**Nexus Address Format:** Format your NXS addresses to your liking. Note, the format (e.g. the 9 spaces in the Segmented style) is NOT copied over when copying an address. This is just for visual preference only. The options are:

* Segmented
* Truncate middle
* Raw

**Theme:**

There are two default themes Dark and Light.

**Background:** We provide two default default backgrounds Twinkling stars and Cosmic Light. You can also upload a custom wallpaper that you have saved on your device.

**Color scheme:** Change the colors to customize your own theme. Upon changing a color in one of the default themes you will see that your ‘Theme’ changes from either Dark or Light to ‘Custom theme’. If you were to then revert back from Custom theme to Dark theme for example, and then back to ‘Custom theme’, you will find that your custom theme has been saved.

**Import Custom Theme:** A variety of custom themes created by the Nexus community can be imported into the Wallet. The below link holds a repository of community made themes. The background can be imported from your local machine, or enter a URL and the Wallet will download the background for you. Acceptable formats are PNG/JPEG/BMP/TIFF/GIF.

**Export Custom Theme:** Themes are Json files that are read by the system and apply changes to the interface. When you export a theme, you will be prompted to save the json file to your computer. Below is a link to the theme guide which describes how to develop themes. If you would like to, please request that your theme is included in the official repository for it to be shared with the community.

**Modules**

Security is very important, and therefore modules are sandboxed to prevent any misuse.

To import a module, simply drag the file into the center of this page.

Module app icons will appear in the bottom menu to the right of the Console icon.

Documentation on how to write modules : [https://github.com/Nexusoft/NexusInterface/tree/master/docs/Modules](https://github.com/Nexusoft/NexusInterface/tree/master/docs/Modules)

We recommend using one of these links as a starting point:

* React-Redux Example: [https://github.com/Nexusoft/react\_redux\_module\_example](https://github.com/Nexusoft/react\_redux\_module\_example)
* React Example: [https://github.com/Nexusoft/simple\_react\_module\_example](https://github.com/Nexusoft/simple\_react\_module\_example)
* HTML Example: [https://github.com/Nexusoft/minimal\_module\_example](https://github.com/Nexusoft/minimal\_module\_example)

The console area of the Wallet is the most ‘technical’ part. We’d recommend only using this if you feel comfortable with CLI (Command Line Interface).

Within the Console, a variety of commands can be made that send instructions to the daemon. This is very useful for debugging your Wallet, and will be used to develop more functionality as developers extrapolate new modules from the available data on our blockchain.

Entering the text ‘Help’ into the console and then pressing Execute will provide a complete list of all the console commands as below:

* **addmultisigaddress <\["key","key"]> \[account]** - Add a required-to-sign multisignature address to the wallet each key is a nexus address or hex-encoded public key. If \[account] is specified, assign address to \[account].
* **backupwallet \<destination>** - Safely copies wallet.dat to destination, which can be a directory or a path with filename.
* **checkwallet** - Check wallet for integrity.
* **dumpprivkey \<NexusAddress>** - Reveals the private key corresponding to \<NexusAddress>.
* **echo \[param]...\[param]** - Test function that echo's back the parameters supplied in the call.
* **encryptwallet \<passphrase>** - Encrypts the Wallet with \<passphrase>.
* **getaccount \<Nexusaddress>** - Returns the account associated with the given address.
* **getaccountaddress \<account>** - Returns the current Nexus address for receiving payments to this account.
* **getaddressesbyaccount \<account>** - Returns the list of addresses for the given account.
* **getbalance \[account] \[minconf=1]** - If \[account] is not specified, returns the server's total available balance. If \[account] is specified, returns the balance in the account.
* **getblock \<hash> \[txinfo]** - txinfo optional to print more detailed tx info. Returns details of a block with given block-hash.
* **getblockcount** - Returns the number of blocks in the longest block chain.
* **getblockhash \<index>** - Returns hash of block in best-block-chain at \<index>.
* **getblocknumber** - Deprecated. Use getblockcount.
* **getconnectioncount** - Returns the number of connections to other nodes.
* **getdifficulty** - Returns difficulty as a multiple of the minimum difficulty.
* **getinfo** - Returns an object containing various state info.
* **getmininginfo** - Returns an object containing mining-related information.
* **getmoneysupply \<timestamp>** - Returns the total supply of Nexus produced by miners, holdings, developers, and ambassadors. Default timestamp is the current Unified timestamp. The timestamp is recorded as a UNIX timestamp.
* **getnetworkhashps** - Get network hashrate for the hashing channel.
* **getnetworkpps** - Get network prime searched per second.
* **getnetworktrustkeys** - List all the Trust Keys on the Network
* **getnewaddress \[account]** - Returns a new Nexus address for receiving payments. If \[account] is specified (recommended), it is added to the address book so payments received with the address will be credited to \[account].
* **getpeerinfo** - Returns data about each connected network node.
* **getrawtransaction \<txid>** - Returns a std::string that is serialized, hex-encoded data for \<txid>.
* **getreceivedbyaccount \<account> \[minconf=1]** - Returns the total amount received by addresses with \<account> in transactions with at least \[minconf] confirmations.
* **getreceivedbyaddress \<Nexusaddress> \[minconf=1]** - Returns the total amount received by \<Nexusaddress> in transactions with at least \[minconf] confirmations.
* **getsupplyrates** - Returns an object containing current Nexus production rates in set time intervals. Time Frequency is in base 13 month, 28 day totalling 364 days. This is to prevent error from Gregorian Figures.
* **gettransaction \<txid>** - Get detailed information about \<txid>.
* **help \[command]** - List commands, or get help for a command.
* **importprivkey \<PrivateKey> \[label]** - Adds a private key (as returned by dumpprivkey) to your Wallet.
* **isorphan \<hash>** - Returns whether a block is an orphan or not.
* **keypoolrefill** - Fills the keypool, requires Wallet passphrase to be set.
* **listaccounts** - Returns object that has account names as keys, account balances as values.
* **listaddresses \[max=100]** - Returns list of addresses
* **listreceivedbyaccount \[minconf=1] \[includeempty=false]** - \[minconf] is the minimum number of confirmations before payments are included. \[includeempty] whether to include accounts that haven't received any payments. This returns an array of objects containing:
*
  * "account" : the account of the receiving addresses
  * "amount" : total amount received by addresses with this account
  * "confirmations" : number of confirmations of the most recent transaction included
* **listreceivedbyaddress \[minconf=1] \[includeempty=false]** - \[minconf] is the minimum number of confirmations before payments are included. \[includeempty] whether to include addresses that haven't received any payments. This returns an array of objects containing:
*
  * "address" : receiving address
  * "account" : the account of the receiving address
  * "amount" : total amount received by the address
  * "confirmations" : number of confirmations of the most recent transaction included
* **listsinceblock \[blockhash] \[target-confirmations]** - Get all transactions in blocks since block \[blockhash], or all transactions if omitted
* **listtransactions \[account] \[count=10] \[from=0]** - Returns up to \[count] most recent transactions skipping the first \[from] transactions for account \[account].
* **listtrustkeys** - List all the Trust Keys this Node owns.
* **listunspent \[minconf=1] \[maxconf=9999999] \["address",...]** - Returns array of unspent transaction outputswith between minconf and maxconf (inclusive) confirmations. Optionally filtered to only include txouts paid to specified addresses. The results are an array of objects, each of which has:{txid, vout, scriptPubKey, amount, confirmations}
* **makekeypair \[prefix]** - Make a public/private key pair. \[prefix] is optional preferred prefix for the public key.
* **move \<fromaccount> \<toaccount> \<amount> \[minconf=1] \[comment]** - Move from one account in your Wallet to another.
* **repairwallet** - Repair wallet if checkwallet reports any problem.
* **rescan** - Rescans the database for relevant wallet transactions.
* **reset** - Restart all node connections
* **sendfrom \<fromaccount> \<toNexusaddress> \<amount> \[minconf=1] \[comment] \[comment-to]** - \<amount> is a real and is rounded to the nearest 0.000001 requires wallet passphrase to be set with walletpassphrase first.
* **sendmany \<fromaccount> {address:amount,...} \[minconf=1] \[comment]** - amounts are double-precision floating point numbers requires wallet passphrase to be set with walletpassphrase first.
* **sendrawtransaction \<hex std::string> \[checkinputs=0]** - Submits raw transaction (serialized, hex-encoded) to local node and network. If checkinputs is non-zero, checks the validity of the inputs of the transaction before sending it.
* **sendtoaddress \<Nexusaddress> \<amount> \[comment] \[comment-to]** - \<amount> is a real and is rounded to the nearest 0.000001 requires wallet passphrase to be set with walletpassphrase first.
* **setaccount \<Nexusaddress> \<account>** - Sets the account associated with the given address.
* **signmessage \<Nexusaddress> \<message>** - Sign a message with the private key of an address.
* **stop** - Stop Nexus server.
* **unspentbalance \["address",...]** - Returns the total amount of unspent Nexus for given address. This is a more accurate command than Get Balance.
* **validateaddress \<Nexusaddress>**- Return information about \<Nexusaddress>.
* **verifymessage \<Nexusaddress> \<signature> \<message>**- Verify a signed message.
* **walletlock** - Removes the wallet encryption key from memory, locking the wallet. After calling this method, you will need to call walletpassphrase again before being able to call any methods which require the wallet to be unlocked.
* **walletpassphrase \<passphrase> \[timeout] \[mintonly]** - Stores the wallet decryption key in memory for \[timeout] seconds. mintonly is optional true/false allowing only block minting. timeout is ignored if mintonly is true / 1.
* **walletpassphrasechange \<oldpassphrase> \<newpassphrase>**- Changes the wallet passphrase from \<oldpassphrase> to \<newpassphrase>.

**Core Output:** Depending on what setting you use for ‘Verbose’, this will show you live output from your actual Nexus Node. We don’t recommend every user watch this closely, as it is more technical information. But if you are ever curious to see what is going on under the hood, this is the place to watch.

**Wallet Functions**

Before creating a new user account, your Wallet must be fully synchronized with the Nexus Blockchain. See [Bootstrap and Synchronize](broken-reference) if this still needs to be completed.

To create your user account, simply choose a username, password, and PIN number.

Username: It must be at least 3 characters long and it’s case sensitive. Examples: Oliver Queen, Oliver.Queen, oliverqueen. We recommend keeping the username simple, because it is the easiest way to transact on Tritium (username:default will be the address to receive nxs or tokens. Example: Oliver Queen:default).

Password: It must be at least 8 characters. It can contain lower and upper case alphabets, numerals from 0-9 and special characters.

PIN: It must be at least 4 digits. It can contain alphanumeric and special characters, and can be used as a second password.

When you submit your create new user request, your Wallet must complete a small proof of work that may take up to 30 seconds. Then, it will create your Signature Chain and submit it for processing. **You cannot log in with your new user account until after this processing is complete and your Signature Chain is added to the Nexus Blockchain.** This may happen with the next new block added, or it may take more than one block.

Typically, it should take less than 5 minutes, after which you can log into your Wallet and access your new user account.

**PLEASE DO NOT USE COMMON WORDS FOR YOUR PASSWORD, THIS WILL LEAVE YOU VULNERABLE TO DICTIONARY ATTACKS THAT COULD DRASTICALLY DECREASE THIS RESISTANCE.**

We therefore recommend that you use a secure [random number generator](broken-reference) to create your password.

The recovery system is designed to protect accounts in the case that credentials are lost or stolen. Think of it like a backup, to ensure that you don’t lose access to your NXS. **WE STRONGLY RECOMMEND THAT EVERY USER ACCOUNT HAS A RECOVERY PHRASE ENABLED.**

**Step 1: Open Recovery Dialogue**

Click the user icon in the top right hand corner of the Wallet, and select 'Set recovery phrase'.

**Step 2: Enter Login Credentials**

PLEASE NOTE: YOUR PASSWORD AND PIN ARE REQUIRED WHEN SETTING UP A RECOVERY PHRASE. Enter your credentials as you do when you are logging into your Wallet.

**Step 3: Generate Recovery Phrase**

Click the link titled 'Generate a recovery phrase'. You can select either 10, 20 or 100 words for your recovery phrase. We recommend using at least 20 words for better security.

BEFORE PROCEEDING, ENSURE THAT YOU HAVE WRITTEN DOWN YOUR RECOVERY PHRASE. WE RECOMMEND WRITING IT ON PHYSICAL MATERIAL, SUCH AS PAPER, TO ENSURE IT IS SAFELY STORED OFFLINE. WE RECOMMEND MAKING MORE THAN ONE COPY OF YOUR RECOVERY PHRASE.

**Step 4: Submit Recovery Phrase**

Click the button labeled 'Set recovery phrase' to generate your recovery phrase. THIS PROCESS CAN TAKE UP TO 30 SECONDS TO COMPLETE. DO NOT CLOSE YOUR WALLET UNTIL THIS COMPLETES.

Once your phrase has been setup, you will see a confirmation prompt:

To confirm that it was set up properly, you can go to your transaction module, to check the most recent transaction.

This shows the contract that updated your recovery phrase, which uses the primitive OP::WRITE.

**Forgot your Password?**

In order to change your password with your recovery phrase, you will need to click the link 'Forgot Password' at the bottom of the login page.

A dialogue box will open to submit your username, recovery phrase, new password and PIN.

You will then gain access to your account again! If you are extra paranoid, you can test recovering your account after you set it up (while using the same password) to make sure that everything is working as it should.

The recovery system works by using a special next hash, called the 'recovery hash' that allows the user to reset their password and PIN without needing account credentials.

As always, stay safe, be vigilant, and PLEASE set up your recovery phrase!

To receive NXS from another sender or an exchange such as Binance or Bittrex, or to receive a Token, go to the User module, and please follow the below instructions:

1. Go to the Account page.
2. Choose the recipient account.
3. Select the Copy to clipboard icon.
4. Send the copied address to the sender, or paste the address into your exchange Wallet. Tritium enables the use of username:account (case sensitive) in this image below will be sirius:default, this makes it really easy for new users to transact and also avoids mistakes when copying the hex address. (This cannot be used to transfer from exchanges as they still use legacy chain).

To receive tokens which are created by a different user account (Sig Chain), the user needs to create a token account first. Every token to be added will require a unique account. To create a token account, the user will need the token's name or address

Note:

* Nexus accounts, such as default, trust, or any other created by the user, cannot store tokens.
* Every user has to create the particular token account to be able to transact the token.

Go to User module on the bottom bar, select the Tokens tab on the left.

In the right, click on “Lookup a token”. In the box enter the token name (case sensitive) or token address and click “Lookup this token”.

If the name or address is correct, it will open the particular token's details.

At the bottom click on “Create new account with this Token”. Give it an unique “Account Name” and leave the Token field empty. click Create Account.

The new token account is created in the accounts page with a fee of 1 NXS deducted from the default account. The token address is also added to the tokens page.

To learn how to create tokens, please view our [Tokens Guide](broken-reference).

You can create as many accounts as you wish within your main user account, for the use of NXS or any other Token issued on the Nexus blockchain. Accounts are free to create, however if you choose to give your account a name (so that you can give out an easy readable address, rather than a hexadecimal address), then a fee of 1 NXS is applied.

To create a new Named account, please follow these steps:

1. Go to the User module
2. Accounts tab
3. Create new account

A new page will open up

1. Choose an Account Name
2. Choose whether the account is for NXS or for a Token
3. Create Account

To learn about staking, please view our [Staking guide](broken-reference).

**Additional Guides**

The following guide contains instructions on migrating your NXS from the Legacy QT wallet to the Tritium wallet.

**Before we start be sure to check you have the following which are absolutely essential for this migration.**

* The QT wallet legacy wallet.dat file. (It should be named as wallet.dat) or the Private Key (Paper Wallet).
* The encryption password for the wallet.dat file.

**Recommended Security:**

We recommend that users have at LEAST 8 characters in their password, and at LEAST 4 characters in their PIN. This will make offline password cracking take 50 billion years to break the password/pin combination.

DO NOT USE COMMON WORDS FOR YOUR PASSWORD, THIS WILL LEAVE YOU VULNERABLE TO DICTIONARY ATTACKS THAT COULD DRASTICALLY DECREASE THIS RESISTANCE.

We therefore recommend you using [secure random number generators](broken-reference) for your password.

**Tritium Wallet Install, Bootstrapping, Synchronizing, and Creating User Account**

1. Download the Nexus Desktop Wallet on your computer. Nexus provides wallets for windows, Mac and Linux.
2. Once you download is complete [verify the installer integrity](broken-reference). Do not skip this step.
3. Install and run the wallet and at first launch it will ask to ‘Bootstrap the Database’ click ‘Yes, Let’s Bootstrap it’ and it will download the database and on completion will extract it to the core data folder.
4. The wallet will synchronize the last few blocks and on completion you can see a check mark icon at the top right.
5. You can double check the block count at [https://explorer.nexus.io/](https://explorer.nexus.io)
6. Create a user account by clicking the ‘User’ icon on the top right corner and selecting ‘Create new user’.
7. In the ‘Create new user’ box enter user name, password and PIN. Click on ‘CREATE USER’, this opens the “Confirm your password and PIN” box, enter your password, PIN and click ‘Confirm’, this creates the new user. It will take 2 blocks to confirm your new user account and a message will be displayed on the top left corner.
8. Log in to your user account by clicking the ‘User’ icon on the top right corner and selecting ‘Log in’. In the Log in box enter your user name, password and pin and click ‘Log in’
9. If your credentials are correct you will get a message on the top left corner “Logged in as ‘User name’”

**Wallet.dat Migration:**

1. Click on the ‘User’ module on the bottom bar and you will be taken to the ‘Accounts’ page where the two accounts created by default are listed. The accounts are ‘default and ‘trust’
2. Copy the address to where you want to send NXS, by hovering on the address box and clicking it (or use the copy button on right of the address) to copy to clipboard. (If you want to stake, your coins have to be in the trust account only.)
3. Go to Help menu and click on “Open Core Data Folder” which will open the core data folder.
4. Close the wallet.
5. Copy your legacy wallet.dat file in the core data folder opened in step 3 (This will replace the existing wallet.dat file created at start. If you have any NXS do back it up)
6. Run the Tritium wallet and then go to ‘File’ menu and click on “Switch to Legacy Mode”.
7. Go to the lock icon on top right corner and It will prompt you for the encryption password to open wallet.dat file. Enter password and click ‘Log In’ . On a successful login “Logged in Successfully” message is dispalyed at the top left corner.
8. Click on ‘Core’ tab and click “Rescan Wallet” and after completion click on “Reload” button to reload your transactions. After it is complete your balance will be visible on the overview or the ‘User’ module Accounts tab.
9. Next step is to send your legacy balance to the Tritium address. Click on the send module on the bottom bar which opens the Send NXS page. Here “SEND FROM” is your legacy address, “SEND TO” is the Tritium address copied in the earlier step. “NXS AMOUNT” enter the full amount of NXS in your legacy wallet and click ‘send’. (This will send your full legacy balance to your Tritium address)
10. On a successful transaction go to File menu and click on “Switch to Tritium Mode”. After a few blocks you should see your NXS balance in the wallet overview.
11. Be sure to [set your Recovery phrase](broken-reference) by clicking on the ‘User’ icon on the top right and clicking “Set Recovery Phrase”.

**Private Key Migration:**

1. Run the Tritium wallet and then go to ‘File’ menu and click on “Switch to Legacy Mode”.
2. If you have encrypted the legacy wallet then unlock the wallet. Go to the lock icon on top right corner and It will prompt you for the encryption password to open wallet.dat file.
3. Click on ‘Settings’ module in the bottom bar, go to ‘Security’ tab on the top and go to the “IMPORT PRIVATE KEY” window.
4. Fill in the Account Name (Label to distinguish the account, except ‘default’ which is already created by default) and the Private Key and click ‘Import’
5. Go to the user icon on top right and select ‘My Addresses’, this will open a window which will list all the legacy addresses for your account. You will find your new account listed here. (The ‘default’ account is created on automatically at wallet start)
6. Go to ‘Settings’ module in the bottom bar (gears icon), click on ‘Core’ tab and click “Rescan Wallet” and after completion click on “Reload” button to reload your transactions. After it is complete your balance will be visible on the overview or the ‘User’ module Accounts tab.
7. Next step is to send your legacy balance to the Tritium address. Click on the send module on the bottom bar which opens the Send NXS page. Here “SEND FROM” is your legacy address, “SEND TO” is the Tritium address copied in the earlier step. “NXS AMOUNT” enter the full amount of NXS in your legacy wallet and click ‘send’. (This will send your full legacy balance to your Tritium address)
8. On a successful transaction go to File menu and click on “Switch to Tritium Mode”. After a few blocks you should see your NXS balance in the wallet overview.
9. Be sure to [set your Recovery phrase](broken-reference) by clicking on the ‘User’ icon on the top right and clicking “Set Recovery Phrase”.

We recommend that users have at LEAST 8 characters in their password, and at LEAST 4 characters in their PIN. This will make offline password cracking take 50 billion years to break the password/pin combination.

DO NOT USE COMMON WORDS FOR YOUR PASSWORD, THIS WILL LEAVE YOU VULNERABLE TO DICTIONARY ATTACKS THAT COULD DRASTICALLY DECREASE THIS RESISTANCE.

We therefore recommend you using secure random number generators for your password:

**Windows Random Number Generator:**

[https://slproweb.com/products/Win32OpenSSL.html](https://slproweb.com/products/Win32OpenSSL.html)

1. Go to the above link and download openssl (lite version only) for 32 or 64 bit windows.
2. Install the openssl package with the default options
3. Go to Start > Run
4. In the open box, type `cmd` and click OK.
5. A command prompt window appears.
6. `cd \Program Files\OpenSSL-Win64\bin` Type this command at the prompt and press Enter. (Change Win64 to Win32 if you have 32 bit version installed, also check the command is case sensitive - type exactly)
7. `openssl` Starts openssl (The command prompt changes to OpenSSL>.)
8. `rand -base64 8` Type this command at the prompt and press Enter. Once you get the code copy it for your password
9. `exit` To exit openssl and then close the window

**Linux Random Number Generator:**

Open the terminal and type or copy the commands using Ctrl+Shift+v

1. `$ sudo apt update; sudo apt upgrade -y` This refreshes the package manager
2. `$ sudo apt install openssl` This installs the Openssl package
3. `$ openssl rand -base64 8` This generates the random number.

The above password generator will provide account security comparable to the above 50 billion years to break, and not include any common words that would enable a dictionary attack success.
