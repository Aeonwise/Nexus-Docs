---
description: Create a Token Using Nexus Interface
---

# Create a Token

This guide will help users to create a **Token** using the Nexus Interface

Before we start to create a token, users need to be familiar with some of the concepts and parameters used with tokens.

## Token Parameters

Token parameters are what define a token like token name, supply and decimals. Learn more about them below:

### TOKEN NAME

This is a local name to identify the token and is optional. This name resides inside the user account (Sigchain) and is not valid outside it.

{% hint style="info" %}
Token name has a separate fee of 1NXS. Issuer can opt not to create a token name and can use the register address to access or search the Asset. This is a local name and is not valid outside the Sigchain.
{% endhint %}

{% hint style="info" %}
If there is a need for a unique global name (ticker) for the token, then the issuer needs to create a Global name and link it to the token.
{% endhint %}

### SUPPLY

This is the total number of fungible tokens that needs to be generated. The fee increases with a higher supply. Check the fees [here](../../readme/fees.md).

{% hint style="info" %}
The max supply of the token cannot be increased once the token is generated.
{% endhint %}

### DECIMAL

This is the no of decimal places for the token, increasing the decimal places also increases the fee. Decimal units are required for micro transactions and is set depending upon the token usage and tokenomics.&#x20;

## Token Accounts:

To create and use token the users need to understand the different token accounts and the token properties:

Once the token is created, the token generation address will be listed in the "Tokens" page. This is the token generating address, and not a token account. This generating address is owned by the user account which issued the token and the user needs to create a token address to receive the tokens.&#x20;

The tokens which are in the generating address can be burnt to remove them permanently out of circulation. This option is not available in the interface today.

### Token Generation Address&#x20;

This is the register address which generates that particular token and tokens in this address are out of circulation. Tokens when sent out to a token account come into circulation. Users can send tokens back to the generation address to remove them from circulation.

### Token account:&#x20;

This is a normal token account which can receive a particular token either from a generation address or another token account. Each token account is liked only to a particular token and cannot receive any other token. Every user has to create a token account to transact a particular token.

{% hint style="warning" %}
Token accounts can only receive the particular token they are linked to. They cannot accept NXS or any other token. The standard "default", "trust" or any NXS account cannot accept any tokens.&#x20;
{% endhint %}



Once created, the token has three important properties:

* maxsupply - the maximum number of tokens that will exist
* currentsupply - the number of circulating tokens that have been distributed to token accounts
* balance - the number of tokens that have not yet been distributed (maxsupply - currentsupply)

### Token Minting Fees

The fee is based on the number of token divisible units you define (the combination of supply and decimals). There is a minimum fee of 1 NXS and the calculation is linear thereafter, so that each additional significant digit costs an additional 100 NXS. E.g.

100 units = 1 NXS

1000 units = 100 NXS

1000000 units = 400 NXS

10000000000 units = 800 NXS

## Create a Token

To create a token using the Interface follow the steps below:

* Open the Nexus Interface, make sure the wallet is fully synched and log into the user account (Sigchain).
* In the Overview page, at the bottom click on the "_User"_ module. This opens the User page.
* In the User page, on the left side click on the "_Tokens_" tab.
* In the Assets page click on "_Create a new token_". This opens the _New Token_ page.&#x20;
* In this page the user has to provide three parameters which define the token. The parameters  and their details are given below:
* Once the parameters are provided, click on the "Create token" button on the bottom of the page.
* Once the token is confirmed on the blockchain, it will be listed in the "Tokens" page.
* To check the details of any token, click on the token address in the "Tokens" page and the token details page will open with the details.
