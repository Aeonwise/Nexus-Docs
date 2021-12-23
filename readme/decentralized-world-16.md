# Decentralized World

**What is an Asset (NFT)?**

Assets are non-fungible tokens (NFTs), meaning they are non-divisible. In its simplest form, an Asset is nothing more than arbitrary data stored on the Nexus blockchain in a state register. You as the user can decide what data is stored in that Asset, and depending on the way the Asset is created, whether or not the data in the Asset can ever be changed (is mutable / immutable). Think of it like writing on a piece of paper. You can choose to write what you want on that piece of paper. If you write it in ink then it is permanent. If you write some of it in pencil, then you can erase it and change it to something else.

**What is a State Register?**

The Nexus architecture uses state registers for storing many different types of data including Accounts, Tokens, Names, and Assets. A state register sounds fancy, but it is really just a space where information can be stored. With the Nexus API, you can make special kinds of transactions to create these registers or update / append to the data in them. When the data in a register changes, it is said that the register is 'changing state' from what it was previously to what you are now changing it to - hence the name state register. Every register on the Nexus blockchain has two main properties: An address (referred to as a register address) which is used to determine the location of the data in the register database, and an owner, which is the genesis hash of the Signature Chain that currently owns the register.

**How do I create an Asset?**

The Nexus API provides a straightforward and intuitive interface for users to create, update, and transfer Assets. To create a basic Asset you can use the Wallet console or Nexus command line interface (CLI) and issue a simple command:

`assets/create/asset name=myfirstasset data=this_is_some_data`

The create/asset API method allows the Asset to be defined in several different formats. Shown above is the basic format, which is the default. In the basic format the data is supplied in key=value pairs, all data is treated internally as a string (a series of alphanumeric characters), and all data is immutable (cannot be changed). The create/asset API alternatively allows complex Assets to be defined using JSON format.

The following example shows how an Asset might be used to store the title deeds to a property:

`assets/create/asset`

`name=deed1A`\
`address=1640 Riversdale Drive, CA`\
`deed-id=494563494`\
`certificate-url=http://www.property.com/deeds/494563494.pdf`\
`certificate-md5-hash=67ac5a9362efdef5a52e5438c4ad7bda`

**How do I transfer an Asset?**

You can transfer ownership of an Asset to another Signature Chain with a simple API command specifying the name/address of the Asset you own, and the username/genesis of the recipient:

`assets/transfer/asset name=myasset username=bob`

Allowing users to store arbitrary data in a blockchain is not a new concept - we've been able to do that since the early days of Bitcoin. What's unique about Nexus' register-based blockchain is that all changes to a register - including changes to the data and to the ownership of it - are captured in the transactions recorded on the blockchain. Not only does this allow us to validate data changes via consensus rules, but it also allows us to view the entire history of changes to the data in a register and its ownership.

It becomes an audit log for data, allowing users to see what that data looked like and who owned it at any point in time. That's a hugely powerful concept and opens the door to many use cases where a history of the data is required, e.g. supply chains, postal tracking, land/real estate deeds, certificates of authenticity, art watermarking, wills, etc. Each Asset is owned by a Signature Chain, which is great for situations where there is one single owner of an Asset.

However, what about those use cases where partial ownership is required, for example where a piece of real estate is owned by two or more investors and they want to prove their ownership via a public blockchain? Nexus solves this by allowing an Asset to be tokenized, which means that the ownership of an Asset is transferred to a token rather than a Signature Chain. Once tokenized, any users that hold the tokens in their Signature Chain become partial owners of the Asset, much like owning shares in a company.

Furthermore, tokenized Assets provide the ability for shared revenue to be automatically distributed in the form of NXS payments to the partial owners of the Asset, based on the percentage of tokens held. This is useful for use cases such as the automatic payment of dividends for Security Token Offerings (STO's), and for the distribution of royalties from revenue earned from an Asset such as a music album.

The fee charged for creating Assets depends on the amount of data you are storing. The charge is 0.01 NXS ber byte, with a minimum fee of 1 NXS. This means that the cost of an Asset will be between 1 and 10 NXS depending on how much data it contains.

Currently all registers are limited to a maximum of 1Kb, which is about 1000 characters of text.

In order to update data in an Asset, you have to initially create them using a JSON format, as opposed to the basic format shown above. Using the JSON format allows you to specify field type, length, mutability, and an initial value for each data field in the Asset.
