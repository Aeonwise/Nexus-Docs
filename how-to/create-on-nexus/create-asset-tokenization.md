# Create Asset Tokenization

### What is Asset Tokenization

**Asset Tokenization** also referred as  "_Asset Backed Tokens"_ or "T_okenized Assets"_ is a new concept that uses digital tokens to fractionalize ownership of assets such as property, jewellery or fine art and uses contracts on blockchain to manage these ownership rights



This guide will help users to  create a _**Tokenized Asset**_ using the Nexus Interface.

Before we start to create an asset tokenization, users need to be familiar with some of the concepts and parameters used.

To tokenize an asset the user needs to create an asset and also create a token as per the guides linked below.

{% content-ref url="create-an-asset.md" %}
[create-an-asset.md](create-an-asset.md)
{% endcontent-ref %}

{% content-ref url="create-a-token.md" %}
[create-a-token.md](create-a-token.md)
{% endcontent-ref %}

{% hint style="info" %}
Make sure that the Asset and Token are named appropriately so they represent the same asset.&#x20;
{% endhint %}



## Create Asset Tokenization

To create a tokenised asset using the Interface follow the steps below:

* Open the Nexus Interface, make sure the wallet is fully synched. Log into the user account (Sigchain).
* In the Overview page, at the bottom click on the "_User"_ module. This opens the _User_ page.
* In the User page, on the left side click on the "_Assets_" tab.
* Under the Assets page, all the assets owned by the user account / Sigchain will be listed.
* Click on the Asset which is to be tokenized, this opens the "Asset Details" page.

![Asset Details Page](<../../.gitbook/assets/Asset Details.png>)

* At the bottom right of this page click on "Tokenize". This will open the "Tokenize" page.
* In this window you can choose the Token to tokenize the asset with, the available tokens list can be accessed using the drop down arrow.&#x20;
* Once the appropriate token is selected, click on the "Tokenize" button on the bottom of the page.



## Asset Payout

The main utility of tokenized assets is to enable fractional ownership and to share the revenue with the token holders. To send the payout to the token holders the user sends NXS equivalent in value to the revenue generated, to the asset address and it will be automatically be distributed as per the percentage token holdings of each holder.

{% hint style="warning" %}
The payout is distributed taking the maxsupply as 100% of the tokens. If any tokens are still in the token generation address, the percentage of payout corresponding to the balance tokens will be returned to the sender.
{% endhint %}
