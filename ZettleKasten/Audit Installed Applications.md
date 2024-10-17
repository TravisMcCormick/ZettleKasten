**Tags:** #Security #SoftwareAudit #Ubuntu #Windows

---

### **Definition**

Reviewing and evaluating all installed applications to remove unauthorized or unnecessary software.

### **Ubuntu/Linux**

- **List Installed Packages:**
    - Run `dpkg --list` or `apt list --installed`.
- **Identify Unnecessary Software:**
    - Review the list and mark unfamiliar packages.
- **Uninstall Applications:**
    - Use `sudo apt remove package-name` to uninstall.
- **Clean Up Residual Files:**
    - Execute `sudo apt autoremove` and `sudo apt clean`.

### **Windows**

- **View Installed Programs:**
    - Go to **Control Panel > Programs and Features**.
- **Identify Unwanted Software:**
    - Look for unfamiliar or unnecessary applications.
- **Uninstall Programs:**
    - Select the program and click **Uninstall**.
- **Check for Leftover Files:**
    - Delete residual folders in **Program Files** and **AppData**.

### **Advantages**

- **Reduces Vulnerabilities:** Removes software that may have security flaws.
- **Optimizes Performance:** Frees up disk space and resources.

### **Disadvantages**

- **Potential Dependencies:** Uninstalling may affect other applications.
- **Time-Consuming:** Requires careful evaluation of each application.

### **Related Notes**

- [[Disable Unnecessary Startup Programs]]
- [[Check for Unauthorized Services and Processes]]
- [[Enable Logging and Auditing]]