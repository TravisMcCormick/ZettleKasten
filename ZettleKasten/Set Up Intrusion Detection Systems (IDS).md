**Tags:** #Security #IDS #Ubuntu #Linux #Windows

---

### **Definition**

Implementing Intrusion Detection Systems to monitor network or system activities for malicious actions or policy violations.

### **Ubuntu/Linux**

- **Install IDS Software:**
    - Use tools like **Snort**, **Suricata**, or **OSSEC**.
    - Install Snort: `sudo apt install snort`.
- **Configure Snort:**
    - Edit `/etc/snort/snort.conf` to set up rules and network configurations.
    - Define home network: `ipvar HOME_NET your_network_subnet`.
- **Start Snort Service:**
    - Run in intrusion detection mode: `sudo snort -A console -q -c /etc/snort/snort.conf -i eth0`.
- **Monitor Alerts:**
    - Check `/var/log/snort/alert` for intrusion alerts.

### **Windows**

- **Install IDS Software:**
    - Use tools like **Snort for Windows** or **OSSEC**.
- **Configure IDS:**
    - Edit configuration files to define rules and monitoring preferences.
- **Start IDS Service:**
    - Run the IDS software as a service or scheduled task.
- **View Alerts:**
    - Check logs or use a GUI dashboard if available.

### **Advantages**

- **Threat Detection:** Identifies malicious activities in real-time.
- **Security Monitoring:** Provides insights into network and system security.

### **Disadvantages**

- **False Positives:** May generate alerts for legitimate activities.
- **Resource Intensive:** Can consume significant system resources.

### **Related Notes**

- [[Enable Logging and Auditing]]
- [[Perform Vulnerability Scanning]]
- [[Set Up Centralized Logging]]