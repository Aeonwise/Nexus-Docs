---
description: All information on the TAO Naming System
---

# Naming System TAO

## Names and Namespaces

Names and Namespaces are special kinds of object registers that are used as locators to other object registers in the blockchain. When an object register is first created (an asset for example) the caller can provide a name for the register. If a name is provided then a Name object register is also created with its register address based on a hash of the name. The Name object also has a address field, which is populated with the register address of the register (asset, token, account etc) that the Name "points" to. In this way, objects can be retrieved by name by first hashing the name to get the Name object's address, retrieving the Name object, and then using the address stored within it to retrieve the object register. A Name then, is best thought of as a named index to object registers.

The TAO Naming System (TNS) allows Name objects to be created in one of three different contexts, or namespaces - `local`, `namespaced`, and `global`. Names must be unique within the namespace in which it was defined.

## NAMES:

Local Names are those created within the context of a signature chain. To use a local name you must prefix the name with the owners username separated by a single colon, e.g. `bob:savings`. This is equivalent to saying "look at all the Names registered in the sig chain `bob` and find one called `savings` and then see what object register it points to". There can only be one Name called `savings` in the sig chain `bob`, but another user `alice` can also create a local name called `savings`

## NAMESPACE:

Namespaces allow users to provide user-friendly names for their object registers without needing to disclose their username. This is useful for privacy, but also to allow names to be related to a business or some other meaningful context. To avoid name-squatting registering a namespace  attracts a high fee (`1000 NXS`). However once registered, creating Names within that namespace costs only `1 NXS`

### Namespaced:

Names that are created within the context of a namespace are called as Namespaced, which itself is a globally unique keyword. To use a namespaced name you must prefix the name with the namespace separated by a double colon, e.g. `bobscoffeeshop::payments`. In this example bob would have first registered the namespace `bobscoffeeshop` and created an account to receive payments to (which could be called anything). He then creates a Name with a `name=payments`, `namespace=bobscoffeeshop` and `address=(register address of the account)`. From then on, anyone can use the name `bobscoffeeshop::payments` and it will resolve to the register address of the account.

## GLOBAL NAMES:

Global Names require no username or namespace prefix, and are therefore globally unique. These will be likely reserved for use cases where a succinct, unique, name is necessary, for example a token ticker symbol. To avoid needless name-squatting, global names attract a high fee (`2000 NXS`).

The Names API allows callers to access and manage both Names and Namespaces. Names can be created to "point" to any register address you wish, whether the caller owns the register or not. This is useful, for example, if somebody gives you the register address of a NXS account to receive payments and you wish to add a friendly Name for it for future use.

Namespaces can be transferred to other signature chains, opening the possibility for a secondary market to buy and sell namespaces (similar to internet domain names).

Global Names and Names that have been created within a namespace can also be transferred to other signature chains. Local names cannot be transferred.

In the future when safenet, the decentralised internet is born, namespace can be used as a domain name.
