---
description: Guide to setup mining on windows
---

# Mining on Windows

This guide will help to set up mining on Windows. The new NexusMiner makes it very easy to mine on Windows. Nexus has its own open prime mining pool and the developers are working on furthur decentralizing mining.

### Mining Support:

If you have any kind of support related to mining, please do visit our telegram channel linked below:

{% embed url="https://t.me/NexusMiners" %}

## Mining Channels:

* **Prime Mining:** GPU  -Supports both Solo & Pool.
* **Hash Mining:** GPU or FPGA’s - Supports both Solo & Pool.

{% hint style="info" %}
**Good to Know:** Dont recommend CPU Prime or Hash mining as it is not profitable and only used for testnet mining
{% endhint %}

### Solo Mining&#x20;

Solo means single or individual mining. It requires the miner to be connected to the Nexus wallet. The wallet and miner can be run on the same or a separate computer especially when mining with FPGA’s.&#x20;

### Pool Mining

Pool mining is similar to group mining. The miner has to be connected to a mining pool. The miner is directly connect to the pool and the mining rewards are paid to miners depending on the percentage of individual hash rate. There are fees to mine on a pool and that is deducted from the mining payouts.&#x20;

## Mining Pools For Nexus:&#x20;

### Prime Pool:

Only one prime pool available, an open pool run by the Nexus mining developer team. To use this pool copy the below lines in the config

```
    "wallet_ip" : "154.16.159.126",
    "port" : 50000,
```

### Hash Pool:

For hash mining use the third party pools listed below:

* https://hashpool.com/&#x20;
* https://pool.blackminer.com/

### Compatible Mining Hardware

Nexus miner can use only nvidia graphics cards or FPGA's.  Before you proceed make sure to update the graphics card driver to the latest nvidia gaming drivers. (Do not install the content creator drivers)

## Mining Hardware:

The NexusMiner can use CPU, GPU for Prime and FPGA for Hash mining. CPU mining is not recommended as it is not efficient.

Mining Calculator:

To get a better understanding of the mining efficiencies of different hardware, use the mining calculator linked below:

{% embed url="https://primepool.nexus.io/mining_calc" %}

### &#x20;GPU:

If using GPU mining, then the only choice today is CUDA cores from Nvidia and to get the best out of the graphics cores we highly recommend to use the latest graphics drivers and MSI afterburner.&#x20;

{% hint style="warning" %}
Do not install the Nvidia content creator drivers, the miner will not work properly
{% endhint %}

### FPGA:

FPGA miners for Nexus are only available from Blackminer

## Download the Miner:

Download the windows miner executable file from the link below (Not an installer)

{% hint style="warning" %}
The miner cannot run prime and hash at the same time on a single computer
{% endhint %}

{% embed url="https://github.com/Nexusoft/NexusMiner" %}

Create or copy the miner.conf and place it in the same folder as the NexusMiner executable

## Miner Configuration:&#x20;

The miner configuration is the most critical part and uses the JSON format.&#x20;

{% hint style="info" %}
**NOTE:** Make sure the NexusMiner executable and the miner config are in the same folder
{% endhint %}

We provide a few standard mining configs, download and configure to suit the setup. Each GPU or FPGA will be configured as a separate worker. (Each core on the CPU will be configured as a worker - Used for solo mining on testnet). Download the configs from the links below

{% embed url="https://github.com/Nexusoft/NexusMiner/tree/master/example_configs" %}

Find below the JSON config files. Copy, paste and change the settings as per setup. Remember that each GPU or FPGA has to be configured as a unique worker. Also make sure the "_wallet\_ip"  "port", "local\_ip", "mining\_mode" and "pool" details are correct._

For pool mining the _N_exus payout address will be the identifier to the pool and the block reward payout will be done to the same address. Most pool's have a minimum reward amount to be collected before payout.

