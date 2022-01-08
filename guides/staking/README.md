# Staking

## **Before You Consider Staking on Nexus**

* Staking on Nexus requires commitment to adequately secure the network and receive the highest possible incentive percentage. Your wallet must remain online 365/24/7.
* Staking on Nexus is based on incentivization and if the node becomes unavailable to the network, the incentives halt immediately. Stake rate and trust also decay with time at a 3:1 ratio (A year of trust decays fully in 4 months, however trust is accumulated beyond 100% so decay timeline can be extended).
* Staked NXS are locked in a trust account and a block must be found to withdraw (a few hours to months), depending on the amount of NXS staked and associated difficulty. For every user the wallet creates two standard accounts named ‘default’ and ‘trust’.
* Staking can only be enabled with NXS in the ‘trust’ account. (Don't send NXS you don't intend to stake to the ‘Trust’ account, use ‘default’ instead).
* When withdrawing NXS from a staking account, there will be a penalty in the form of lost trust proportional to the percentage withdrawn. If trust is accumulated beyond 100%, the amount of trust lost will decrease correspondingly.
* The Staking computation requirements may change with time as adoption accelerates.
* The Nexus wallets, infrastructure and frameworks will be continuously evolving so maintaining updated software is crucial, especially during hard forks. Please join our social media channels to keep abreast of ongoing developments.

{% hint style="info" %}
Staking on Nexus is similar to running a full node
{% endhint %}

### **Additional Staking Resources**

In addition to the thorough guide below, we encourage readers to take a look in the video tutorials folder below and at the following links:

* The Staking section of our FAQs.
* The Glossary to learn more about staking specific terms.

