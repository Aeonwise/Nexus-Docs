# Lower Level Library (LLL)

The Lower Level Library (LLL) is the foundation for the TAO Framework. It is a base template library written in C++ minimizing hardware abstraction, thus maximizing bare metal efficiencies. Architecturally, the LLL is an interchangeable construct requiring logical development of templates and modules for specific functions. The LLL-TAO or TAO Framework is a series of LLL templates and data models that are accessible through a simple JSON-based API, allowing any type of developer to improve their application’s security, scalability, and robustness.

The LLL contains three main components: Cryptography (LLC), Database (LLD), and Protocol (LLP). There are several representations of LLD in the stack; Ledger, Register, Operations and API. The LLC is primarily applied at the Ledger layer although can be implemented elsewhere. As a component of the Network Layer, the LLP is designed to be a light, fast protocol that allows a developer to customize their packet design and message interpretation.

### Lower Level Crypto

#### Set of Operations for handling Crypto including:

* Digital Signatures (ECDSA, Hash Based)
* Hashing (SHA3 / Notable Secure Algorithms)
* Encryption (Symmetric / Asymmetric)
* Post-Quantum Cryptography (Experimental)

#### Currently Implemented:

* SK Hashing (Skein and Keccak)
* Argon2 Password hashing
* AES Standard (Symmetric)
* FALCON (Quantum Resistant Lattice Signatures)
* OpenSSL wrapping functions (EC\_KEY, BIGNUM)

### Lower Level Database

Set of Templates for designing high efficiency database systems. Core templates can be expanded into higher level database types.

* Keychain Database
* ACID Transactions
* Sector Database

Keychains Included:

* Binary File Map
* Binary Hash Map

We welcome any contributions of new keychains to provide different indexing data structures of the sector data.

### Lower Level Protocol

Set of Client / Server templates for efficient data handling. Inherit and create custom packet types to write a new protocol with ease and no network programming required.

* Data Server
* Listening Server
* Connection Types
* Packet Styles
* Event Triggers
* DDOS Throttling

LLP Protocols Implemented:

* Legacy
* Tritium
* HTTP

#### Utilities

Set of useful tools for developing any program such as:

* Serialization
* Runtime
* Debug
* Json
* Arguments
* Containers
* Configuration
* Sorting
* Allocators
* Filesystem
