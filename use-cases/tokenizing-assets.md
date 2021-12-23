# Tokenizing Assets

### Tokenizing Assets

**What Does Tokenizing An Asset (NFT) Mean?**

Simply put, tokenizing an asset means to digitally represent the value and ownership credentials of a real world asset in a secure and easily transferable manner on the internet using blockchain technology. We refer to this digital representation of data as a token.

Nexus utilizes [Signature Chains](broken-reference) (SigChains) technology to simplify the creation of tokenized assets and validate ownership on the Nexus blockchain. Once created, a token (and all the value & rights associated with it) can be easily transferred from one SigChain to another (or in other words, from person to person). In other words, if we transfer ownership of an example real estate property to a token called, for instance, "Ownership\_1020\_Greengate\_Dr\_Columbia\_SC\_29229", and the amount of that token is 100, the token can serve as a percentage of ownership in the property. So, someone buying in 10% ownership in the property would receive, in exchange for their money, 10 of the ownership tokens. Alternatively, if someone purchased 50% ownership in a self portrait asset, they would receive half of the available tokens associated with the asset, which might be called "Ownership in Self Portrait".

**Why Tokenize An Asset?**

For the purposes of this article, there are two primary reasons for tokenizing an asset. First, it can store asset ownership permanently by the person who owns the tokens. For the self portrait asset, this percentage ownership can be made accessible via DApp created for the purpose of reporting high-value asset ownership. Second, it can automatically distribute revenue associated with the asset to the owners according to the allocated percentages. In the case of our fictitious real estate property, when the occupant pays the rent, 10% of the rent paid will be automatically transferred to the signature chain which owns 10% of the "Ownership..." token for this asset. This can be done with NXS (the cryptocurrency itself) or with a fungible token that the owners of the property agree to accept as rental proceeds, using the same mechanism used to send NXS or a token to any other address on the Nexus network.

Briefly, an asset is a user-definable entity that is recorded on a SigChain. Examples of assets used for this article include a) a real estate property and b) a high-value work of art. On the blockchain, a real estate property asset might be represented with fields containing a tax identifier, a URL to a deed, and a hash used to verify the integrity of the deed file.

`assets/create/asset name=1020_Greengate_Dr_Columbia_SC_29229`\
`parcelID=R19908-04-06`\
`documentURL=http://richlandcountysc.gov/documents/deeds/12-3456789.pdf`\
`documentMD5=d3d767fe83507c80c182660a8ccb87fe`

For the high-value work of art, one might represent the asset with fields containing the artist, creation date, a URL to a certificate of authenticity, and a hash to verify the integrity of that certificate file.

`assets/create/asset name=Self Portrait artist=Neal Helman`\
`creationDate=20200909`\
`certificateURL=http://certificate-of-authenticity-for-artwork.com/certificates/NSH05-09082020.pdf`\
`documentMD5=e3e767fd00207c80c234660a8ccb63fd`

