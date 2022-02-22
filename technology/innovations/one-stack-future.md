# ONE Stack (Future)

The ONE acronym stands for One Nexus Execution, a stack designed to replace the OSI (Open system Interconnect) reference model. It is a fundamental reference model for the Nexus Protocol. The ONE stack is made up of 7 layers, out of which two are from the current OSI.

{% embed url="https://www.youtube.com/watch?t=197s&v=BS3Cfo784z8" %}



Application

Concession

Session

Transport





### Signal

The Signal layer refers to the communication between the satellites and ground stations. The signal layer is responsible the physical modulation of the carrier wave. it is connected wirelessly to phased ray antennas. It uses the unlicensed 5.8 GHz band for communication for open deployment of terrestrial and orbital infrastructure. It will follow MCS (Modulation and Coding scheme) up to MCS-11, using 1024-QAM.

### Location

The second layer is the Locator layer, which is responsible for routing the packet to the correct geo-location. It will have multiple type of locators, the prominent types are Geo- Spatial Locator (GSL), Wide Radius Locator (WRL) and Internet Protocol Locator (IPL). Routing is done topologically   independent, not requiring any state to be managed to get a complete route. It inter-operates with the legacy internet, IP, as another set of locator&#x20;

### Identifier

The identifier layer is where packets are actually addressed to. It like a computer having a permanent phone number anyone can contact no matter which network that particular computer is on. Identifiers are unique and is cryptographically authenticated meaning the identifiers cannot be spoofed. It expands upon the 128 bit available number space for IPV6, but it uses that only as a common interface between IP/NP.

The Transport and Session layers are brought over from the OSI. Protocols like UDP and TCP will still be used in NP. Session layer security such as TLS will still be utilized.  There will still be the same socket interface, even when running LX-OS over IP, as you will always open TCP/NP/IP to their 128 bit identifier. This means&#x20;
