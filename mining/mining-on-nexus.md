# Mining on Nexus

This guide will help to set up mining. Mining helps secure the network and Nexus has two mining channels prime and hash. The new nexus miner makes it very easy to mine on Windows. Nexus does not have its one mining pool as of now and developers are working on building an open pool.

{% hint style="warning" %}
The miner cannot run prime and hash at the same time on a single computer
{% endhint %}

## Mining Channels:

* **Prime Mining:** GPU  -Supports both Solo & Pool &#x20;
* **Hash Mining:** GPU or FPGA’s - Supports both Solo & Pool&#x20;

{% hint style="info" %}
**Good to Know:** Dont recommend CPU Prime or Hash mining as it is not profitable and only used for testnet mining
{% endhint %}

### Solo Mining&#x20;

It requires the miner to be connected to the Nexus wallet. The wallet and miner can be run on the same or a separate computer especially when mining with FPGA’s.&#x20;

### Pool Mining

The miner is directly connect to the pool.&#x20;

&#x20;Mining Pools For Nexus Mining:&#x20;

As of today you can mine only on two pools for hash mining. The pools are https://hashpool.com/ https://pool.blackminer.com/

The Nexus miner can use only nvidia graphics cards or FPGA's. FPGA setup is out of the scope of this guide Before you proceed make sure to update the graphics card driver to the latest nvidia gaming drivers. (Do not install the content creator drivers)

Miner Configuration: The miner configuration is the most critical part and it uses JSON format. This guide will provide a few miner configs which you can download and configure to suit your system. Each GPU will be configured as a separate worker. Each core on the CPU will be configured as a worker.

Links to sample config files: Solo prime miner with CPU Solo prime Miner with GPU Solo prime Miner with CPU+GPU Solo hash Miner with CPU - for testnet only Solo hash Miner with GPU/FPGA Pool hash Miner with GPU/FPGA

Solo MIning Prime or Hash:

Download the windows miner from the link below (Not an installer)

https://github.com/Nexusoft/NexusMiner

Create the miner.conf and place it in the same folder as the NexusMiner executable

Copy the below code in the miner.conf file and change the required fields to suit your configuration. In the configuration “wallet\_ip” is the IP address of the wallet and “local\_ip” is the IP address of the miner. Save the file and if using notepad make sure it does not suffix it with the .txt extension.

{ "wallet\_ip" : "127.0.0.1", "port" : 9325, "local\_ip" : "127.0.0.1", "mining\_mode" : "HASH", "connection\_retry\_interval" : 5, "get\_height\_interval" : 2, "use\_pool" : false, "pool" : { "username" : "" }, "logfile" : "miner.log", "stats\_printers" : \[ { "stats\_printer" : { "mode" : "console" } }, { "stats\_printer" : { "mode" : "file", "filename" : "stats.log" } } ], "print\_statistics\_interval" : 10, "workers" : \[

```
    {
        "worker0" :
        {
            "id" : "hash0",
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

Start the wallet. Go to settings > Core > enable mining by clicking on the toggle button next to it. For the MiningIpWhitelist provide the IPaddress:port of the miner. If mining on the same computer then enter 127.0.0.1:9325 or if the miner is running on another computer or FPGA then enter the particular ipaddress:9325. If there are more than one miner then use ‘; ’to separate the Ip addresses. Wildcards ‘_’ are supported for IP addresses only ex:192.168._.\*:9325.

If using the wallet core then add a line ”llpallowip=[ipaddress:port](ipaddress:port)” in the nexus.config for each miner. Use 127.0.0.1:9325 for mining on the same computer or the ipaddress:9325 for a separate miner.

In the wallet log in to the user account used for mining.

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
