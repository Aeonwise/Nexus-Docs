# Asset Using Interface

This guide will help users to create an Asset (NFT) using the Nexus Interface

{% hint style="info" %}
This asset will reside on the Nexus network and will be owned by the user account / sigchain which created it.
{% endhint %}

Open the Nexus Interface, make sure the wallet is fully synched. Log into the user account (sigchain).

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
Naming Convention:\

{% endhint %}

* Use a unique name if creating an asset. Short names are preferred, but if needed use long names.
* If creating an asset of a real world assets like real estate, provide clear and precise information for the Asset Name&#x20;
* If creating a bunch of NFT's say from a single art collection, then suffix the collection name with a unique serial Number series Ex: "_Iron Maiden #0001"_
* __

### Asset Data

This section is for the asset data or metadata. The information provided here helps to give validity to the Asset and its value. The asset data has to be precise, complete and should enable anyone to check authenticity of the asset its backing. The data provided will depend on the digital or physical asset which is being backed as a blockchain Asset. &#x20;

{% hint style="info" %}
Asset data has a limit of 1KB and this is binding. An asset can hold approximately 990 - 995 characters including spaces. This excludes the Asset Name.
{% endhint %}

{% hint style="warning" %}
**Note:** If creating an Asset of a digital art, which basically is an image file, provide a md5 hash of the original image for anyone to check the authenticity of that particular file. If all the details are provided without the file hash, the asset will not be of any use, due to the fact that no one will be able to confirm the authenticity of the file which represents the asset.&#x20;
{% endhint %}

Asset Data is entered in fields which represent a single line in the image above. First column is the  field name and next is the value. Next is the mutable radio button, next is the Type drop down and &#x20;

|          | Bytes | Min - Max Value |
| -------- | :---: | --------------- |
| uint8    |   1   | 0 - 255         |
| unit16   |   2   | 0 - 65535       |
| uint32   |   4   | 0 - 4294967295  |
| unit64   |   8   | 0 -             |
| unit256  |   16  |                 |
| uint512  |   32  |                 |
| uint1024 |   64  |                 |
|          |       |                 |

&#x20;
