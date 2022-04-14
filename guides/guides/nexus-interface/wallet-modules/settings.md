# Settings

There are 4 pages within settings: Application, Core, Style, Modules.

**Application**

**Language:** Select your language of choice. The default language is English.

**Minimize on close:** With this enabled, even though the Wallet disappears, it is still open in the background. To re-open your Nexus Wallet do the following:

* Mac: Click on the Nexus logo in the top right hand corner, and then click ‘Show Nexus Wallet’
* Windows: Double click on the Nexus logo in the bottom right hand corner menu.

With this enabled, your Wallet (node) will still be online; this is therefore advisable. If your Wallet application is closed fully (Minimize on Close setting Disabled), then you will not be in sync with the Nexus Blockchain when you next open the application, and will therefore need to catch up to the current block.

**Auto update:** Rather than having to manually download a new Wallet each time a new update is released, which is a common necessity with many cryptocurrency Wallets, the Nexus Wallet notifies you of an update to be accepted, comparable to regular computer software updates.

Nexus strongly recommend that this setting remains enabled. This setting enabled will automatically check for new versions and notify you if a new version is available. If automatic updates are not enabled, you will be required to manually download the new Wallet version either from github.com/Nexusoft/NexusInterface or our website.

Any Wallet updates will show in a pop up box. These updates must be installed as soon as possible. Not having your Wallet on the newest version update will put your coins at risk, and could mean you are no longer synchronised with the Nexus Blockchain. **Please ensure you update your Wallet as soon as you are notified of an update.**

**Send anonymous usage data:** Send anonymous data usage to allow the Nexus developers to improve the Wallet.

**Base Currency:** The option selected will be the currency in which the Balance, Market Price, Market Cap & 24hr is displayed in. The default currency is USD.

**Minimum Confirmations:** Minimum amount of confirmations before a block is accepted. The minimum number of confirmations is 1, but you can customize how many you require to wait before your Wallet sees the transaction as valid. 3 to 6 confirmations are recommended to maintain high levels of security.

**Backup Directory:** This is where your Nexus Wallet Backups are stored. When you click ‘Backup Wallet’, you are prompted with a dialogue box that allows you to select a custom directory other than the default ‘Nexus Backups’ directory.

**Developer Mode:** Development mode enables advanced features to aid in development. After enabling, the Wallet must be closed and reopened to enable those features

**Core**

**Enable Mining:** When mining is enabled, your Wallet will run a special server called the ‘Mining LLP’, which will allow you to connect an external miner to your Wallet for producing blocks on the Prime or Hash channels.

**Enable Staking:** When Staking is enabled (the default), your Wallet is enabled for Staking and will stake your Trust Account whenever you log in. You must also have ‘Staking Enabled’ in order for your Wallet to receive Trust payments. This is to prevent people from unintentionally Staking coins.

**Verbose Level:** Verbose level for logs shows more under the hood data on the network. We recommend that you run verbose level 0 if you don’t need to see a lot of logging information. If you experience Wallet troubles though, more debug data is important for the developers to use to find bugs and push new releases. Use this setting at your own discretion.

**Style**

**Render Globe:** Turn the globe on or off.

**Overview Display:** Customize the Wallet Display. The options are:

* Standard: The Wallet comes with the globe.
* Miner: Displays Mining metrics, such as Prime, Hash and Stake difficulty.
* Hidden Balance: Hide your NXS, USD, and incoming balances.
* None: Display only the modules and twinkling stars.

**Nexus Address Format:** Format your NXS addresses to your liking. Note, the format (e.g. the 9 spaces in the Segmented style) is NOT copied over when copying an address. This is just for visual preference only. The options are:

* Segmented
* <img src="https://nexus.io/ResourceHub/images/guide/settings1.png" alt="" data-size="original">
* Truncate middle
* <img src="https://nexus.io/ResourceHub/images/guide/settings2.png" alt="" data-size="original">
* Raw
* <img src="https://nexus.io/ResourceHub/images/guide/settings3.png" alt="" data-size="original">

**Theme:**

There are two default themes Dark and Light.

**Background:** We provide two default default backgrounds Twinkling stars and Cosmic Light. You can also upload a custom wallpaper that you have saved on your device.

**Color scheme:** Change the colors to customize your own theme. Upon changing a color in one of the default themes you will see that your ‘Theme’ changes from either Dark or Light to ‘Custom theme’. If you were to then revert back from Custom theme to Dark theme for example, and then back to ‘Custom theme’, you will find that your custom theme has been saved.

**Import Custom Theme:** A variety of custom themes created by the Nexus community can be imported into the Wallet. The below link holds a repository of community made themes. The background can be imported from your local machine, or enter a URL and the Wallet will download the background for you. Acceptable formats are PNG/JPEG/BMP/TIFF/GIF.

**Export Custom Theme:** Themes are Json files that are read by the system and apply changes to the interface. When you export a theme, you will be prompted to save the json file to your computer. Below is a link to the theme guide which describes how to develop themes. If you would like to, please request that your theme is included in the official repository for it to be shared with the community.

**Modules**

Security is very important, and therefore modules are sandboxed to prevent any misuse.

To import a module, simply drag the file into the center of this page.

Module app icons will appear in the bottom menu to the right of the Console icon.

Documentation on how to write modules : [https://github.com/Nexusoft/NexusInterface/tree/master/docs/Modules](https://github.com/Nexusoft/NexusInterface/tree/master/docs/Modules)

We recommend using one of these links as a starting point:

* React-Redux Example: [https://github.com/Nexusoft/react\_redux\_module\_example](https://github.com/Nexusoft/react\_redux\_module\_example)
* React Example: [https://github.com/Nexusoft/simple\_react\_module\_example](https://github.com/Nexusoft/simple\_react\_module\_example)
* HTML Example: [https://github.com/Nexusoft/minimal\_module\_example](https://github.com/Nexusoft/minimal\_module\_example)
