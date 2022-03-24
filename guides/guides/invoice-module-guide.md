# Invoice Module Guide

## **What is the Invoice Module?**

The Invoice DApp module is an initial and essential step in the evolution of decentralized finance (DeFi), supply chains and similar blockchain use cases being built on Nexus. We envision the Nexus invoice system to not only streamline payments and reduce the costs of administration within an organization, but across businesses and between industries.

This module is a downloadable add-on for the Nexus wallet. All invoices are recorded on the blockchain and only transferred to the debtor once settled, providing a transparent record for auditing or legal purposes. A time expiration for the invoice contract can also be specified if required.

**How do I get it?**

This guide provides details on how to install the Nexus Invoice System module, create a new invoice, and pay an invoice. Screenshots from the current Nexus wallet along with descriptions provide users with the knowledge required to use this fairly simple module for accounting tasks on the Nexus network.

Download the Nexus Invoice Module tar.gz from the Github link below.&#x20;

{% embed url="https://github.com/Nexusoft/Nexus-Interface-Invoice-Module/releases" %}

The Module section of the Nexus wallet is accessible via the top _Settings_ menu or gears icon on the bottom. Choose the _Modules_ section within the _Settings_ screen. The following screenshot shows the _Modules_ section without any modules installed.

As the instructions on the screen indicate, installing a module is as simple as dragging a module's archive file (e.g., _tar.gz_ archive file) into the field on the screen. Instead of the archive file, you can also download the zip file, extract it, and drag it into the same field on the screen.

Upon dragging the invoicing module’s archive file onto the screen depicted above, the following prompt is displayed. If everything is as expected (e.g., the module hash matches that listed on the github repository), click the _Install Module_ button to begin installation.

The following prompt is presented to indicate that the module has been successfully installed. Upon dismissing this prompt, the wallet will be restarted.

Now, as a result of installing the invoicing module, it is included in the list of installed modules, and the toggle button indicates that the module is active.

{% hint style="info" %}
Note: The invoice module adds a new icon to the extreme right of the module icons located  at bottom of the wallet.
{% endhint %}

![](../../.gitbook/assets/Invoice.png)



Running the Nexus Invoice System is as simple as clicking on the icon at the bottom of the wallet screen which was added when the module was installed. The first time the module is run, the Nexus Invoice System is displayed with an empty list of invoices. On subsequent review after creating invoices, this is where they will be listed.

Before getting into the creation of invoices, it is worth noting that the _More options_ dropdown displayed above reveals additional fields with which invoices can be searched, as shown in the screenshot below. These fields include _Description_, the _Payable_ account, the _Recipient_ identifier (e.g., the username for a SigChain), and a toggle to cause only past due invoices to be displayed.

### Create New Invoice:

To create a new invoice, click the +_New Invoice_ button shown in the above screenshot. The following screen is displayed where details comprising this invoice are entered. These details include _Description_, _Reference_ (typically used to tie an invoice and payment to an accounting ledger item), _Number_ (used to help identify particular invoices), and _Due Date_.

![](<../../.gitbook/assets/New Invoice.png>)

In the _From_ group of fields, the _Account Payable_ information for this invoice is specified, which is used to indicate which account within the sender’s SigChain will receive the funds once paid. In addition, the _Sender Details_ for this invoice can be specified, for instance, to include the human-readable name of the person being paid in this invoice.

The following screenshot shows the dropdown in the _From_ section which lists the accounts to where the funds for this invoice could be paid. Choose one from the list.

The next screenshot shows in the _To_ section, the _Recipient_ field is filled out. This field takes the username or hash of the SigChain that will be paying this invoice. Below that, in the _To_ section, _Recipient Details_ could be included such as the human-readable name associated with the paying SigChain (if the hash is being used to identify the SigChain).

Further down on the invoice screen, the _Items_ section holds the specific elements being invoiced. In the example shown below, the recipient is being invoiced for laptop upgrade items: memory, an SSD, and labor. For each item, the unit cost in NXS is provided, as is the number of units being invoiced. The module multiplies these to get the _Total_ for each item. It also totals all items to show the _Total_ for this invoice at the bottom right. The total is listed in NXS and the currency configured to be shown in the wallet (in this case USD).

Note that the invoice screen has two buttons at the bottom of it: _Submit_ and _Save As Draft_. Next to the _Submit_ button the fee in NXS for submitting the form is displayed.

{% hint style="info" %}
A invoice fee of 1 NXS is deducted from the "`default`"account on submit&#x20;
{% endhint %}

The following screenshot shows the invoice saved as a draft. Note that at this point, the _Reference_ does not display. However, draft invoices can be displayed by selecting _DRAFT_ from the _Status_ dropdown at the top of the invoice module.

Upon clicking the _Submit_ button to send an invoice to the recipient, the following prompt is presented to enter the PIN for the SigChain from which the invoice is being sent.

After submitting an invoice, it displays in the list of invoices with a _Status_ of OUTSTANDING. Note that this is how the invoice will be displayed to both the sender and receiver.

### Cancel Invoice:

If the sender wants to cancel the invoice, they should open the invoice and click the _Cancel_ button. A prompt to enter the sender’s SigChain PIN will be presented, and after entering the PIN, the invoice will be marked CANCELLED.

### Pay Invoice:

To pay the invoice, the receiver clicks on the invoice in the list of invoices (as displayed above). The following prompt will be displayed.

Clicking the _Pay_ button presents a prompt allowing the payer to choose an account from their SigChain from which the invoice will be paid. The dropdown on this prompt lists all available accounts from which the payer can choose.

After selecting the payment account, the payer clicks the _Pay with this Account_ button to indicate their designation. A confirmation prompt, shown below, is presented to validate the payer’s intention to fulfill this invoice.

As a final confirmation and authentication, when the payer clicks the Yes button (above) to indicate their confirmed intention to fulfill the invoice, they are presented with a prompt to enter their SigChain’s PIN.

Finally, the invoice is marked PAID. The screenshot below depicts what displays in both the sender’s and receiver’s list of invoices in the invoice module.

The following screenshot shows from the receiver’s perspective the transaction resulting from paying the invoice. The screenshot was taken before any blockchain confirmations of the transaction had been applied.

The ensuing screenshot shows both the invoice creation transaction (the lower one with the FEE deducted) and the transaction in which the sender has been paid.
