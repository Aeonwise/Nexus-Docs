---
description: Guide to setup mining on windows
---

# Mining on Windows

This guide will help to set up mining on Windows. The new nexus miner makes it very easy to mine on Windows. Nexus does not have its one mining pool as of now and developers are working on building an open pool.

{% hint style="warning" %}
The miner cannot run prime and hash at the same time on a single computer
{% endhint %}

### Mining Support:

If you have any kind of support related to mining, please do visit our telegram channel linked below:

{% embed url="https://t.me/NexusMiners" %}

## Mining Channels:

* **Prime Mining:** GPU  -Supports both Solo & Pool &#x20;
* **Hash Mining:** GPU or FPGA’s - Supports both Solo & Pool&#x20;

{% hint style="info" %}
**Good to Know:** Dont recommend CPU Prime or Hash mining as it is not profitable and only used for testnet mining
{% endhint %}

### Solo Mining&#x20;

Solo means single or individual mining. It requires the miner to be connected to the Nexus wallet. The wallet and miner can be run on the same or a separate computer especially when mining with FPGA’s.&#x20;

### Pool Mining

Pool mining is like group mining. The miner has to be connected to a third party pool miner, there are open pools also. The miner is directly connect to the pool and the mining rewards are paid to miners depending on the percentage of individual hash rate. There are fees to mine on a pool ans that is deducted from the mining payouts/&#x20;

## Mining Pools For Nexus:&#x20;

Prime Pool:

This pool is an open pool run by the Nexus mining developer team. To use this pool copy the below lines in the config

```
    "wallet_ip" : "154.16.159.126",
    "port" : 50000,
```



As of today you can mine only on two pools for hash mining. The pools are:

* https://hashpool.com/&#x20;
* https://pool.blackminer.com/

### Compatible Mining Hardware

Nexus miner can use only nvidia graphics cards or FPGA's.  Before you proceed make sure to update the graphics card driver to the latest nvidia gaming drivers. (Do not install the content creator drivers)

{% hint style="warning" %}
Do not install the Nvidia content creator drivers, the miner will not work properly
{% endhint %}

## Miner Configuration:&#x20;

The miner configuration is the most critical part and uses JSON. This guide will provide a few miner configs which you can download and configure to suit your system. Each GPU will be configured as a separate worker. Each core on the CPU will be configured as a worker.

Links to sample config files: Solo prime miner with CPU Solo prime Miner with GPU Solo prime Miner with CPU+GPU Solo hash Miner with CPU - for testnet only Solo hash Miner with GPU/FPGA Pool hash Miner with GPU/FPGA

Solo MIning Prime or Hash:

## Setup the Miner:

Download the windows miner executable file from the link below (Not an installer)

{% embed url="https://github.com/Nexusoft/NexusMiner" %}

Create or copy the miner.conf and place it in the same folder as the NexusMiner executable

{% embed url="https://github.com/Nexusoft/NexusMiner/tree/master/example_configs" %}

{% tabs %}
{% tab title="Prime Solo" %}
```
// Some code
```
{% endtab %}

{% tab title="Prime Pool" %}
```
// Some code
```
{% endtab %}

{% tab title="Hash Solo" %}
```
// Some code
```
{% endtab %}

{% tab title="Hash Pool" %}
```
// Some code
```
{% endtab %}
{% endtabs %}

## Nexus Desktop Wallet:

### Nexus Interface:

Download and install the wallet.

Start the wallet.&#x20;

Go to settings > Core > Enable mining by clicking on the toggle button next to it.&#x20;

Now you see an additional field below Mining IP Whitelist. Enter the  `<ipaddress:port>` of the miner. If mining on the same computer then enter `127.0.0.1:9325`,  if the miner is running on another computer or FPGA then enter the particular `ipaddress:9325`. If there are more than one miner then use ‘; ’to separate the IP addresses. Wildcards ‘_’ are supported for IP addresses only ex:192.168._.\*:9325.

### Wallet Daemon or CLI

If using the wallet core then add a line `llpallowip=<ipaddress:port>` in the nexus.config for each miner. Use 127.0.0.1:9325 for mining on the same computer or the ipaddress:9325 for a separate miner.

In the wallet log in to the user account used for mining.

## Run the Miner

Go to the folder where the NexusMiner executable and miner.conf are located, double click on the NexusMiner executable. A confirmation window will pop up, click run and the miner will start in a terminal.

Pool MIning Hash:

Download the windows miner from the link below (Not an installer)

https://github.com/Nexusoft/NexusMiner

Create the miner.conf and place it in the same folder as the NexusMiner executable

Copy the below code in the miner.conf file and change the required fields to suit your configuration. In the configuration “wallet\_ip” is the pool DNS, port is the pool port and “local\_ip” is the local IP address and not the public IP address of the miner. Make sure to enter your Nexus wallet address to receive pool payouts in the pool username field. Save the file and if using notepad make sure it does not suffix it with the .txt extension.

{ "wallet\_ip" : "nxs.stratum.hashpool.com", "port" : 9012, "local\_ip" : "192.168.1.118", "mining\_mode" : "HASH", "connection\_retry\_interval" : 5, "get\_height\_interval" : 2, "use\_pool" : true, "pool" : { "username" : "Nexus address to receive payouts" }, "logfile" : "miner.log", "stats\_printers" : \[ { "stats\_printer" : { "mode" : "console" } }, { "stats\_printer" : { "mode" : "file", "filename" : "stats.log" } } ], "print\_statistics\_interval" : 10, "workers" : \[

```
    {
        "worker" :
        {
            "id" : "hash1",
            "mode" : 
            {
                "hardware" : "gpu",
				"device" : 0
            }
        }
    }
]
```

} This is a sample config file

The nexus payout address will be the identifier to the pool and the block reward payout will be done to the same address. Most pool's have a minimum reward amount to be collected before payout.

Go to the folder where the NexusMiner executable and miner.conf are located, double click on the NexusMiner executable. A confirmation window will pop up, click run and the miner will start in a terminal.
