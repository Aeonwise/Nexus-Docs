---
description: Mining on Linux computer.
---

# Mining on Linux

Mining on Linux is not straightforward like windows and the user has to compile the NexusMiner from source. This guide will help you setup mining on Linux. This guide is tailored for Ubuntu and Debian based distributions.

{% hint style="info" %}
Make sure you install the latest GPU drivers from the manufacturer. Driver installation is outside the scope of this guide.
{% endhint %}

## Prepare Ubuntu for Miner:&#x20;

Install the dependencies

```
sudo apt install build-essential libboost-all-dev libdb-dev libdb++-dev libssl-dev libminiupnpc-dev libgmp-dev -y 
```

Ubuntu does not have the latest version of boost. The install will be a manual process listed below:

### Install Boost

This below is a direct link to the boost website:

{% embed url="https://www.boost.org/users/download#live" %}

Download the latest version of boost. At the time of writing the latest version boost is 1.78.0:

```
wget https://boostorg.jfrog.io/artifactory/main/release/1.78.0/source/boost_1_78_0.tar.gz
```

Extract boost installer to a new directory named Boost.

```
tar xzvf boost_1_69_0.tar.gz -C ~/Boost
```

Change into the Boost folder

```
cd Boost
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

Nexus miner uses the latest version of cmake  and Ubuntu does not ship with the latest version of cmake. If  the distro has cmake version lower than 3.19, then follow the steps below to install latest version of cmake manually.

Go to the cmake downloads page (link below) and download the linux cmake script files with .sh extension

{% embed url="https://cmake.org/download" %}

Change into the folder where the file is downloaded

```
cd Downloads
```

Run the installer

![](https://lh6.googleusercontent.com/9FU6gF8E6ij0g0gNkuYbuG-7IG7IaypFe\_oKBTi4DUXocjKkKckEHrQLRDMFXscUVmvDuDmM-kKywvYzqNeb1F6xiBo-48uUPovFe10xyO2V57ctc8vB\_\_r81XApwWsRmpIpBkJ6tG7cqFV5-Q)

![](https://lh4.googleusercontent.com/KeXuGqp8Qe4uSpiQ8MTJFlctZcrVGEHUBQzK90ioKSwwiaV7VLbnnuy0I9-kkMLmZT4xwdhwbwL63J1tqFyYhCMb5E-eVmt2fRQ1qN0PdWNmMKZupIu5xGuAobsmnjYLwoIvrkyqWhD4BWrhuA)

```
./<cmakefilename.sh>
```

First will be the licence, use “Enter” to scroll down or “spacebar” to scroll to the end, accept licence and then accept the location to extract, which will install the cmake binary. Change into the cmake/bin folder. Change the cmake folder name accordingly

Cmake is installed and ready for the next step.

## Download and Compile NexusMiner

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

Change into the cmake/bin folder installed in the step above. At time of writing the cmake version is 3.21.2, change the name accordingly.&#x20;

```
cd /Downloads/cmake-3.21.2-linux-x86_64/bin/
```

Run cmake to build the NexusMiner executable. \<pathtosource> is the path to the NexusMiner folder and \<pathtobuildfolder> is the path to NexusMiner/build. Use the option `"-DWITH_PRIME=On"` to include for prime mining support during compile.

```
./cmake -S <pathtosource> -B <pathtobuildfolder> -DCMAKE_BUILD_TYPE=Release -DWITH_PRIME=On
```

```
./cmake -S ~/NexusMiner -B ~/NexusMiner/build -DCMAKE_BUILD_TYPE=Release -DWITH_PRIME=On
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

## Miner Configuration:&#x20;

To configure the miner, check the link below:&#x20;

{% content-ref url="../../mining/miner-configuration.md" %}
[miner-configuration.md](../../mining/miner-configuration.md)
{% endcontent-ref %}

## Run the Miner:

To run the miner change into the miner directory.

{% hint style="info" %}
For solo mining start the wallet, login and then start the miner.
{% endhint %}

```
cd NexusMiner
```

```
./NexusMiner
```

Hope you enjoyed the guide!!
