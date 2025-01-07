**Tags:**

---

### **Definition**

DHCP (Dynamic Host Configuration Protocol) is a network management protocol used to automate the process of configuring devices on IP networks. It assigns IP addresses, subnet masks, gateways, and other network parameters to devices, enabling them to communicate effectively on the network.

### **How It Works**

1. **Discovery:** Client broadcasts a DHCPDISCOVER message to find available DHCP servers.
2. **Offer:** DHCP servers respond with a DHCPOFFER message containing IP configuration.
3. **Request:** Client requests the offered IP by sending a DHCPREQUEST message.
4. **Acknowledgment:** DHCP server confirms with a DHCPACK, finalizing the configuration.

### **DHCP vs. Static IP**

- **DHCP:**
    - **Pros:** Simplifies management, reduces configuration errors, supports mobile devices.
    - **Cons:** Relies on DHCP server availability, potential for IP conflicts if misconfigured.
- **Static IP:**
    - **Pros:** Consistent IP address, essential for servers and network devices.
    - **Cons:** Manual configuration, prone to errors, less scalable.

### **DHCP Options**

- **Option 53:** DHCP Message Type
- **Option 54:** DHCP Server Identifier
- **Option 51:** IP Address Lease Time
- **Option 1:** Subnet Mask
- **Option 3:** Router (Default Gateway)

### **Security Considerations**

- **Rogue DHCP Servers:** Unauthorized servers can assign incorrect IP configurations.
- **DHCP Snooping:** A network security feature to prevent rogue DHCP servers.
- **IP Address Reservation:** Ensures specific devices receive consistent IP addresses.

### **Related Notes**

- DNS Zone Transfer
- Firewalls and Network Security
- Top-Level Domains (TLDs)