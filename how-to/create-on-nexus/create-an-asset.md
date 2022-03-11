---
description: Create Asset using the Interface
---

# Asset Using Interface

This guide will help users to create an Asset (NFT) using the Nexus Interface

Open the Nexus Interface, make sure the wallet is fully synched. Log into the user account (Sigchain).

In the Overview page, at the bottom click on the "_User"_ module. This opens the User page.

&#x20;In the User page, on the left side click on the "_Assets_" tab.

In the Assets page click on "Create a new asset". This opens the Create a new asset page.

{% hint style="info" %}
Creating an Asset has a fee of 1 NXS and "_Asset Name"_ has a fee of 1 NXS. Total cost of an Asset with Name will be 2 NXS
{% endhint %}

Here you have two main sections "Asset Name" and "Asset Data".

### Asset Name

This is a globally unique name for the asset. Duplicate names will not be allowed. If creating a bunch of  assets with a similar name then use a serial no with the name.&#x20;

{% hint style="info" %}
Asset Name has a separate fee of 1NXS. Users can opt not to create an Asset Name and can use the register address to access or search the Asset.
{% endhint %}

{% hint style="info" %}
Naming Convention:

* Use a unique name if creating an asset. Short names are preferred, but if needed use long names.
* Names can contain upper lower case letters, numbers and special characters.
* If creating an asset of a real world assets like real estate, provide clear and precise information for the Asset Name&#x20;
* If creating a bunch of Assets / NFT's, say from a single art collection, then suffix the collection name with a unique serial Number series Ex: "_Iron Maiden #0001"_
{% endhint %}

* Use a unique name if creating an asset. Short names are preferred, but if needed use long names.
* If creating an asset of a real world assets like real estate, provide clear and precise information for the Asset Name&#x20;
* If creating a bunch of NFT's say from a single art collection, then suffix the collection name with a unique serial Number series Ex: "_Iron Maiden #0001"_

### Asset Data

This section is for the asset data or metadata. The information provided here helps to give validity to the asset and its value. The asset data has to be precise, complete and should enable anyone to check authenticity of the asset its backing. The data provided will depend on the digital or physical asset which is being backed as a blockchain Asset. &#x20;

{% hint style="info" %}
Asset Data has a limit of 1KB and this is binding. An asset can hold approximately 990 - 995 characters including spaces. This excludes the Asset Name.
{% endhint %}

{% hint style="warning" %}
**Note:** If creating an Asset of a digital art, which basically is an image file, provide a md5 hash of the original image for anyone to check the authenticity of that particular file. If all the details are provided without the file hash, the asset will not be of any use, due to the fact that no one will be able to confirm the authenticity of the file which represents the asset.&#x20;
{% endhint %}

Asset Data is entered in fields which represent a single line in the image above.&#x20;

#### Name:&#x20;

The first column is the field name, which is the name for the data you are going to add like Description, Owner, Artist, Hash etc.

#### Value:&#x20;

The second column is the value of the field, like the owner's name

#### Mutable:

Third is the radio button to enable mutable field (default is disabled). Mutable fields can be changed anytime by the sigchain owner of the asset. This is very helpful in case you have a house minted as an Asset and once you sell the house, transfer the asset to the new owner and he can change the "Owner" field to his name.

{% hint style="info" %}
Only make the fields mutable which really need. Ex When creating a asset which refers to a house, The "Owner" field needs to be mutable, this is due to the  where as Location, Name, Registration No&#x20;
{% endhint %}

#### Type:

String: It is a data type used to represent text. It is comprised of a set of characters that can also contain spaces and numbers. For example, the word "hamburger" and the phrase "I ate 3 hamburgers" are both strings. Even "12345" could be considered a string.&#x20;

Date types uint8, uint16, uint32, uint64, uint128, uint256, uint512 and uint1024 represents an unsigned integer number stored with 8, 16, 32 or 64 bit.&#x20;

|       Type | No of Bits | Min - Max Value                |
| ---------- | :--------: | ------------------------------ |
| uint8      |      1     | 0 - 255                        |
| unit16     |      2     | 0 - 65535                      |
| uint32     |      4     | 0 - 4,294,967,295              |
| unit64     |      8     | 0 - 18,446,744,073,709,551,615 |
| unit256    |     16     | 0 - 2^256-1                    |
| uint512    |     32     | 0 - 2^512-1                    |
| uint1024   |     64     | 0 - 2^1024-1                   |

Max Length:

This field is enabled only if the field is selected as mutable and the type is selected as "string". This is important as this will allow to limit the length of the field when it's changed later and to contain the Asset Data within the 1 KB limit.

#### Add Another Field

To add another field click on the "+ADD FIELD" button below the first field.

#### Remove Field

To remove a field hover the mouse pointer on that field, a "x" icon will appear on the left side of the field, click on it to remove the field.

### Create the Asset

Once all the asset name and data is filled, at the bottom you can see the estimated cost to mint this asset.

ON the bottom of the page click on "Create Asset" which will save mint the asset on the blockchain and dedect the fees

{% hint style="info" %}
The fees will be deducted automatically from the "default" account, make sure that you have NXS to cover the fees or it will fail to mint the asset.&#x20;
{% endhint %}

Once the asset is minted you will see a new entry in the "Assets" page.

{% hint style="info" %}
This asset will reside on the Nexus network and will be owned by the user account which created it.
{% endhint %}
