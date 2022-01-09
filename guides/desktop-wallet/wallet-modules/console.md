---
description: Console
---

# Console

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

\
