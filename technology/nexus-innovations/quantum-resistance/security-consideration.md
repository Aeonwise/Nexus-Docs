---
description: Man In The Middle Attack
---

# Security Consideration

Nexus offers post quantum cryptography as an optional feature to users, as at the moment ECC is still considered safe. Our optional safeguards provide adequate levels of resistance against attacks using a quantum computer. The following will describe a MITM (Man-In-The-Middle) attack, which is the only known attack able to penetrate a signature chain if the user has not opted in to use FALCON (post quantum cryptography).

## Man-In-The-Middle Attack on Nexus

A MITM attack can be described as someone eavesdropping on node communication, and at the same time, relaying information to other nodes, masquerading as the sender. In order for this type of attack to take place, an attacker would need to control the sigchain of every single node that the user is connected to (i.e to compromise the private keys of all connected nodes). This is because Nexus records a hash in a sigchain’s crypto object register, that is a hash of the certificate being used for SSL/TLS (Secure Socket Layer / Transport Layer Security). This means that the attacker has further difficulty pretending to be a remote node, because the blockchain acts as a certificate authority (CA).

On top of verifying certificates, nodes require additional authentication before the network will accept their transactions. The authentication message is signed by another key in the crypto object register, which can be facilitated by FALCON or Brainpool. In order to successfully authenticate a connection as a MITM attacker, the attacker would need to gain access to all the remote node’s authentication keys.

{% hint style="info" %}
_**Note:** It is important to note that a replay attack would not work in this case, due to the authentication message containing a random session Nonce and timestamp that even if intercepted cannot be used to fake authentication._
{% endhint %}

Now, we will detail the steps of an attempted attack, assuming the user has not configured their account to use FALCON, and that the attacker is using a 3,800 qubit quantum computer.

1. The MITM attacker needs to first: brute force a user's certificate key or wait until the user's node sends it out in a key exchange. They cannot create their own self-signed certificate as in a normal MITM attack, since the blockchain acts as a certificate authority (CA).
2. The attacker now needs to brute force the user's authentication hash or again wait for an authentication message, and attempt to break the authentication key. Breaking this key would enable the attacker to forge authentication messages, and thus pretend to be a node that the user is connected to and trusts.
3. The attacker would then need to break the remote node's authentication key (assuming they can forge signatures on every open connection which is 16+ nodes, and that the remote node is not already using FALCON).
4. The attacker would then need to wait for the user to create a transaction, i.e for them to reveal their public key, and in less than 500ms, break this public key in order to forge transactions.

This is a requirement, because to successfully hijack a user’s account, the attacker would need to capture the transaction before it was broadcast, brute force the sender’s public key to obtain its private key, and then broadcast a forged transaction to take over this user’s account, all in less than 200ms.

## **Why is the attack window only 500ms?**

The network considers the most valid transaction the one that nodes receive first. With the internet round trip time taking roughly 200ms, this is your upper bound of packet propagation time. Therefore, in order to create a conflicting transaction that could hijack a user’s signature chain, the attacker would need their ‘attack’ transaction to propagate over the network before the user’s transaction. The window is only 200ms as the users transaction begins to propagate at the time that the users public key is revealed, making it highly improbable that any computer, including a quantum computer, could ever break a user’s public key.

We believe that even when ECC is being used instead of FALCON, the likelihood of a successful attack even by a quantum computer is very unlikely. However, users that wish to move away from ECC and switch to FALCON can do so with a click of a button, and with little risk to their previous transactions. This is because the keys that have already been used in our Signature Chain architecture, no longer have any use, and therefore can not be attacked.
