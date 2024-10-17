**Tags:** #Networking #Security #Firewalls #PacketFiltering

---

### **Definition**

A **Packet Filtering Firewall** controls network access by analyzing incoming and outgoing packets and allowing them to pass or halt based on the source and destination IP addresses, protocols, and ports.

### **Characteristics**

- **OSI Layer**: Operates at the Network Layer (Layer 3) and Transport Layer (Layer 4).
- **Rule-Based Filtering**: Uses predefined rules to filter traffic.
- **Stateless**: Does not track connection states; treats each packet independently.

### **Advantages**

- **Simplicity**: Easy to implement and manage.
- **Performance**: Minimal impact on network speed.

### **Disadvantages**

- **Limited Security**: Cannot inspect packet payloads.
- **Vulnerability**: Susceptible to IP spoofing and certain types of attacks.

### **Related Notes**

- [[Stateful Inspection Firewall]]
- [[Firewall Policies and Rules]]
- [[Common Firewall Ports and Protocols]]