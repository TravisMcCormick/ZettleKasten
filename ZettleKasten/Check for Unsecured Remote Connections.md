**Tags:** #Security #RemoteAccess #Ubuntu #Windows

---

### **Definition**

Identifying and securing remote access services like SSH and RDP to prevent unauthorized remote connections.

### **Ubuntu/Linux**

- **Check Open Ports:**
    - Use `sudo netstat -tulnp` or `sudo ss -tulnp` to list listening services.
- **Secure SSH:**
    - Edit `/etc/ssh/sshd_config` to disable root login (`PermitRootLogin no`) and change the default port.
- **Disable Unnecessary Services:**
    - Stop and disable services like Telnet with `sudo systemctl stop telnet` and `sudo systemctl disable telnet`.

### **Windows**

- **Review Remote Settings:**
    - Go to **System Properties > Remote** tab.
    - Disable **Allow Remote Assistance** and **Remote Desktop** if not needed.
- **Check Listening Ports:**
    - Use `netstat -ano` in CMD to identify open ports.
- **Configure Firewall:**
    - Block or limit inbound connections on RDP port 3389.
- **Disable Unused Services:**
    - Turn off services like **Remote Registry** and **Telnet** via **services.msc**.

### **Advantages**

- **Prevents Unauthorized Access:** Reduces risk of remote attacks.
- **Resource Optimization:** Frees up resources by disabling unused services.

### **Disadvantages**

- **Accessibility:** May hinder legitimate remote administration.
- **Configuration Effort:** Requires careful setup to balance security and functionality.

### **Related Notes**

- [[Secure SSH Configuration (Linux)]]
- [[Secure Remote Desktop Settings]]
- [[Configure Firewall Rules]]