The videos below are brought to you by [The Digital Future!](https://www.youtube.com/channel/UC1lMk6jKYv4lg6gs1oS\_OYw)

An introduction to Nexus Staking:

This guide is intended to demystify trust-based staking and provide clarification on Nexus’ specific centralization safeguards. The significance of this consensus power shift to staking cannot be overemphasized, especially considering the vulnerable state of governance with emerging decentralized ecosystems.

Nexus trust based Proof of Stake (PoS) is a greener form of mining supplying similar consensus properties that Proof of Work (PoW) channels provide with minimal management overhead. The probability of finding a block is largely determined by the amount of coins staked. It is hardware agnostic, instead basing its hashing algorithm off balance and weight. This means there is no set amount of time to earn a reward. It happens when you stake a block, with the chances of doing that increased by staked amount/Stake weight and decreased by current network PoS channel difficulty.

Ultimately, the only thing that matters is that the wallet (node) finds a block once every 72 hours to keep growing stake rate. The reward itself is based on time, so frequency isn't important. If it takes 2 days then the reward is twice as much as if it takes one day. Once you stake a block then that node is locked for 240 blocks (120 min).

In PoW, if network hash rate increases, so does difficulty; similarly for PoS, more total coins staked on network = more difficulty. You can increase PoW hash rate by adding hardware, however hardware makes no difference for PoS. Effective PoS hash rate is increased by stake weight (block and trust weights) and staked amount.

True stake rewards, however, are not like earning interest. Staking rewards are given for running a node to secure blocks via consensus, similar to PoW rewards although generated differently.

Nexus has a total of 78 million native coins and these will be mined fully in 2024 with a tail end emissions / inflation of 3.67%. 3% will be for the PoS if all the nexus tokens are staked and 0.67% for the hash and prime mining channels.

Nexus provides desktop wallets for windows, mac and Linux. The mobile wallet (lite node only) is currently in public beta and will be released in Q1 of 2021. As of today, Nexus only supports full-node staking, although the next major upgrade will also include pooled staking using a lite node with a minimum balance of 1 NXS.

Nexus staked holdings will also be valuable for voting in the upcoming DAO, where trust will be an crucial factor. Voting will supply weight/age values to trust and amount of staked NXS, providing considerable resistance against manipulation and bad actor influences.. Note: In the previous election conducted for Nexus embassy allocation, the amount of nxs for each vote was capped at 10K nxs + trust weight. This is currently not hard coded, but will be implemented in the upcoming DAO release. The threshold variables can be changed as per the requirement and also can be voted on by the community.

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

Nexus wallet daemon staking on a RPi 4 takes just 243 MB of RAM and is extremely resource conservative overall.

**Operating System:**

All major Operating Systems (OS) are supported , but the community recommended OS is Ubuntu LTS or derivatives. Any Linux distribution can be used however the guides have been tailored for Ubuntu.

**Stake Rate:** This is the annual incentive percentage of your total stake. It begins at 0.5% p.a. and increases non-linearly to a max of 3% p.a. in a year (1% in a month, 2% in 6 months, and 3% in a year).

**Block Weight:** This starts with the genesis transaction at 0%, then begins climbing slowly to 100% within 72 hours, once a new block is staked the block weight resets to zero and then the cycle starts again.

**Trust Weight:** Trust is representative of cumulative time spent staking, though it can decay if your node doesn't mine a block within 72 hours of the previous one. It starts at 1.1% and increases to 100% when staking continuously for a year. Trust extends beyond 100%.

**Stake Weight:** Stake weight is a product of block and trust weights, and the higher this weight, the higher chance of staking a block.

Approximately 25-30K NXS (For full node only at the time of writing).

The minimum threshold varies every few minutes as staking difficulty changes. The only way to know for sure is to start staking. If no blocks are found within a reasonable time, add more NXS to trust balance and adjust the staking amount. This is the equivalent of adding more Graphics Processing Units (GPUs) to a PoW mining rig. The minimum amount is an estimation, a ballpark approximation depending on community participation and ecosystem adoption. Additional clarification is provided below:

* Nexus staking incentive is a product of the total number of staking NXS and node trust (elapsed time spent securing the network).
* When the node starts staking, trust is minimal. For example, 20K NXS is sent to a trust account, after the coin matures for 72 hours, it takes a few days to generate a genesis which is your first stake transaction that locks your NXS in the trust account.
* The node may not be able to stake the next block before 72 hours (Block Weight = 100%). Don’t be alarmed, continue staking and over time the duration between new stake blocks decreases, and a block may be found within the 72 hour deadline.
* Remain persistent, continue staking at least for 3 months, before you decide to quit (if you wait longer your chances increase). In the meantime the stake amount can be increased.

The Nexus wallet is enabled for staking by default. No setting adjustments are required initially.

Go to the “Settings” module on the bottom, click on the “Core” tab and locate the toggle button to enable/disable staking. (Follow highlighted icons & text in image below).

Staking can be stopped or started from the “User” module at the bottom bar. Click the “Staking” tab on the left, then find the “Stop Staking” button on the right. Once selected the core will restart and activate the “Start Staking” button.

​Send the staking coins to the trust account. (All unstaked NXS should remain in the default account).

NXS coins need to age 72 hrs in the trust account for staking to start. If any additional coins are sent between the 72 hour aging window, the timer will reset to the beginning.

After 72 hours the wallet attempts to find a block and depending upon the number of NXS in the account, a genesis transaction is initiated, which locks the stake amount in a trust account. Genesis is the start of your staking journey.

To increase the incentive from 0.5% to 3% (stake rate) the wallet must stake a block (mine a block) within 72 hours of the previous stake block. (Block weight = 100%).

Staking must occur continuously in order to increase the stake rate to 3%; This is attained after persistent staking for a year, and thereafter to maintain it.

The incentive earned is accrued in the trust account under “Available Balance” and will not be added to the stake. Accrued incentives can be withdrawn without penalties.

As the node is left unattended most of the time, please remain vigilant and verify activity at least every few days, this can be accomplished with a block explorer as well. Remember, if the node stops staking for whatever reasons the trust and stake rate will decay at a 3:1 ratio.

Send the additional NXS to the trust account.

Go to the “User” module at the bottom, click on “Staking” tab on the left. On the right it shows the staking details. Find the NXS under “Available Balance”, click “Adjust stake Amount” and select the total NXS to be staked. For example, you have 20K NXS already staked and would like to add 5K then, the adjusted amount should be 25K. Click ‘Set staking amount “ to save the changes.

The changes will be reflected in the stake details and on the next stake block the NXS will be transferred to the trust account.

**Note:** ‘Stop Staking’ is not the same as unstake. Staked coins are locked in a trust account and will not be available until properly unstaked.

* To unstake, go to the “User” module at the bottom, click on “Staking” tab on the left. On the right, it shows you the staking details.
* Click "Adjust stake Amount", and enter the amount to keep staking. For example, the wallet is staking 25K NXS and there is a need to remove 10K, then enter 15K. If the entire balance needs to be withdrawn, enter 0. Click "Set staking amount" to save the changes.
* The changes will be reflected in the stake details, continue staking and on the next stake block the NXS will be unlocked and available in the trust account under "Available Balance".
* The unstaked NXS can now be sent to another account. If you have withdrawn your entire balance then you can stop staking.
