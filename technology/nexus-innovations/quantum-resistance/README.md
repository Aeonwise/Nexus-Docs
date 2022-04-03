---
description: Designed for the quantum future.
---

# Quantum Resistance

With the rise in the power of classical computers and the emergence of quantum computers, public keys are becoming increasingly vulnerable. Most cryptocurrency addresses are created by hashing or obscuring the public key. Though, when a user makes a transaction the public key is revealed on the blockchain. In the realm of classical computing there is little risk with this method. However, a quantum computer running Shor’s algorithm could break most public key cryptography in little to no time, resulting in funds being stolen. Though most conjectures range from five to ten years before security could begin to break, Nexus has prepared by integrating a number of cryptographic innovations that support increased levels of quantum resistance.

We have developed an architecture called [Signature Chains](broken-reference) that enhance the security of existing DSA (Digital Signature Algorithm), by hashing the public key until it is used while changing the key pair with every transaction. We have also integrated the following cryptographic functions: FALCON (a second round contender for the NIST Post-Quantum cryptography competition), Argon2 (winner of the password hashing competition, and a superior alternative to S-Crypt or B-Crypt), and Keccak (winner of the SHA3 competition).

## Classic vs Quantum Computers

Classical computing uses an array of transistors. These transistors form the heart of your computer (the CPU). Each transistor is capable of being either on or off, and these states are used to represent the numerical values 1 and 0. Binary digits’ (bits) number of states depends on the number of transistors available, according to the formula (2^n) + 1, with n being the number of transistors. Classical computers can only be in one of these states at any one time, so the speed of your computer is limited to how fast it can change state.

Quantum computers on the other hand, use what are termed quantum bits or ‘qubits’ which are represented by the quantum spin of electrons or photons. These particles are placed into a state called superposition, allowing the qubit to assume a value of 1 and 0 simultaneously, generally resulting in an exponential increase in computational power over their classical counterparts.

## Signature Chain

Nexus is accessible through technology we designed called Signature Chains, a decentralized blockchain account that allows you to login from any computer with a username, password, and pin. They are comparable to a personal blockchain that allows decentralized access through a login system, removing the need to store a private key. Sigchains deterministically create a mathematical ‘lock’ that only your login credentials can unlock.

Fundamentally, a Sigchain decouples the private key from the user account, therefore one is unbound by the possession or security of a single private key. When one creates a transaction on the network, they claim ownership by revealing the public key of the NextHash (the hash of your public key) and produce a signature from the one time use private key. The private key becomes obsolete when the next transaction is generated, producing higher levels of security compared to the continual reuse of a private key, as is the case with other blockchain technologies. The future use of biometric username generation will strengthen your credentials and Signature Chain access.

## Key Management

Signature Chains decouple keys from the user account, meaning that at any time, you are able to change the type of key that your account uses. This gives users the option to use Post-Quantum cryptography such as FALCON, or the option to use more time-tested Brainpool curves. If any flaws were to be found in either of these cryptographic schemes, your account would be safe using a signature chain. These safeguards are important in order to protect systems over time, as ongoing crypto-analysis are always finding vulnerabilities and attack vectors that will begin to break once secure cryptographic standards (eg. SHA1).

[Large Bitcoin Collider Finds Another Bitcoin Private Key](https://bitcoinwhoswho.com/blog/2017/09/13/are-your-bitcoins-safe-large-bitcoin-collider-finds-another-private-key/)

## FALCON

Complemented with this is the use of FALCON (Fast-Fourier Lattice-Based Compact-Signatures Over NTRU) as an optional setting, that uses Lattice Based cryptography to ensure the security of accounts in the post-quantum age. The computational requirements are at least 1/40th of Elliptic Curve Digital Signature Algorithm (ECDSA), which means you can verify signatures much faster than ECDSA. However, the downside is that it requires about 1.5kb for both the public key and signature. Though Falcon is based on aged and proven mathematics (NTRU lattices), it has not undergone as much crypto-analysis as Elliptic Curve Cryptography (ECC) or Rivest Shamir Adleman (RSA).

## Argon2

Is an open source password hashing function we have integrated for key and username generation. Argon2 is a memory-hard password hashing algorithm with variable complexity which means it can control how many seconds it takes to generate a key or username. This drastically increases the time and resources it takes an offline hacker to brute-force a Signature Chain. Because the time to generate an Argon2 hash is bound by memory latency, a specialized ‘password cracking’ device has no advantage over a general purpose CPU.

Our default Argon2 settings requires at least 0.3 – 0.5 seconds to generate a new key, meaning one is only able to try two to three passwords per second. Combining this with a minimum requirement of at least 8 alphanumeric \[a-Z, 0-9] characters per password, even if the username and PIN were known by the attacker, the time required to crack the password would be in the order of 5 million years.

## Keccak

Due to the recommendation from NIST (National Institute for Standards in Technology), the bit requirement for symmetric encryption schemes and hash functions must be at least twice the size for equivalent quantum resistance (eg. 512 vs 256). This recommendation inspires our standard hash: 256-bits for registers, 512-bit for transactions, and 1024-bit for blocks for equivalent 128-bit, 256-bit, and 512-bit quantum resistance respectively.

## Cryptographic Redundancy

We do not rely on the security of only one cryptographic function for the security of the entire system, and treat every public key as disposable once used. This means our security uses many different layers of redundancy to provide protection, in the event that one of them becomes vulnerable. Relying on a single private key for security is a ticking time bomb, though this approach is largely used by most blockchain applications.

[Cryptographic Flaws found in IOTA](https://medium.com/@neha/cryptographic-vulnerabilities-in-iota-9a6a9ddc4367)

## Inherited security Flaw

The copy/paste mentality of source code used to create many cryptocurrency projects today has led to the pervasion of many security flaws. Below is one such example that created a pandemonium for hundreds of projects that inherited a flaw from Zcoin.

[Fatal Flaws may be embedded in all Privacy Coins](https://micky.com.au/expert-warning-fatal-flaw-embedded-in-all-privacy-coins/)

