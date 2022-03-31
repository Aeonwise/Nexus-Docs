# LX-OS

**The Foundation: seL4**

![](../../.gitbook/assets/Sel4.webp)

Nexus has finally settled upon the seL4 (secure L4) microkernel as a foundation for NexOS. The seL4 microkernel branches from the L4 family of microkernels. This family has enjoyed significant commercial success (including billions in mobile phone sales) and adoption in critical systems around the world ([2](https://en.wikipedia.org/wiki/L4\_microkernel\_family)).&#x20;

Released in 2009 by the [Trustworthy Systems group](http://ts.data61.csiro.au), seL4 focuses on critical systems such as military applications such as drones and satellites. Its core innovation comes from the guarantees in isolation properties between applications and unique approaches to kernel resource management. Specifically, seL4 led the world of operating systems by becoming the first formally verified general purpose microkernel (proofs are limited to only a few instruction sets such as ARM).

Formal verification involves transforming a code’s specification into mathematical abstractions, then constructing proofs to “prove” that the implementation follows the specification ([3](https://www.sciencedirect.com/science/article/pii/S1405774314706596)). Some describe formal verification as proving that bugs can’t occur, but this is imprecise, especially in complex systems where unknown inputs exist.&#x20;

For consumer applications which may be designed for other operating systems, seL4 runs a hypervisor which allows the virtualization of another OS (windows linux, etc.), however a consumer level use implementation of the NexOS won't occur until IoT use cases exhibit success. Overall, SeL4 provides Nexus developers an extremely stable, proven and innovative microkernel to serve as the cornerstone for NexOS.&#x20;
