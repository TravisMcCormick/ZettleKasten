**Tags:** #Security #Firewall #Rules #Ubuntu #Windows

---

### **Definition**

Creating specific rules in the firewall to allow or deny traffic based on protocols, ports, and IP addresses.

### **Ubuntu/Linux**

- **Using UFW:**
    - Allow specific ports: `sudo ufw allow 80/tcp`.
    - Deny specific IP: `sudo ufw deny from 192.168.1.100`.
- **Advanced Configuration:**
    - Edit `/etc/ufw/before.rules` for complex rules.
- **Logging:**
    - Enable logging with `sudo ufw logging on`.
- **Reload Firewall:**
    - Apply changes with `sudo ufw reload`.

### **Windows**

- **Access Advanced Settings:**
    - Open **Windows Defender Firewall with Advanced Security**.
- **Create New Rule:**
    - Inbound or Outbound rules can be set based on program, port, or custom criteria.
- **Configure Rule Properties:**
    - Define protocols, ports, and scope (IP addresses).
- **Rule Actions:**
    - Choose to **Allow**, **Block**, or **Allow if Secure**.

### **Advantages**

- **Traffic Control:** Precisely manage network access.
- **Security Enhancement:** Blocks unwanted or malicious traffic.

### **Disadvantages**

- **Complexity:** Requires careful planning to avoid disrupting services.
- **Maintenance:** Needs regular updates as network configurations change.

### **Related Notes**

- [[Enable and Configure Firewall]]
- [[Check Open Ports and Close Unused Ones]]
- [[Implement Network Segmentation]]