{% tabs %}
{% tab title="Prime Pool" %}
```
{
    "version" : 1,
    "wallet_ip" : "154.16.159.126",
    "port" : 50000,
    "local_ip" : "auto",
    "mining_mode" : "PRIME",
    "pool" :
    {
        "username" : "<INSERT_HERE NXS ADDRESS>",
        "display_name" : "<INSERT HERE>"
    },
    "stats_printers" :
    [
        {
            "stats_printer" :
            {
                "mode" : "console"
            }
        }
    ],
    "workers" : 
    [
        {
            "worker" :
            {
                "id" : "myWorker0",
                "mode" : 
                {
                    "hardware" : "gpu",
					"device" : 0
                }
            }
        }
    ]
}
```
{% endtab %}

{% tab title="Hash Solo" %}
```
{
    "version" : 1,
    "wallet_ip" : "127.0.0.1",
    "port" : 9325,
    "local_ip" : "127.0.0.1",
    "mining_mode" : "HASH",
    "connection_retry_interval" : 5,
    "get_height_interval" : 2,
    "ping_interval" : 10,
    "log_level" : 2,
    "logfile" : "miner.log",
    "stats_printers" :
    [
        {
            "stats_printer" :
            {
                "mode" : "console"
            }
        },
        {
            "stats_printer" :
            {
                "mode" : "file",
                "filename" : "stats.log"
            }
        }
    ],
    "print_statistics_interval" : 10,
    "workers" : 
    [
        {
            "worker" :
            {
                "id" : "myWorker0",
                "mode" : 
                {
                    "hardware" : "gpu",
                    "device" : 0
                }
            }
        },
        {
            "worker" :
            {
                "id" : "myWorker1",
                "mode" : 
                {
                    "hardware" : "gpu",
                    "device" : 1
                }
            }
        },
        {
            "worker" :
            {
                "id" : "myWorker2",
                "mode" : 
                {
                    "hardware" : "gpu",
                    "device" : 2
                }
            }
        } 
    ]
}
```
{% endtab %}

{% tab title="Hash Pool" %}
```
{
    "version" : 1,
    "wallet_ip" : "nxs.pool.blackminer.com",
    "port" : 9012,
    "local_ip" : "auto",
    "mining_mode" : "HASH",
    "pool" :
    {
        "username" : "<INSERT_HERE NXS ADDRESS>",
        "use_deprecated" : true
    },
    "stats_printers" :
    [
        {
            "stats_printer" :
            {
                "mode" : "console"
            }
        }
    ],
    "workers" : 
    [
        {
            "worker" :
            {
                "id" : "myWorker0",
                "mode" : 
                {
                    "hardware" : "fpga",
					"serial_port" : "<INSERT HERE>"
                }
            }
        }
    ]
}
```
{% endtab %}
{% endtabs %}

## Nexus Desktop Wallet:

### Nexus Interface:

Download and install the Nexus Interface wallet or setup the CLI core.&#x20;

Start the wallet, create the user, login and unlock the wallet for mining and notifications.

### Nexus Interface:

1. Go to settings > Core > Enable mining by clicking on the toggle button next to it.&#x20;
2. A new field below will pop out below:  Mining IP Whitelist. enter the  `<ipaddress:port>` of the miner. If mining on the same computer then enter `127.0.0.1:9325`,  if the miner is running on another computer or FPGA then enter the particular `ipaddress:9325`. If there are more than one miner then use ‘; ’to separate the IP addresses. Wildcards ‘_’ are supported for IP addresses only ex:192.168._.\*:9325.

![](<../../.gitbook/assets/Screenshot 2022-01-10 at 6.03.56 PM.png>)

### Wallet Daemon or CLI:

If using the wallet core then add a line `llpallowip=<ipaddress:port>` in the nexus.config for each miner. Use 127.0.0.1:9325 for mining on the same computer or the ipaddress:9325 for a separate miner.

Restart the core for the changes to take effect

## Run the Miner

Go to the folder where the NexusMiner executable and miner.conf are located, double click on the NexusMiner executable. A confirmation window will pop up, click run and the miner will start in a terminal.

{% hint style="info" %}
**NOTE:** For the miner to work the user has to be logged in and unlocked for mining and notifications
{% endhint %}


