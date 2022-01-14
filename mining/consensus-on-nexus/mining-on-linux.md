# Mining on Linux

Mining on Linux is not straightforward like windows and the user has to compile the NexusMiner from source. This guide will help you setup mining on Linux. This guide is tailored for Ubuntu

## Compile the Miner:&#x20;

Install the dependencies (Only required if installing miner on a separate computer)

```
sudo apt install build-essential libboost-all-dev libdb-dev libdb++-dev libssl-dev libminiupnpc-dev libgmp-dev -y 
```

Clone the NexusMiner repository&#x20;

```
git clone --depth 1 https://github.com/Nexusoft/NexusMiner 
```

```
git clone --branch v1.4 https://github.com/Nexusoft/NexusMiner
```

Change into the source code folder&#x20;

```
cd NexusMiner 
```

To precompile the source code use cmake. (cmake version 3.19 or higher only) \<pathtosource> is the path to the NexusMiner folder and \<pathtobuildfolder> is the path to NexusMiner/build

```
cmake -S <pathtosource> -B <pathtobuildfolder> -DCMAKE_BUILD_TYPE=Release
```

To change into the prebuilt binaries folder

```
cd build
```

&#x20;To compile use:&#x20;

```
make 
```

This will create the NexusMiner executable.&#x20;

## Cmake Problems&#x20;

Nexus miner uses the latest version of cmake, if the system has a version lower than 3.19, then do the following Go to the cmake downloads page (link below) and download the linux cmake script files with .sh extension

{% embed url="https://cmake.org/download" %}

Change into the folder where the file is downloaded

```
cd Downloads
```

Run the installer

```
./<cmakefilename.sh>
```

cmake install

cmake install complete&#x20;

First will be the licence, use “Enter” to scroll down or “spacebar” to scroll to the end, accept licence and then accept the location to extract, which will install the cmake binary. Change into the cmake/bin folder. Change the cmake folder name accordingly

```
cd cmake-3.21.2-linux-x86_64/bin/
```

Run cmake. is the path to the NexusMiner folder and is the path to NexusMiner/build&#x20;

```
./cmake -S <pathtosource> -B <pathtobuildfolder> -DCMAKE_BUILD_TYPE=Release
```

cmake building the prebuilt make binaries To change into the prebuilt binaries folder&#x20;

```
cd ~/NexusMiner/build 
```

To compile use:&#x20;

```
make
```



NexusMiner compiling This will create the NexusMiner executable.&#x20;



## Configuring the Miner:&#x20;

For the proper functioning of the miner, it needs to be configured; create a configuration file named miner.conf in the same folder as the executable.&#x20;

cd NexusMiner/build Create the miner.conf file&#x20;

```
nano miner.conf 
```

Copy the miner configuration given below to the file, it uses the JSON format. Change the settings as per needs. The mainnet will use the port 9325 as default. This config uses four workers, for a testnet just one worker can get the job done.



To save the config file Ctrl+s & Ctrl+x

This is a sample miner.config with one worker&#x20;

## Run the Miner:

For the miner to mine blocks, a user account is to be created, logged in and unlocked for mining, this also works to bootstrap a new network. Create two separate user accounts for the two nodes. Start the wallet. Wait for a few min for the wallet to be loaded: cd LLL-TAO ./nexus If a user account is not configured, auto create and auto login in the wallet configuration, then create an user account, login and unlock for mining. To create a new user account: ./nexus users/create/user username= password= pin= Login to the user account: ./nexus users/login/user username= password= pin= Unlock the user account for mining: ./nexus users/unlock/user pin= mining=1 notifications=1

Wallet started, create a user account , login and unlock for mining Start the miner: cd NexusMiner ./NexusMiner

Miner started with one worker - Blocks Accepted Check the messages the miner prints out, every 10 secs there is a miner statistics printed on the screen (Time set in miner.config). Check for the “Submitting Block ...” and “Block Accepted By Nexus Network”

Warning- Block Rejected By Nexus Network In the image above check the “Submitting Block ...” and “Block Rejected By Nexus Network” Stop the miner: Ctrl+c

Wallet- Check the mining info To check the mining information on the wallet: ./nexus ledger/get/info - 5.1.0-rc1 and above ./nexus ledger/get/mininginfo - Below 5.1.0-rc1 To check the total wallet balance of the logged in user account: ./nexus finance/get/balances To check the account details of the logged in user account: ./nexus finance.list/accounts In account details the newly minted testnet coins are shown in the balance. These can be transferred similar to main net coins to other users for testing purposes.

This is the two wallets and miners running side by side Hope you enjoyed the guide!!
