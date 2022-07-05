---
description: How to configure the miner
---

# Miner Configuration

The miner configuration is the most critical part and uses the JSON format. This configuration is the same for windows or linux.

{% hint style="info" %}
**NOTE:** Make sure the NexusMiner executable and the miner config are in the same folder
{% endhint %}

The miner configuration is stored in a **`miner.conf`** file, it should be in the same folder as the `NexusMiner` executable.  In windows or linux with UI you can create a text file and save the configuration and save the file as miner.conf.

For linux CLI, use the below commands:

To change into the Miner folder where the NexusMIner executable is available, if it's a different folder change accordingly.

```
cd Miner
```

Create the miner.conf file.

```
nano miner.conf
```

Find below the JSON config files for both prime and hash miners. Copy paste and change the settings as per the setup. Remember that each GPU or FPGA has to be configured as a unique worker. Also make sure the "_wallet\_ip"  "port", "local\_ip", "mining\_mode" and "pool" details are correct._

For Nexus prime and hash pools the payout address will be the identifier to the pool and the  reward payout will be done to the same address. Most pool's have a minimum reward amount to be collected before payout.

{% tabs %}
{% tab title="Prime Pool" %}
```
{
    "version" : 1,
    "wallet_ip" : "primepool.nexus.io",
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
}sh
```
{% endtab %}

{% tab title="Hash Pool" %}
```
{
    "version" : 1,
    "wallet_ip" : "hashpool.nexus.io",
    "port" : 50000,
    "local_ip" : "auto",
    "mining_mode" : "HASH",
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

To save the config file Ctrl+s & Ctrl+x

#### Miner Config Direct Link:

We provide a few standard mining configs, download and configure to suit the setup. Each GPU or FPGA will be configured as a separate worker. (Each core on the CPU will be configured as a worker - Used for solo mining on testnet).&#x20;

Download the config files from the link below:

{% embed url="https://github.com/Nexusoft/NexusMiner/tree/master/example_configs" %}



