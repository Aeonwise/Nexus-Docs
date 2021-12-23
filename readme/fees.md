# Fees



| Action                                          | Cost | Note                                                                                                                                                                                                                                                                                   |
| ----------------------------------------------- | ---: | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sending NXS or other tokens                     |    0 |                                                                                                                                                                                                                                                                                        |
| Receiving NXS or other tokens                   |    0 | If the debit being credited has contract conditions, a fee may apply for executing those conditions depending on their complexity. A fee-free threshold for conditions means that simple contract conditions such as adding an expiry to a debit will mean crediting them will be free |
| Transferring assets (NFTs) and other registers  |      |                                                                                                                                                                                                                                                                                        |
| Claiming ownership of assets or other registers |      | If the register being claimed is a named register, i.e. there exists a local name for it in the previous owners signature chain, then a corresponding local name is created for it when claiming. This name creation attracts a 1 NXS fee                                              |
| Creating a NXS or token account                 |      | The fee is calculated based on the size of data stored in the register at 0.001 NXS per byte. However there is a minimum fee of 1 NXS and (at the time of writing) a maximum register size of 1Kb, meaning the fee will vary between 1 an 1.024 NXS.                                   |
|                                                 |      |                                                                                                                                                                                                                                                                                        |
|                                                 |      |                                                                                                                                                                                                                                                                                        |







If the transfer being claimed has contract conditions, a fee may apply for executing those conditions depending on their complexity. A fee-free threshold for conditions means that simple contract conditions such as adding an expiry to a transfer will mean claiming them will be free



0

If the account is given a name, there is a 1 NXS fee applied for the creation of the name register.

Creating an asset or other register

1+

The fee is calculated based on the size of data stored in the register at 0.001 NXS per byte. However there is a minimum fee of 1 NXS and (at the time of writing) a maximum register size of 1Kb, meaning the fee will vary between 1 an 1.024 NXS.

Updating an asset or other register

0

Nexus has a fees intergated for the various functions or facilities provided. The fee is a deterrent so that the network is not spammed, prevent hoardingCreating a local name

1

Creating a global name

2000

Creating a namespace

1000

Creating a token

1+

The fee calculation for creating a token is based on the number of total supply of token divisible units, which in turn is calculated from the token supply and the number of decimals in the token definition. For example, a token with supply 1,000,000 and 2 decimals has a total of 100,000,000 divisible units. The actual fee calculation is a logarithmic scale based on this number, using the formula:

Fee = (log10(divisible units) – 2) \* 100

A minimum fee of 1 NXS always applies. This yields the following fees based on number of divisible units

100 = 1 NXS\
1,000 = 100 NXS\
100,000 = 300 NXS\
1,000,000 = 400 NXS\
1,000,000,000 = 700 NXS\
1,000,000,000,000 = 1000 NXS

Transaction Fee

0-1 NXS

A transaction fee is applied whenever a transaction is created within 10 seconds of the last transaction within a signature chain. The fee is calculated based on the number of contracts within the transaction at a rate of 0.01 NXS per contract, of which there can be a maximum of 100 (at the time of writing). Therefore the transaction fee will be between 0 and 1 NXS.

The transaction fee is applied in addition to any of the other fees described in this table.
