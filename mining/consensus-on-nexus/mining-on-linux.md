# Mining on Linux

{% hint style="danger" %}
This guide is in the works and not completed.
{% endhint %}

Mining on Linux is not straightforward like windows and the user has to compile the NexusMiner from source. This guide will help you setup mining on Linux. This guide is tailored for Ubuntu

## Prepare Ubuntu for Miner:&#x20;

Install the dependencies

```
sudo apt install build-essential libboost-all-dev libdb-dev libdb++-dev libssl-dev libminiupnpc-dev libgmp-dev -y 
```

Ubuntu does not have the latest version of boost and libgmp-dev. The install will be a manual process listed below:

This below is a direct link to the boost website:

{% embed url="https://www.boost.org/users/download#live" %}

Download the latest version of boost. At the time of writing the latest version boost is 1.78.0:

```
wget https://boostorg.jfrog.io/artifactory/main/release/1.78.0/source/boost_1_78_0.tar.gz
```

Extract boost installer to a new directory named Boost.

```
tar xzvf boost_1_69_0.tar.gz -C~/Boost
```

Install boost

```
./bootstrap.sh --prefix=/usr/
```

Compile boost from source.

```
./b2
```

Copy the compiled files to the location specified with "_**–prefix**_ command line option.

```
sudo ./b2 install
```

To verify boost version:

```
./get_boost_version
```

### Install Cmake:

Nexus miner uses the latest version of cmake. Ubuntu does not have the latest version of cmake. If  the distro has cmake version lower than 3.19, then follow the steps below to install latest version of cmake manually.

Go to the cmake downloads page (link below) and download the linux cmake script files with .sh extension

{% embed url="https://cmake.org/download" %}

Change into the folder where the file is downloaded

```
cd Downloads
```

Run the installer

```
./<cmakefilename.sh>
```

First will be the licence, use “Enter” to scroll down or “spacebar” to scroll to the end, accept licence and then accept the location to extract, which will install the cmake binary. Change into the cmake/bin folder. Change the cmake folder name accordingly

### Download and Compile NexusMiner

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

Change into the cmake/bin folder

```
cd cmake-3.21.2-linux-x86_64/bin/
```

Run cmake to build the NexusMiner executable. \<pathtosource> is the path to the NexusMiner folder and \<pathtobuildfolder> is the path to NexusMiner/build. Use the option `"-DWITH_PRIME=On"` to include for prime mining support during compile.

```
./cmake -S <pathtosource> -B <pathtobuildfolder> -DCMAKE_BUILD_TYPE=Release -DWITH_PRIME=On
```

Cmake will build the prebuilt make binaries and keep them in prebuilt binaries folder "/build". Change into build folder.

```
cd ~/NexusMiner/build 
```

To compile use:

```
make
```

This will compile and create the NexusMiner executable.&#x20;



Create a folder for the NexusMiner.&#x20;

```
mkdir ~/Miner
```

Copy the NexusMiner to the _`"Miner`  f_older

```
cp NexusMiner ~/Miner
```

## Configuring the Miner:&#x20;

For the proper functioning of the miner, it needs to be configured; create a configuration file named miner.conf in the same folder as the executable.&#x20;

cd NexusMiner/build Create the miner.conf file&#x20;

```
cd ~/Miner
```

```
nano miner.conf 
```

Copy the miner configuration given below to the file, it uses the JSON format. Change the settings as per needs. The mainnet will use the port 9325 as default. This config uses four workers, for a testnet just one worker can get the job done.

```
"wallet_ip" : "primepool.nexus.io", 
"port" : 50000,
```

To save the config file Ctrl+s & Ctrl+x

## Run the Miner:

To run the miner change into the miner directory



Hope you enjoyed the guide!!
