# LX-OS (Future)

### LX-OS

**What is the LX-OS?**

LX-OS, the Nexus Operating System will initially run on micro-satellites and IoT (Internet of Things) devices, which generally have weak security models. LX-OS will drive the Nexus Protocol, utilizing the immutability of Nexus to verify it’s internal states, making it resistant to most known operating system level exploits. It will be controlled by a security hardened operating system kernel, decentralised by virtue of its security and change-state blockchain-based authentication. This kernel is designed to resist attacks from malware, backdoors, and other vulnerabilities.

Kernel design and management represents a key feature distinguishing operating systems. Kernels are the closest software to your computer’s hardware, often referred to as Ring 0. They allocate and regulate applications with the necessary physical resources while maintaining strong isolation characteristics between processes. Most applications run in an unprivileged ‘user mode’ rather than a privileged ‘kernel mode’ which gives access directly to the hardware.

**seL4**

LX-OS is built on the seL4 micro-kernel, which when combined with Nexus, can resist attacks from malware, backdoors, and other common vulnerabilities. seL4 is an open source, high-assurance, high-performance, security-hardened operating system kernel. It is part of an ecosystem supporting active use in various domains including automotive, aviation, infrastructure, medical and defence. It has found commercial success in mission-critical military applications. It is unique because of its comprehensive formal verification, without compromising performance. Formal verification involves transforming a code specification into mathematical abstractions, then constructing proofs to prove that the implementation follows specification. The core strength is its isolation between applications running in the system, meaning that a compromise in one part of the system can be contained and prevented from harming other, potentially more critical parts of the system. Overall, seL4 provides Nexus developers an extremely stable, proven, and innovative microkernel to serve as the foundation for LX-OS

**Monolithic Kernel**

![](../../.gitbook/assets/monolithic)

Many types of kernels exist, but most consumer operating systems tend toward what is called monolithic kernels. Monolithics use the kernel for all system operations such as memory handling, file operations, drivers, and thread scheduling. This monolithic structure keeps operations quick by not requiring IPC (Inter-Process Communication), however it has limitations such as poor fault tolerance (if a driver crashes, your kernel and thus computer will crash too). The historic _Windows Blue Screen of Death_, experienced in early versions of Windows, highlights the sensitivity of monolithic kernels, as one minor mistake can cause full system failure.

**Microkernel**

![](../../.gitbook/assets/microkernel)

Microkernels embody a modular design focusing on fault tolerance and footprint minimization. Since a primary goal of kernels is to shield the hardware space, microkernels avoid running unnecessary code in the privileged space when it could be offloaded to the user mode (unprivileged). The increased fault tolerance and modularity can come at the cost of latency, especially in interactions with non-kernel components, but the security and code simplicity helps make up for the loss.

LX-OS uses [Signature Chains](broken-reference) to authenticate the runtime memory, file systems, and other system servers. It will operate on a distributed file system, solving the problem of moving the entire App & OS state from one device to another. Listed below, three main innovations illustrate this novel security infrastructure. The first two relate to traditional operating systems components and the third relates to Nexus Protocol routing.

**Runtime memory and binary verification:** Runtime memory provides the temporary storage necessary for processing binary instructions. Operating systems create memory to process code and reclaim that memory once the process is finished. Binary verification refers to the ability to check that the binaries (0s and 1s comprising code) match a referential source. With LX-OS, all executable code must be authenticated either by the source developer or by the user running the application. The hash of the binary you’re installing will have to match the one stored in the developers Signature Chain. Every single runtime instruction will be authenticated with additional checksums. LX-OS ultimately resolves many of the vulnerability issues of today’s Operating Systems (Windows/Linux) that allows hackers to piggyback malware onto PC’s using elevated privileges, because they don’t use a ‘safe’ reference to authenticate changes against. LX-OS will authenticate all changes to the virtual user space across the entire runtime environment.

**File integrity:** Utilizing merkle trees maintains file integrity. Instead of hashing the entire file and storing it as authentication, merkle trees allow hashing of subsets of files, so changes to one part of the file won’t require the rehashing of the entire file. Creating a new file requires a user’s confirmation, generating a new merkle root that is stored in a special object register on Nexus that points to the data.

**Software-defined routers (SDR):** Even after 20 years, the IPV6 protocol upgrade has not been completed, as the upgrade requires global hardware replacement that is unfeasible due to logistics, cost and compatibility complexities. LX-OS will use SDR to replace the ageing and insecure dedicated hardware routing system. It will utilise every device as a stateless router, enabling instant updates to routing and protocols with software updates. It also significantly improves the root of trust, mitigating the inherent risk of centralized entities like BGP, Domain Naming Service (DNS), Certificate Authorities (CA), back doors and similar vulnerabilities. This and the other authentication features remove the ability for many common attack vectors like trojans, injections, DDoS and similar.

**Decentralized Internet:** The Lower-Level Library & LISP (LLLL) provides the basis for the entire Nexus Protocol, which is highlighted in the name LX-OS (L represents the LLLL, X for Nexus, and OS for Operating System). Nexus integrates verification into the LX-OS by interweaving consensus throughout the user and kernel spaces. It leverages Signature Chains and the ledger to authenticate the file system, runtime memory, and any change to the state of the kernel.

**Distributed File System:** Data sharding is enabled by the Lower Level Database (LLD), which will allow users to monetize spare disk space for a decentralized network-based cloud equivalent.

**Distributed computing framework:** Inheritance of the distributed database, ledger, and protocols from Nexus constitute a form of distributed virtualization. Users login to their Signature Chains on any device to access a synchronized virtual desktop and file system while up-leveling security to the blockchain. LX-OS provides an important feature that no one in the computer industry has solved, that is, moving the entire app and OS state from one device to another. VMware solves this with VMs in data center servers, but why can’t users migrate their computer OS state to another computer or mobile device? LX-OS solves this by hosting all OS states in the blockchain network (in virtualized space) while the device executes commands. Besides security properties, other desirable features emerge such as offline identity verification and roaming device synchronization.

**Internet of Things (IoT):** IoT is going to be a major use case. Using deterministic hardware identifications for device-level authentications (e.g. International Mobile Equipment Identity — IMEI) with a cryptographic identity based on Signature Chains, is an innovative security control mechanism for the IoT industry. At first the LX-OS will only target IoT use cases, but a consumer version for desktops, tablets and mobile devices will eventually follow, along with a hypervisor, which allows the visualization of another OS (Windows, Mac, Linux etc).

To learn more, please read the Nexus Protocol Whitepaper.

{% content-ref url="nexus-protocol-future/" %}
[nexus-protocol-future](nexus-protocol-future/)
{% endcontent-ref %}
