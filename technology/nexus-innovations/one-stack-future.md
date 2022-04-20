---
description: ONE stack
---

# ONE Stack (Future)

The ONE acronym stands for One Nexus Execution, a stack designed to replace the OSI (Open system Interconnect) reference model. It is a fundamental reference model for the Nexus Protocol. The ONE stack is made up of 7 layers, out of which two are from the current OSI.

Watch the ONE stack presentation by Colin Cantrell, link below:

{% embed url="https://www.youtube.com/watch?t=197s&v=BS3Cfo784z8" %}
ONE Stack Presentation By Colin Cantrell.
{% endembed %}

## Layers of the ONE Stack

The image below shows how the ONE stack interacts with the Nexus software stack and also the OSI stack.

![ONE Stack interaction with the Nexus Software Stack](../../.gitbook/assets/ONE-Stack-Dark.png)

### SIGNAL

The Signal layer refers to the communication between the satellites and ground stations. The signal layer is responsible the physical modulation of the carrier wave. it is connected wirelessly to phased ray antennas. It uses the unlicensed 5.8 GHz band for communication for open deployment of terrestrial and orbital infrastructure. It will follow MCS (Modulation and Coding scheme) up to MCS-11, using 1024-QAM.

### LOCATION

The second layer is the Locator layer, which is responsible for routing the packet to the correct geo-location. It will have multiple type of locators, the prominent types are Geo- Spatial Locator (GSL), Wide Radius Locator (WRL) and Internet Protocol Locator (IPL). Routing is done topologically   independent, not requiring any state to be managed to get a complete route. It inter-operates with the legacy internet, IP, as another set of locator&#x20;

### IDENTIFIER

The identifier layer is where packets are actually addressed to. It like a computer having a permanent phone number anyone can contact no matter which network that particular computer is on. Identifiers are unique and is cryptographically authenticated meaning the identifiers cannot be spoofed. It expands upon the 128 bit available number space for IPV6, but it uses that only as a common interface between IP/NP.

### SESSION

The session layer is brought over from the OSI. Protocols like UDP and TCP will still be used in NP. Session layer security such as TLS will still be utilized.  There will still be the same socket interface, even when running LX-OS over IP, as you will always open TCP/NP/IP to their 128 bit identifier. This means a user can use IP or NP and it will be as if using one large internet.

The session layer creates communication channels, called sessions, between devices. It is responsible for opening sessions, ensuring they remain open and functional while data is being transferred, and closing them when communication ends. The session layer can also set checkpoints during a data transfer—if the session is interrupted, devices can resume data transfer from the last checkpoint.

### TRANSPORT

The transport layer is brought over from the OSI. The transport layer takes data transferred in the session layer and breaks it into “segments” on the transmitting end. It is responsible for reassembling the segments on the receiving end, turning it back into data that can be used by the session layer. The transport layer carries out flow control, sending data at a rate that matches the connection speed of the receiving device, and error control, checking if data was received incorrectly and if not, requesting it again.

### CONSENSUS

The consensus layer is responsible for the creating a layer of trust on both IP and NP. It is a common reference point of truth for managing root of trust such as security certificates. It is composed of the three layers from the Nexus Software Stack: Ledger, Register and Operations. This is where we get the One Nexus Execution.

### APPLICATION

The application layer is the human-computer interaction layer where applications can access the network services, such as web browsers and email clients. It provides protocols that allow software to send and receive information and present meaningful data to users. A few examples of application layer protocols are the Hypertext Transfer Protocol (HTTP), File Transfer Protocol (FTP), Post Office Protocol (POP), Simple Mail Transfer Protocol (SMTP), and Domain Name System (DNS).

