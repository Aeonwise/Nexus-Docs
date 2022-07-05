---
description: Guide to setup mining on windows
---

# Mining on Windows

This guide will help to set up mining on Windows. The new NexusMiner makes it very easy to mine on Windows. Nexus has its own open prime mining pool and the developers are working on further decentralizing mining.

## Download the Miner:

Download the windows miner executable file from the link below (Not an installer)

{% hint style="warning" %}
The miner cannot run prime and hash at the same time on a single computer
{% endhint %}

{% embed url="https://github.com/Nexusoft/NexusMiner" %}

## Miner Configuration:&#x20;

To configure the miner, check the link below:&#x20;

{% content-ref url="mining-on-nexus/miner-configuration.md" %}
[miner-configuration.md](mining-on-nexus/miner-configuration.md)
{% endcontent-ref %}

## Nexus Desktop Wallet:

{% hint style="info" %}
This is only for solo miners. Pool miners can skip this step&#x20;
{% endhint %}

### Nexus Interface:

Download and install the Nexus Interface or setup the CLI core.&#x20;

Start the wallet, create the user, login and unlock the wallet for mining and notifications.

#### Mining Settings on Interface:

1. Go to settings > Core > Enable mining by clicking on the toggle button next to it.&#x20;
2. A new field below will pop out below:  Mining IP Whitelist. enter the  `<ipaddress:port>` of the miner. If mining on the same computer then enter `127.0.0.1:9325`,  if the miner is running on another computer or FPGA then enter the particular "`ipaddress:9325`. If there are more than one miner then use ‘; ’to separate the IP addresses. Wildcards ‘_**\*’** are supported for IP addresses only ex: 192.168.10.\*:9325._

### Nexus Core

If using the Nexus core then add a line `llpallowip=<ipaddress:port>` in the nexus.config for each miner. Use 127.0.0.1:9325 for mining on the same computer or the ipaddress:9325 for a separate miner.

Restart the core for the changes to take effect

{% hint style="info" %}
**Good to Know:** For solo mining to work, the user has to be logged in and unlocked for mining and notifications.
{% endhint %}

## Run the Miner

Go to the folder where the NexusMiner executable and miner.conf are located, double click on the NexusMiner executable. A security warning window will pop up (shown in image below), click run and the miner will start in a terminal. The miner will run and start mining which you can see from the messages on the miner terminal window. There is no user interaction required.&#x20;

![](../.gitbook/assets/Miner61.png)

To check if everything is working, go to the mining pool page link below, on the header right side, paste the Nexus address entered in the miner.conf file in the search box and click on search. This will open a page like below, where you can see the details of your miner.&#x20;

{% embed url="https://primepool.nexus.io/overview" %}
**Prime Pool Miner Website**
{% endembed %}

![Mining Details for Each Miner](../.gitbook/assets/Miner7.png)

## Stop the Miner

To stop the miner close the NexusMiner terminal window.

## Screenshots

![miner.conf for prime pool with 1 GPU](../.gitbook/assets/Miner31.png)

![NexusMiner v1.4 Prime Pool mining with single GPU](../.gitbook/assets/Miner1.png)

![NexusMiner v1.4 Prime Pool mining with single GPU](../.gitbook/assets/Miner2.png)

![miner.conf for prime pool with 1 GPU & 2 CPU cores](../.gitbook/assets/Miner41.png)

![NexusMiner v1.4 Prime Pool mining with single GPU and two CPU Cores](../.gitbook/assets/Miner5.png)
