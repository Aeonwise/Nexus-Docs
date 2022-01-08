# Page 1

**Modular Wallet Design:**

Nexus wallet includes modular functionality consisting of the interface, module framework and core. The intuitive interface provides users and businesses an easy and seamless experience. A node can also be run as a daemon exclusively with management available via API or remote interface. This is advantageous when running a staking node on a headless system like a Raspberry Pi or NUC.

**Computer Requirements:**

The daemon is tested and works flawlessly on a Raspberry Pi 3B+ with 1GB Ram, but the minimum recommendations are as follows to account for growth:

**ARM:** The Raspberry Pi 4B with 2GB RAM or equivalent SBC with 2GB with a min of 64GB SD card (Daemon /CLI on Linux only).

**x64:** Any processor with 4GB RAM. Make sure that you have at least 30GB free hard disk space before you install the wallet.

**Note:** The full node will download the complete copy of the blockchain database and as of today the extracted database is about 12.5GB in size and grows over time. Lite nodes will only maintain block headers and signature chain data minimizing the storage impact dramatically, 250MB approximately.

**Economical Implementations and IoT:**

The PoS fundamental principle is securing the network, and for that it provides an incentive. Node operators incur expenses with the hardware, management, bandwidth and electricity. The instructions in this section provide an optimal configuration for strict budgets and the IoT industry.

**Average Users (GUI Wallet):** Any computer which meets the minimum requirements, If staking is the only service planned an Intel NUC core i3 / Ryzen 3 or equivalent with 4GB RAM and 120GB SSD is recommended. If the staking computer will be used for other purposes, increase memory and disk space appropriately.

**Advanced Users (CLI Wallet):** RPI 4 with 2/4GB, NUC or equivalent will run the headless core and control it via an interface from an alternate computer. (RPI can run only the CLI daemon so command line interaction is necessary. Nexus has great step-by-step guides to aid those who are unfamiliar.)

![](https://nexus.io/ResourceHub/images/guide/stake-guide1.png)

Nexus wallet daemon staking on a RPi 4 takes just 243 MB of RAM and is extremely resource conservative overall.

**Operating System:**

All major Operating Systems (OS) are supported , but the community recommended OS is Ubuntu LTS or derivatives. Any Linux distribution can be used however the guides have been tailored for Ubuntu.
