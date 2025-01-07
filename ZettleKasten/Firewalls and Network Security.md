**Tags:** 
---

### **Definition**

Firewalls are security devices or software that monitor and control incoming and outgoing network traffic based on predetermined security rules. They act as a barrier between trusted internal networks and untrusted external networks, such as the internet, to prevent unauthorized access and protect against cyber threats.

### **Types of Firewalls**

- **Packet-Filtering Firewalls:** Inspect packets based on IP addresses, ports, and protocols.
- **Stateful Inspection Firewalls:** Track the state of active connections and make decisions based on the context.
- **Proxy Firewalls:** Act as intermediaries between clients and servers, providing content filtering.
- **Next-Generation Firewalls (NGFW):** Incorporate advanced features like intrusion prevention, application awareness, and deep packet inspection.

### **Configuration Best Practices**

- **Default Deny Policy:** Block all traffic by default and allow only necessary traffic.
- **Regular Updates:** Keep firewall rules and firmware up to date to protect against new threats.
- **Least Privilege:** Grant the minimum necessary permissions for services and users.
- **Logging and Monitoring:** Enable logging to detect and respond to suspicious activities.

### **Common Threats Mitigated**

- **Unauthorized Access:** Prevents unauthorized users from accessing network resources.
- **Malware and Viruses:** Blocks malicious traffic and prevents malware from spreading.
- **DDoS Attacks:** Mitigates distributed denial-of-service attacks by filtering excessive traffic.
- **Port Scanning:** Detects and blocks attempts to discover open ports on the network.

### **Examples**

- **Cisco ASA:** A widely used hardware firewall appliance.
- **pfSense:** An open-source firewall and router platform.
- **Windows Defender Firewall:** Built-in firewall solution for Windows operating systems.

### **Related Notes**

- Cache Poisoning
- DNS Zone Transfer
- Google Dorking