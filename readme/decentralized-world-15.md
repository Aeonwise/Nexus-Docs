# Decentralized World

**What is a Token?**

In the broader sense, tokens can be thought of as virtual currencies that exist on a blockchain.

**What can Tokens be used for?**

They can be used for a variety of uses such as:

1. Representing ownership in an [asset](broken-reference) such as a company, preperty or land title, rights to a piece of art, or patents.
2. Utilities
3. Loyalty programs
4. Gaming tokens
5. DAO voting rights

**How does a Token created on the Nexus blockchain differ to tokens created on Ethereum, Waves, NEO, NEM, Stellar, etc?**

The primary difference is simplicity. To create a token on Ethereum, or most other token platforms, users must write a smart contract - code written in a specific programming language - to define the token and how it will be used/distributed. This requires the user to have programming skills and the task can often be quite complicated. Nexus has taken a different approach by simplifying the process, allowing users to create a token in one short console command / API request. The wallet interface goes a step further providing a simple interface to guide users through the process.

**How do I create a token?**

Tokens can easily be created through the Nexus Wallet or the console/CLI. The user defines a new token so that it can be distributed, traded, or used to tokenize an asset.

To create a new Token, go to the User module in the Wallet, and please follow the below instructions:

1. Click on Tokens.
2. Click Create new Token.
3. Choose a Token Name.
4. Choose the total number of Tokens to be created.
5. Choose the amount of significant digits the Token will have.
6. At the top of the box, the fee will be displayed in NXS for creating your supply of tokens.
7. Click Create Token.
8. Pay Fees.

To achieve the same using the console use the following command:

`tokens/create/token name=My Token supply=100 decimals=2`

The tradeoff for simplicity is flexibility. A token created from a traditional smart contract allows developers to define any rules they wish for the distribution and use of a token, which are encoded in the token definition contract. This flexibility is certainly useful, but is overly complex for people without programming skills.

Nexus decouples the contract rules from the token definition allowing the token creation to be far simpler, though provides further steps if more complex rules are needed. For those use cases that require more complex token utility, Nexus users can add contract rules as conditions to token debit transactions.

If the rules are too complex to be supported by a transaction condition, developers can write these rules into their application layer.

When you first create a token you must specify the supply (the maximum number of whole tokens that will be available) and decimals (the number of decimal places that a token amount can have).

The combination of these two values gives the number of token divisible units that will be available (the equivalent of Bitcoin’s Satoshi’s property). For example a decimals value of 3 means that each token can be divided into 10^3 (1,000) parts. Therefore a token created with a supply of 1,000,000 and decimals of 3 would result in 1,000,000,000 (1,000,000 x 1,000) token divisible units. This is important, as this figure is what is used to calculate the fee applied when creating the token.

Once created, the token has three important properties:

* maxsupply - the maximum number of tokens that will exist
* currentsupply - the number of circulating tokens that have been distributed to token accounts
* balance - the number of tokens that have not yet been distributed (maxsupply - currentsupply)

The fee is based on the number of token divisible units you define (the combination of supply and decimals). There is a minimum fee of 1 NXS and the calculation is linear thereafter, so that each additional significant digit costs an additional 100 NXS. E.g.

100 units = 1 NXS

1000 units = 100 NXS

1000000 units = 400 NXS

10000000000 units = 800 NXS

Initially all of the token supply is held in the balance of the token. Distributing your token to other users is then very similar to how you send NXS. The first step is that the receiving users must create a new account for your token type and then provide you with the account name/address. Then you can use the wallet interface to send them just like you would send NXS, choosing the token from the Send From list. Alternatively, you can use the console with the following command:

`tokens/debit/token name=My Token name_to=paul:tokenaccount amount=1000`

At the time of writing, no the maximum supply cannot be changed once the token has been created. However, this ability is planned for a future release. How do I use a token to represent partial ownership of a digital or real-world asset?

One of the most significant use cases for tokens is the ability to tokenize an asset. Tokenized Assets provide the ability for shared revenue to be automatically distributed in the form of NXS payments to the partial owners of the Asset, based on the percentage of tokens held. This is useful for use cases such as the automatic payment of dividends for Security Token Offerings (STO’s), and for the distribution of royalties from revenue earned from an Asset such as a music album.
