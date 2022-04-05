---
description: Locator Identifier Separation Protocol
---

# LISP

### Locator Identifier Separation Protocol (LISP)

When using the SafeNet, challenges of the traditional Internet will be a thing of the past, creating a more transparent and authentic Internet where sources are able to build reputation, peers are verifiable, and information is freely exchanged. It will take time to come to fruition, though we believe these innovations and many more will change the way we interact with the Internet.

Nexus runs on the Locator Identifier Separation Protocol (LISP) overlay, developed by team member Dino Farinacci who was the first Fellow (the most senior rank or title one can achieve in engineering) of Cisco.

LISP increases the reliability and security of communication between nodes, and is responsible for network scaling through multicast, identification through a static EID (Endpoint Identifiers), and authentication by using these identifiers. It will be used to enable secure access schemes for hybrid networks.

Through IPv6 addressing LISP provides ample capacity for the emerging IoT industry. It will also be used in a critical capacity with the release of Amine, which uses the Network (IP) layer to shard data and assign identifiers to data segments for management of the distributed database, without the loss of security or privacy. Some of the below features are fully integrated, and others are being deployed through the [TAO Framework](broken-reference).

{% hint style="info" %}
LISP is used by many organisations in their networks, But its implementation in blockchain was first done on Nexus. LISP will play a major role in the decentralised internet.built on top of Nexus. &#x20;
{% endhint %}

### Ease of Use

Imagine if your phone number changed every time you changed location, this is how IP (Internet Protocol) addresses work in their current form. Alternatively, LISP provides a unique End Point Identifier (EID), that allows one to have a consistent address, even when roaming between networks.

This means that genuine peer-to-peer connectivity is possible, because you are always accessible at one address, and remain so even when mobile. LISP enables you to remotely access your staking node from anywhere, while your node is busy working at the original location. This greatly increases the usability of your Nexus Wallet.

### Endpoint Identifier (EID)

An EID is a form of identity on the network layer. This is critical to security, as an EID is linked to a Signature Chain, that can be cryptographically associated with reputation on the ledger. This creates an elevated layer of trust and integrity to the Internet, as one can verify with certainty that their peer is who they claim to be.

EIDs replace your IP address that contains the identifier and the location in a standard network. With LISP, the EID becomes the identifier, while the RLOC (Routing Locator) becomes the location. This decoupling enables a device to freely roam between networks, as only the RLOC changes, not the EID.

EIDs don’t rely on any trusted third party for verification, as they can be proven in a decentralized manner on the ledger. Therefore, having to verify a new IP or a new device will no longer be necessary, as the identity of the device can be easily verified by both the network and ledger layers.

### Decentralization

Peer Discovery is a concept required for an effective and truly decentralized network. Nodes must be available to their peers by being able to accept incoming connection requests. Though this is not a novel concept, it is seldom achieved as the node or a device is usually behind a NAT (Network Address Translator), that generally leads to only 10% of peers being accessible or discovered. LISP handles NAT traversal differently to software such as UPnP, resulting in higher levels of node availability. Therefore, the Nexus network will rely less on ‘seed nodes’ to relay messages, creating a truly distributed network topology.

### IPV6 and Scalability

Most Internet devices use IPv4 addressing (the Internet equivalent of phone numbers), which is limited to around 4 billion devices. To accommodate the growth of Internet-connected devices, IPv6 was developed, though even decades later it still has not been widely adopted. LISP is able to use IPv6 as an overlay, since it does not suffer from the compatibility issues of underlay devices. The capacity of IPv6 is 2^128 devices, providing ample capacity for the growth of IoT devices.

LISP supports multicast and IPv6 EIDs which provide additional scaling and security to the network, making it a very attractive feature for blockchain applications and the emerging IoT industry.

### Multicast

Even though multicast is a well established protocol, not all routers provide it natively. This is due to the agreement between many Internet Service Providers (ISPs) to route each others’ traffic, where there are no incentives to forward multicast traffic. The LISP Overlay solves this with a technique called ‘head end forwarding’, which is consistent and operable across the entire global network regardless of the underlay nuances.

Multicast is important for blockchain scaling, because it routes packets in constant time O(1). This can be likened to a speaker making one speech to an entire group of people, whereas Unicast, the speaker tells one person, who tells the next person, and so on.

### Sharding

Another crucial use case for LISP is its role in the sharding of data within the [3D Chain](broken-reference), where it will be used to translate database indexes into usable and routable IPs. This will result in the network becoming one entirely accessible global database.

This means that components of the blockchain, such as transactions and blocks, will receive their own unique EID enabling any node to retrieve data without having to make complex ‘lookups’, or manage many states. This will be similar to typing ‘0xf8ea48fac8’ into your web browser, and in response receiving the data associated with this key.

In practical applications, nodes will only have to store a small portion of the ledger, and won’t have to undertake long and arduous synchronization processes. This is imperative to scaling, as normal computers are unable to run a full node as the blockchain grows. This was the main factor of the Bitcoin block size debate, which resulted in very small block sizes, and an increasingly unscalable network.

### Security and Privacy

The Internet was designed as an open system with few security parameters, which has resulted in many people experiencing hacks, IP spoofing, MITM (Man-In-The-Middle) and DoS attacks. Though openness is one of the cornerstones of the Internet today, security can be improved through the use of the LISP Overlay.

LISP supports ‘data plane’ encryption for any device (including ‘Internet of Things’ (IoT) devices) to communicate over the underlay, meaning that one benefits from encryption at the level of LISP and at the Nexus application layer. Similar to choosing when to answer your cell-phone, or to respond to a message, LISP provides options of how to interact with other users. This resonates with the Internet’s model of ‘openness’, while simultaneously protecting rights of privacy.
