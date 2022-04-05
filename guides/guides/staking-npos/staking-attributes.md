---
description: Understanding Staking Attributes
---

# Staking Attributes

If staking using the Interface the overview will show the staking attributes on the right side of the interface. It includes stake rate, block weight, trust weight and stake weight. For CLI users use the API finance/get/stakeinfo to get the stake information.

![](https://nexus.io/ResourceHub/images/guide/stake-guide2.png)

**Stake Rate:** This is the annual incentive percentage of your total stake. It begins at 0.5% p.a. and increases non-linearly to a max of 3% p.a. in a year (1% in a month, 2% in 6 months, and 3% in a year).

**Block Weight:** This starts with the genesis transaction at 0%, then begins climbing slowly to 100% within 72 hours, once a new block is staked the block weight resets to zero and then the cycle starts again.

**Trust Weight:** Trust is representative of cumulative time spent staking, though it can decay if your node doesn't mine a block within 72 hours of the previous one. It starts at 1.1% and increases to 100% when staking continuously for a year. Trust extends beyond 100%.

**Stake Weight:** Stake weight is a product of block and trust weights, and the higher this weight, the higher chance of staking a block.
