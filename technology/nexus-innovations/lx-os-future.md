# LX-OS (Future)

Nexus is building the next generation decentralised internet which will be connected by a decentralized infrastructure. To power the satellites which are critical to the decentralised infrastructure setup there is a need for a secure Operating System (OS) and none of the OS existing today are suitable to power the decentralised internet of the future.

Due to these limitations Nexus has no other choice than to create a new OS which is a perfect fit to power the decentralized infrastructure, IoT and even desktop of the future.&#x20;

### **LX-OS**

LX-OS, the Nexus Operating System will initially run on micro-satellites and IoT (Internet of Things) devices, which generally have weak security models. LX-OS will drive the [Nexus Protocol](https://nexus.io/files/nexus\_protocol/Nexus\_Protocol\_1.0.0.pdf), utilizing the immutability of Nexus to verify it’s internal states, making it resistant to most known operating system level exploits. It will be controlled by a security hardened operating system kernel, decentralised by virtue of its security and change-state blockchain-based authentication. This kernel is designed to resist attacks from malware, backdoors, and other vulnerabilities.

## **The Foundation: seL4**

![](../../.gitbook/assets/Sel4.webp)

Nexus has finally settled upon the seL4 (secure L4) microkernel as a foundation for NexOS. The seL4 microkernel branches from the L4 family of microkernels. This family has enjoyed significant commercial success (including billions in mobile phone sales) and adoption in critical systems around the world ([2](https://en.wikipedia.org/wiki/L4\_microkernel\_family)).&#x20;

Released in 2009 by the [Trustworthy Systems group](http://ts.data61.csiro.au/), seL4 focuses on critical systems such as military applications such as drones and satellites. Its core innovation comes from the guarantees in isolation properties between applications and unique approaches to kernel resource management. Specifically, seL4 led the world of operating systems by becoming the first formally verified general purpose microkernel (proofs are limited to only a few instruction sets such as ARM).

Formal verification involves transforming a code’s specification into mathematical abstractions, then constructing proofs to “prove” that the implementation follows the specification. Some describe formal verification as proving that bugs can’t occur, but this is imprecise, especially in complex systems where unknown inputs exist.&#x20;

For consumer applications which may be designed for other operating systems, seL4 runs a hypervisor which allows the virtualization of another OS (windows linux, etc.), however a consumer level use implementation of the NexOS won't occur until IoT use cases exhibit success. Overall, SeL4 provides Nexus developers an extremely stable, proven and innovative microkernel to serve as the cornerstone for LX-OS.&#x20;

## **What is LX-OS?**

What makes LX-OS unique from Sel4 is the integration of the latter with the Nexus blockchain to further enhance security and functionality. LX-OS uses Nexus blockchain to authenticate the runtime memory, file systems, and other system services. It will operate on a distributed file system, solving the problem of moving the entire App & OS state from one device to another. Listed below, three main innovations illustrate this novel security infrastructure. The first two relate to traditional operating systems components and the third relates to Nexus Protocol routing.

### **Runtime Memory and Binary Verification:**&#x20;

Runtime memory provides the temporary storage necessary for processing binary instructions. Operating systems create memory to process code and reclaim that memory once the process is finished. Binary verification refers to the ability to check that the binaries (0s and 1s comprising code) match a referential source. With LX-OS, all executable code must be authenticated either by the source developer or by the user running the application. The hash of the binary you’re installing will have to match the one stored in the developers Signature Chain. Every single runtime instruction will be authenticated with additional checksums. LX-OS ultimately resolves many of the vulnerability issues of today’s Operating Systems (Windows/Linux) that allows hackers to piggyback malware onto PC’s using elevated privileges, because they don’t use a ‘safe’ reference to authenticate changes against. LX-OS will authenticate all changes to the virtual user space across the entire runtime environment.

### **File Integrity:**&#x20;

Utilizing merkle trees maintains file integrity. Instead of hashing the entire file and storing it as authentication, merkle trees allow hashing of subsets of files, so changes to one part of the file won’t require the rehashing of the entire file. Creating a new file requires a user’s confirmation, generating a new merkle root that is stored in a special object register on Nexus that points to the data.

### **Software-Defined Routers (SDR):**&#x20;

Even after 20 years, the IPV6 protocol upgrade has not been completed, as the upgrade requires global hardware replacement that is unfeasible due to logistics, cost and compatibility complexities. LX-OS will use SDR to replace the ageing and insecure dedicated hardware routing system. It will utilise every device as a stateless router, enabling instant updates to routing and protocols with software updates. It also significantly improves the root of trust, mitigating the inherent risk of centralized entities like BGP, Domain Naming Service (DNS), Certificate Authorities (CA), back doors and similar vulnerabilities. This and the other authentication features remove the ability for many common attack vectors like trojans, injections, DDoS and similar.

****

## **Use-Cases of Lx-OS**

#### **Decentralized Internet:**&#x20;

The Lower-Level Library & LISP (LLLL) provides the basis for the entire Nexus Protocol, which is highlighted in the name LX-OS (L represents the LLLL, X for Nexus, and OS for Operating System). Nexus integrates verification into the LX-OS by interweaving consensus throughout the user and kernel spaces. It leverages Signature Chains and the ledger to authenticate the file system, runtime memory, and any change to the state of the kernel.

#### **Distributed File System:**&#x20;

Data sharding is enabled by the Lower Level Database (LLD), which will allow users to monetize spare disk space for a decentralized network-based cloud equivalent.

#### **Distributed computing framework:**

Inheritance of the distributed database, ledger, and protocols from Nexus constitute a form of distributed virtualization. Users login to their Signature Chains on any device to access a synchronized virtual desktop and file system while up-leveling security to the blockchain. LX-OS provides an important feature that no one in the computer industry has solved, that is, moving the entire app and OS state from one device to another. VMware solves this with VMs in data center servers, but why can’t users migrate their computer OS state to another computer or mobile device? LX-OS solves this by hosting all OS states in the blockchain network (in virtualized space) while the device executes commands. Besides security properties, other desirable features emerge such as offline identity verification and roaming device synchronization.

#### **Internet of Things (IoT):**

IoT is going to be a major use case. Using deterministic hardware identifications for device-level authentications (e.g. International Mobile Equipment Identity — IMEI) with a cryptographic identity based on Signature Chains, is an innovative security control mechanism for the IoT industry. At first the LX-OS will only target IoT use cases, but a consumer version for desktops, tablets and mobile devices will eventually follow, along with a hypervisor, which allows the virtualization of another OS (Windows, Mac, Linux etc).
