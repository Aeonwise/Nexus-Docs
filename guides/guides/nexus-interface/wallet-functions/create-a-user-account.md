---
description: How to create a user account
---

# Create a User Account

Before creating a new user account, the wallet must be fully synchronized with the Nexus network. See [Bootstrap and Synchronize](https://nexus.io/ResourceHub/wallet-guide#bootstrap) if this still needs to be completed.

To create your user account, simply choose a username, password, and PIN.

{% hint style="info" %}
User Accounts on Nexus are also referred as Signature Chains (SigChains)
{% endhint %}

**Username:** It must be at least 3 characters long and it’s case sensitive. Examples: Oliver Queen, Oliver.Queen, oliverqueen. We recommend keeping the username simple, because it is the easiest way to transact on Tritium (username:default will be the address to receive nxs or tokens. Example: Oliver Queen:default).

**Password:** It must be at least 8 characters. It can contain lower and upper case alphabets, numerals from 0-9 and special characters.

**PIN:** It must be at least 4 digits. It can contain alphanumeric and special characters, and can be used as a second password.

{% hint style="danger" %}
**PLEASE DO NOT USE COMMON WORDS FOR YOUR PASSWORD, THIS WILL LEAVE YOU VULNERABLE TO DICTIONARY ATTACKS THAT COULD DRASTICALLY DECREASE THIS RESISTANCE.**

We therefore recommend that you use a secure [random number generator](https://nexus.io/ResourceHub/wallet-guide#random-password-generator) to create your password.
{% endhint %}

![](https://nexus.io/ResourceHub/images/guide/create\_user.png)

When user submits the create new user request, a new confirmation window will appear where the user has to enter the password and pin again, then click "Create Account .

The wallet must complete a small proof of work that may take up to 30 seconds, and then the request to create a new account is sent to the network for confirmation. This will take a minimum of 2 minutes to 5 minutes, be patient.

{% hint style="info" %}
**The new account user cannot log in, until the new account request is processed by the network and is confirmed and written into the blockchain.** &#x20;

Users can see a message on the wallet top left which says the user account is confirmed on the blockchain.
{% endhint %}

Once the user get the confirmation or after 5 minutes the user can log into the user account at-least a couple of times to make sure, everything works perfectly.

{% hint style="warning" %}
The next step is to [Set a Recovery Phrase](set-recovery-phrase.md) for the account. Do not skip this step.&#x20;
{% endhint %}
