**Tags:** #Security #Updates #Patching #Ubuntu #Windows

---

### **Definition**

Applying the latest security patches and updates to ensure the system is protected against known vulnerabilities.

### **Ubuntu/Linux**

- **Update Package Lists:**
    - Run `sudo apt update` to refresh package information.
- **Upgrade Installed Packages:**
    - Execute `sudo apt upgrade` to install available upgrades.
- **Full Distribution Upgrade:**
    - Use `sudo apt full-upgrade` for major system upgrades.
- **Automate Updates:**
    - Configure automatic updates by editing `/etc/apt/apt.conf.d/50unattended-upgrades`.

### **Windows**

- **Using Windows Update:**
    - Go to **Settings > Update & Security > Windows Update**.
    - Click **Check for updates** and install available updates.
- **Configure Automatic Updates:**
    - Set update policies in **Settings** or via **Group Policy Editor** under **Computer Configuration > Administrative Templates > Windows Components > Windows Update**.
- **Command Line Updates:**
    - Use `wuauclt /detectnow` or `UsoClient StartScan` in CMD to force update checks.

### **Advantages**

- **Security Enhancements:** Protects against exploits targeting known vulnerabilities.
- **System Stability:** Fixes bugs and improves system performance.

### **Disadvantages**

- **Downtime:** May require system restarts, causing temporary unavailability.
- **Compatibility Issues:** Updates might conflict with existing applications.

### **Related Notes**

- [[Enable and Configure Firewall]]
- [[Run Antivirus Scan]]
- [[Audit Installed Applications]]