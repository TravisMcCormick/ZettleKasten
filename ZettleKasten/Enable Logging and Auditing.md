**Tags:** #Security #Logging #Auditing #Ubuntu #Windows

---

### **Definition**

Activating system logging and auditing features to monitor activities and detect potential security incidents.

### **Ubuntu/Linux**

- **Ensure Syslog is Running:**
    - Verify `rsyslog` or `syslog` service is active.
- **Configure Auditd:**
    - Install with `sudo apt install auditd`.
    - Edit `/etc/audit/auditd.conf` for settings.
- **Define Audit Rules:**
    - Add rules in `/etc/audit/audit.rules`, e.g., `-w /etc/passwd -p wa -k passwd_changes`.
- **View Logs:**
    - Use `ausearch` or check `/var/log/auth.log` and `/var/log/audit/`.

### **Windows**

- **Configure Audit Policy:**
    - Open **secpol.msc** and navigate to **Local Policies > Audit Policy**.
- **Enable Auditing Categories:**
    - Set policies for **Logon Events**, **Account Management**, **Object Access**, etc.
- **Advanced Audit Policy Configuration:**
    - For granular control, use **Advanced Audit Policy Configuration**.
- **View Event Logs:**
    - Open **Event Viewer** and check logs under **Windows Logs**.

### **Advantages**

- **Security Monitoring:** Detects unauthorized activities.
- **Forensic Evidence:** Provides logs for incident investigation.

### **Disadvantages**

- **Storage Requirements:** Logs can consume significant disk space.
- **Performance Impact:** May slightly affect system performance.

### **Related Notes**

- [[Implement Account Auditing]]
- [[Set Account Lockout Policies]]
- [[Perform Vulnerability Scanning]]