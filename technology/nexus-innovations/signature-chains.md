---
description: User Accounts on Nexus
---

# Signature Chains

## Key Management - The Problem

A major benefit of using cryptocurrencies is the security gained through the use of public key cryptography. Though this is a vast improvement to centralized login systems, this benefit comes with the drawback of key management. In order to manage keys, most cryptocurrency wallets use a database storage file called a ‘wallet.dat’ that keeps a record of all the keys that have been / will be used to access coins.

We believe that the adoption of cryptocurrency and blockchain technology will always be limited if relying on such a model, due to the inconvenience of having to make regular wallet backups, loss or theft of hard drives, and the risk of sending funds to unspendable addresses. These systems are susceptible to human error, boding for the need for complex hardware designed specifically to store private keys securely. Though these devices are a step towards user friendliness, they contain proprietary hardware and software, still at risk of being lost or stolen, and therefore are not a reliable replacement for authorization systems.

## Signature Chain - Solution&#x20;

Nexus designed a system to automate the management of keys via a decentralized login system we call Signature Chains (SIgChains). This allows users to log in to the Nexus Wallet simply using  Username, Password and PIN. Signature Chains still use public key cryptography, but rather than maintaining the keys on disk or the cloud, they are stored in ‘mathematical hyperspace’ meaning that your credentials become the 'key' to a 'virtual space' that users own with a Signature Chain. This also removes the burden of key management when using DApps, which often require third party plugins such as MetaMask.

Signature Chains decouple the private key from the user account, therefore one is unbound by the possession or security of a single private key. The private key becomes obsolete when the next transaction is generated, producing higher levels of security compared to the continual reuse of a private key, as is the case with other blockchain technologies.

Signature Chains (Sigchains) are comparable to a 'personal Blockchain', and provide the foundation for DApps that manage all types of digital property. They integrate into existing application frameworks that already rely on authorization systems through username and password combinations, and thereby provide DApp developers the ability to integrate blockchain functionalities as an elevated layer into existing applications with minimal architectural modification. They can also be integrated with various security measures such as biometrics and hardware password managers.

Additional benefits are the efficiency gained by reducing the requirement of storing a large amount of signatures on disk, and the ability to use a variety of key types such as FALCON for quantum Resistance.

### Speed and Scalability

Sigchains use an account based model that replaces the clunky UTxO (Unspent Transaction Output) architecture that Bitcoin introduced. Sigchains contain all user data on a unique chain, and provide higher levels of scalability, as only one signature is required to be verified per transaction.

Along with Sigchains, Nexus transactions are decoupled from the block, which means that only a single hash or ‘proof’ per transaction is required in the block level data, rather than the entire transaction itself. This results in the accommodation of approximately 31,728 transactions per 2 MB block. Together, these innovations produce lightweight blocks and efficient transaction processing, without the requirement of off chain (Layer 2) scaling solutions.

### Pruning

A Signature Chain is named as such due to it being a chain of nexthashes, a hash of signature and public key. Since this is a consistent chain of events that cannot be altered, it provides additional scaling benefits by requiring only two signatures to verify an entire Sigchain: the first and last transaction. This means that all the signatures in between can be discarded along with the public keys, saving a large amount of storage space without sacrificing security. This is because a Sigchain is an immutable chain of transactions A valid signature at the head transaction of the chain proves that the entire chain is valid, as it locks the entire Sigchain from modification.

Usually, this signature is the largest part of the transaction, therefore removing the need to save it on disk improves the scalability of the Nexus Blockchain. In Bitcoin, the average input size is 186 bytes, with the signature consuming 146 of these bytes, resulting in 77% of the Bitcion blockchain being comprised of signatures stored on disk. As you can see, signature chaining has a huge impact on combating blockchain bloat.

### Secure Digital Identity

An End Point Identifier (EID) is similar to an Internet Protocol (IP) address, and is a form of identity on the network layer. Through the use of [LISP](broken-reference), the EID becomes the identifier, while the RLOC (Routing Locator) becomes the location. This decoupling enables a device to freely roam between networks as only the RLOC changes, not the EID. This is contrary to how the Internet currently functions, where both the identifier and location are bound together in a single IP address.

An EID is a critical security feature, as it can be linked to a Sigchain which makes the network identifier cryptographically associated with the Ledger. EIDs, Sigchains and the use of reputation combined create an elevated layer of trust to the Internet, as one can verify with certainty that the other party is who they claim to be without the need for third party services like Certificate Authorities (CA). A reduction in fraud, hacking, fake accounts, and identity theft for both consumers and service providers is envisioned as a result of this technology.

### Quantum Resistance

Sigchains increases resistance to attack by both classical and theoretical quantum computers. This is achieved by decoupling the identity of the account from the cryptography associated with it, similar to how [LISP](broken-reference) decouples the identifier and the location. This enables the architectural advantage of changing the key pair that is used to access the Sigchain with every transaction, and hiding the public key until it is used. When an individual creates a transaction on the network, they claim ownership by revealing the public key of the NextHash (the hash of the public key) by producing a valid signature from the one time use private key. This significantly reduces the time window for an attack to take place, naturally increasing the required computing power to successfully hijack a signature chain with MITM (Man in the Middle) attacks. Please see [Quantum Resistance](broken-reference) for more information.

Since the account identity is decoupled from the cryptography, a Sigchain supports multiple signature schemes such as FALCON (Fast Fourier Lattice-Based Compact Signatures Over NTRU) or Brainpool. Due to FALCON being still under study and assessment by NIST (National Institute of Standards and Technology), it is generally recommended that it is only used in production in what is termed a ‘hybrid signature scheme’, meaning you don’t rely solely on the security of FALCON for the security of the system. In our implementation, a Sigchain acts like a hybrid signature scheme, making use of FALCON safe for our production environment.
