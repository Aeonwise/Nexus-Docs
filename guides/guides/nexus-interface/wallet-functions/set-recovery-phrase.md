---
description: Set Recovery Phrase
---

# Set Recovery Phrase

## Recovery Phrase

The recovery system is designed to protect accounts in the case that credentials are lost or stolen. Think of it like a backup, to ensure that users don’t lose access to their Nexus assets.&#x20;

{% hint style="danger" %}
NOTE:

* WE STRONGLY RECOMMEND THAT EVERY USER ACCOUNT HAS A RECOVERY PHRASE ENABLED. ****&#x20;
* FAILURE TO SET A RECOVERY PHRASE MAY LEAD TO PERMANENT LOSS OF YOUR NEXUS ASSETS.
{% endhint %}

### **Step 1: Open Recovery Dialogue**

Click the user icon in the top right hand corner of the Wallet, and select 'Set recovery phrase'.

![](https://nexus.io/ResourceHub/images/guide/recovery1.png)

### **Step 2: Enter Login Credentials**

PLEASE NOTE: YOUR PASSWORD AND PIN ARE REQUIRED WHEN SETTING UP A RECOVERY PHRASE. Enter your credentials as you do when you are logging into your Wallet.

![](https://nexus.io/ResourceHub/images/guide/recovery2.png)

### **Step 3: Generate Recovery Phrase**

Click the link titled 'Generate a recovery phrase'. You can select either 10, 20 or 100 words for your recovery phrase. We recommend using at least 20 words for better security.

![](https://nexus.io/ResourceHub/images/guide/recovery3.png)

{% hint style="warning" %}
**NOTE:**&#x20;

BEFORE PROCEEDING, ENSURE THAT YOU HAVE WRITTEN DOWN YOUR RECOVERY PHRASE. WE RECOMMEND WRITING IT ON PHYSICAL MATERIAL, SUCH AS PAPER, TO ENSURE IT IS SAFELY STORED OFFLINE. WE RECOMMEND MAKING MORE THAN ONE COPY OF YOUR RECOVERY PHRASE.
{% endhint %}

### **Step 4: Submit Recovery Phrase**

Click the button labeled 'Set recovery phrase' to generate your recovery phrase.&#x20;

{% hint style="info" %}
THIS PROCESS CAN TAKE UP TO 30 SECONDS TO COMPLETE. DO NOT CLOSE YOUR WALLET UNTIL THIS COMPLETES.
{% endhint %}

Once your phrase has been setup, you will see a confirmation prompt:

![](https://nexus.io/ResourceHub/images/guide/recovery4.png)

To confirm that it was set up properly, you can go to your transaction module, to check the most recent transaction.

![](https://nexus.io/ResourceHub/images/guide/recovery5.png)

This shows the contract that updated your recovery phrase, which uses the primitive OP::WRITE.

## **Forgot your Password?**

In order to change your password with your recovery phrase, you will need to click the link 'Forgot Password' at the bottom of the login page.

![](https://nexus.io/ResourceHub/images/guide/recovery6.png)

A dialogue box will open to submit your username, recovery phrase, new password and PIN.

![](https://nexus.io/ResourceHub/images/guide/recovery7.png)

Users will then gain access to their account again! If you are extra paranoid, you can test recovering your account after you set it up (while using the same password) to make sure that everything is working as it should.

The recovery system works by using a special next hash, called the 'recovery hash' that allows the user to reset their password and PIN without needing account credentials.

As always, stay safe, be vigilant, and PLEASE set up your recovery phrase!
