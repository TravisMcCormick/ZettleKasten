**Tags:** #networking #protocol #data-link-layer #ARP 

---

### Definition

**ARP** is a protocol used to map IP addresses to the physical MAC addresses in a local network.

### Function

- **IP to MAC Translation**: Essential for data link layer communication.
- **Caching**: Stores mappings to reduce network traffic.

### Security Considerations

- **ARP Spoofing**: Malicious actors can redirect traffic by sending fake ARP messages.

### Personal Insight:

**ARP functions like a local directory assistance.** When a computer knows another device's IP address but not its physical MAC address, it broadcasts a request: "Who has IP address X.X.X.X?" The device with that IP responds with its MAC address, enabling direct communication at the data link layer.

### **Related Notes**

- [[How IP Addresses Facilitate Communication]]
- [[IP Spoofing]]
- [[MAC Addresses]]
- [[Data Link Layer]]
- [[Networking Protocols]]
- [[Ethernet Protocol]]
- [[What is an IP Address]]