Rest assured that the above examples are purely fictional. The assets and documents referenced do not exist. The [API calls](https://github.com/Nexusoft/LLL-TAO/tree/master/docs/API), however, exemplify how you might create an asset from the console in the Nexus wallet. This guide will also look at how one would use the wallet to do the same things demonstrated here with the console and API calls. It is anticipated that someone will create a DApp that will allow such assets to be created in a more industry-appropriate manner.

The following screenshot shows the location in the wallet to create an asset. On the _User_ screen, in the _Assets_ tab, click the _Create new asset_ button to begin creating a new asset.

The next screenshot shows the fields filled in for the real estate asset. Note that none of the fields are numeric, so they are all _string_ types, and none of them can be changed in the future meaning their _mutable_ buttons are turned off. Upon scrolling to the bottom of this screen, one will see the button for submitting the fields and creating the asset. The user PIN for the SigChain is required in order to confirm the creation of the asset.

As mentioned previously, two tokens will have to be created for the purpose of tokenizing our two fictitious assets. The API calls below show how one might create these two tokens, with the assumption being that we only need 100 tokens to represent percentage ownership. For this example, fractional percentage ownership of up to four decimal places can be used (e.g., 5.1200%). Of course, one would provide the proper PIN for the SigChain on which the tokens are being created.

`tokens/create/token pin=1234`\
`name=Ownership_1020_Greengate_Dr_Columbia_SC_29229`\
`supply=100`\
`decimals=4`

`tokens/create/token pin=1234`\
`name=Ownership in Self Portrait`\
`supply=100`\
`decimals=4`

The following screenshots shows the corresponding process using the wallet of creating the token representing ownership in the real estate asset. First, on the _User_ screen, go to the _Tokens_ tab. There you will see the _Create new token_ button.

This screenshot demonstrates the filled fields for the real estate asset’s ownership token. The supply is set at 100 to easily represent percentage amounts, and by allowing 4 decimal places, someone might have 45.5123% ownership in the asset. Note that with this supply parameter, the fee for creating this token is currently 400 NXS. Click the _Create token_ button to submit the form fields and create the token.

The formula for calculating the fee for creating a token is (log10(TotalSupply) - 2) \* 100 NXS, with a minimum of 1 NXS. TotalSupply is the number of divisible token units, so, in our case 100 tokens divisible into 4 decimal places is 1,000,000 divisible units. Thus, 400 NXS to create this token.

After creating the token, the wallet prompts to create an account. This isn’t a requirement unless the SigChain (in this case, bobby.walsh) will also be represented in the ownership of the asset.

Now that the assets and tokens have been created, the asset can be tokenized. The following API calls illustrate how this might be done from the Nexus wallet console.

`assets/tokenize/asset pin=1234`\
`name=1020_Greengate_Dr_Columbia_SC_29229`\
`token_name=Ownership_1020_Greengate_Dr_Columbia_SC_29229`

`assets/tokenize/asset pin=1234`\
`name=Self Portrait token_name=Ownership in Self Portrait`

Note that, as with most of the API calls, the asset and token addresses can be used as an alternative to the names that are used in the example above. Here is what it looks like when these API calls are issued from the wallet’s console.

Once the assets have been tokenized, the tokens can be distributed to the owners in their allotted percentages. Note that to participate in the ownership of the assets, the SigChain on which the assets and tokens were created will also need accounts for the tokens used to tokenize the assets, and will also need tokens sent to those accounts.

The next screenshots demonstrate the process of creating an account for the token just used to tokenize the real estate asset. The account is being created on the SigChain of _claudia.hush_, who we will then give 45% ownership of the real estate asset to.

First, Claudia needs to look up the token for which she will create the account. The lookup function is on the _User_ screen in the _Tokens_ tab. At the top right of the tab is a _Lookup a token_ button. Clicking that button displays the following input where she can enter the fully-qualified name (e.g., including the SigChain) of the token representing ownership in the real estate asset. The _Lookup this token_ button retrieves the token information from the blockchain.

Here we see that Claudia has found the token. She can now create the token account on her SigChain by clicking the _Create new account with this token_ button. On the resulting prompt, she confirms to create the account.

Now that the SigChains of the owners have accounts for the tokens with which the real estate asset was tokenized, the owner of the token (e.g., _bobby.walsh_) can transfer a percentage of tokens to the accounts in order to represent partial ownership. This includes a token account on his own SigChain as well as a token account on the SigChain of _claudia.hush_. The following screenshot demonstrates Bobby transferring 45 tokens (45% ownership in the real estate asset) to Claudia’s token account.

After transferring the remaining tokens to his own token account, the following screenshot reflects that Bobby now owns 55% ownership in the real estate asset.

Once Claudia’s 45% ownership in the tokenized asset is represented by her SigChain’s possession of 45 of the tokens used to tokenize the asset, she qualifies for 45% of the revenue paid to the asset. For our example, a third entity, _harry.twilight_ is paying rent on the real estate asset, in this case 100 NXS. In addition to NXS, he could have paid with any fungible token residing on the Nexus blockchain. As seen below, Claudia receives 45 NXS from Harry’s payment of 100 NXS (topmost CREDIT transaction). The second topmost transaction shows where Claudia received the 45 tokens representing her ownership stake in the real estate asset.
