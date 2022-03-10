---
description: All about the NVM
---

# Nexus Virtual Machine

The Nexus Virtual Machine (NVM) is a **`state machine`** and exists as one single entity maintained by hundreds of connected Nexus nodes.

The Nexus software stack exists solely for the purpose of keeping the continuous, uninterrupted, and immutable operation of this special state machine; it's the environment in which all Nexus Accounts and Advanced contracts live. At any given point in the chain, Nexus has one and only one **`canonical`** state, and the NVM is what defines the rules for computing a new valid state from block to block.

Even though all smart-contract platforms are state machines, the obsession to be scalable for real world usage, culminated in the distinct architecture of NVM. To easily distinguish the better architecture, it was imperative to name contracts on Nexus as Advanced contracts. Below we will unravel the architecture.

### NVM Architecture

The NVM is designed as a "`64 bit"`, "`register based`; this design was chosen as it matches the CPU's 64 bit and mimics the CPU cache registers.

This design makes the NVM very fast compared to EVM as it's designed for the processors of today. To put it in numbers, EVM takes 1.7 million nanoseconds/instruction and NVM takes 33 nanoseconds/instruction. EVM is at a huge disadvantage as it takes 4 cycles to complete an instruction due to its 256 bit length on a 64 bit CPU and also its dated stack design.

The NVM is designed intentionally not to be turing complete, this decision also stems from the fact the Nexus is a **`Verification`** engine. This design has a huge upside and that is free simple transactions, while EVM needs Gas to control computation requests due to bad code, which can grind the network to a halt. With the NVM design advanced contracts will have predictable fees which will be calculated before contract execution.

Nexus will have different types of contracts, for the higher level API's, templates will be provided, which a user can choose from a dropdown list. For advanced users augmented contracts will empower them to use contracts with their choice of domain specific language. Augmented contracts will be available at a later date. For more details refer the [roadmap](https://nexus.io/roadmap)
