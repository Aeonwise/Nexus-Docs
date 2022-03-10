# Quantum Resistance

### What is a Quantum Computer?

A quantum computing is a rapidly-emerging technology that harnesses the laws of quantum mechanics to solve problems too complex for classical computer.

Quantum computers are elegant machines, smaller and requiring less energy than supercomputers.    The Quantum processor is a wafer not much bigger than the one found in a laptop. And a quantum hardware system is about the size of a car, made up mostly of cooling systems to keep the superconducting processor at its ultra-cold operational temperature.

Classical computing uses an array of transistors. These transistors form the heart of your computer (the CPU). Each transistor is capable of being either on or off, and these states are used to represent the numerical values 1 and 0. Binary digits’ (bits) number of states depends on the number of transistors available, according to the formula (2^n) + 1, with n being the number of transistors. Classical computers can only be in one of these states at any one time, so the speed of your computer is limited to how fast it can change state.

Quantum computers on the other hand, use what are termed quantum bits or ‘qubits’ which are represented by the quantum spin of electrons or photons. These particles are placed into a state called superposition, allowing the qubit to assume a value of 1 and 0 simultaneously, generally resulting in an exponential increase in computational power over their classical counterparts.



### What is Quantum Resistance?

Quantum-resistance — also known as post-quantum, quantum-secure, and quantum-safe — are cryptographic algorithms that can fend off attacks from quantum computers.



### Why we Need Quantum Resistance?

The first quantum computing algorithm was published by Peter Shor in 1994 — three years before the first quantum computer was built. But the idea that quantum computers could solve problems traditional computers can’t was first put forward by Richard Feynman, Paul Benioff, and Yuri Manin in the early 1980s.

While the first quantum computer was built in 1997, the field became an arms race during the 2010s.

IBM unveiled the first quantum computer for scientific and commercial use — IBM Q System One — in January 2019. In October of the same year, Google made history by announcing they’d achieved quantum supremacy. Their quantum computer had solved a mathematical problem it would take a traditional machine 10,000 years to solve.

Most blockchains like Bitcoin, Ethereum use Elliptic Curve Digital Signature Algorithm (ECDSA) for public key cryptography. Using a quantum computer, Shor’s algorithm can be used to break ECDSA.&#x20;

With Bitcoin, a private key, picked at random, is run through these algorithms to generate a public key. And the Bitcoin protocol uses the hash value of this to create a public Bitcoin address. A quantum computer could reverse this process and derive the private key from a public one. And voila! Bitcoin’s claim of inviolability and unhackability is gone. Two major quantum algorithms that threaten the current state of cryptography have already been developed: Grover's and Shor's algorithms.

Researchers at the University of Singapore have said that Bitcoin’s cryptographic algorithm could be under threat by quantum computers as soon as 2027.&#x20;



### Quantum Resistance for Blockchains

With the rise in the power of classical computers and the emergence of quantum computers, public keys are becoming increasingly vulnerable. Most cryptocurrency addresses are created by hashing or obscuring the public key. Though, when a user makes a transaction the public key is revealed on the blockchain. In the realm of classical computing there is little risk with this method. However, a quantum computer running Shor’s algorithm could break most public key cryptography in little to no time, resulting in funds being stolen. Though most conjectures range from five to ten years before security could begin to break, Nexus has prepared by integrating a number of cryptographic innovations that support increased levels of quantum resistance.



### Nexus - Quantum Resistance&#x20;

We have developed an architecture called Signature Chains that enhances the security of existing DSA (Digital Signature Algorithm), by hashing the public key until it is used while changing the key pair with every transaction. We have also integrated the following cryptographic functions: FALCON (a second round contender for the NIST Post-Quantum cryptography competition), Argon2 (winner of the password hashing competition, and a superior alternative to S-Crypt or B-Crypt), and Keccak (winner of the SHA3 competition).

\
