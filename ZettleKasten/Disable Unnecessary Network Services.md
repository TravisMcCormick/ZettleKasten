**Tags:** #Security #NetworkServices #Ubuntu #Windows

---

### **Definition**

Turning off network services that are not needed to reduce potential entry points for attackers.

### **Ubuntu/Linux**

- **List Active Services:**
    - Use `sudo netstat -tulnp` or `sudo ss -tulnp`.
- **Identify Unnecessary Services:**
    - Common services to check include Telnet, FTP, and rlogin.
- **Disable Services:**
    - Stop service with `sudo systemctl stop servicename`.
    - Disable service from starting at boot with `sudo systemctl disable servicename`.
- **Remove Services:**
    - Uninstall with `sudo apt remove package-name`.

### **Windows**

- **View Services:**
    - Open **services.msc**.
- **Identify Services:**
    - Look for services like **Telnet**, **Remote Registry**, **SNMP**.
- **Disable Services:**
    - Right-click the service, select **Properties**, set **Startup type** to **Disabled**.
- **Uninstall Features:**
    - Go to **Control Panel > Programs and Features > Turn Windows features on or off**.
    - Uncheck unnecessary components.

### **Advantages**

- **Reduces Attack Surface:** Fewer services mean fewer vulnerabilities.
- **Resource Optimization:** Frees up system resources.

### **Disadvantages**

- **Functional Impact:** Disabling needed services can disrupt operations.
- **Maintenance Effort:** Requires understanding of service dependencies.

### **Related Notes**

- [[Check for Unauthorized Services and Processes]]
- [[Configure Firewall Rules]]
- [[Secure SSH Configuration (Linux)]]