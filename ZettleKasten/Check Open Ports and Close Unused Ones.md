**Tags:** #Security #NetworkPorts #Ubuntu #Windows

---

### **Definition**

Scanning for open network ports and closing those that are not required to prevent unauthorized access.

### **Ubuntu/Linux**

- **List Open Ports:**
    - Use `sudo netstat -tulnp` or `sudo ss -tulnp`.
- **Identify Unnecessary Ports:**
    - Cross-reference open ports with running services.
- **Close Ports:**
    - Stop associated services with `sudo systemctl stop servicename`.
    - Configure firewall to block ports using `sudo ufw deny portnumber`.
- **Verify Changes:**
    - Re-run port scan to ensure ports are closed.

### **Windows**

- **List Open Ports:**
    - Execute `netstat -ano` in CMD.
- **Identify Services:**
    - Match PID from netstat output to processes in Task Manager.
- **Close Ports:**
    - Stop or disable the associated service.
- **Configure Firewall:**
    - Use Windows Defender Firewall to block specific ports.

### **Advantages**

- **Security Enhancement:** Minimizes potential entry points for attacks.
- **Network Control:** Better management of network traffic.

### **Disadvantages**

- **Disruption Risk:** Closing necessary ports can interrupt services.
- **Technical Complexity:** Requires knowledge of network protocols.

### **Related Notes**

- [[Disable Unnecessary Network Services]]
- [[Enable and Configure Firewall]]
- [[Perform Vulnerability Scanning]]