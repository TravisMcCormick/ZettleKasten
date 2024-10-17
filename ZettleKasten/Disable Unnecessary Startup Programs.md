**Tags:** #Performance #StartupPrograms #Ubuntu #Windows

---

### **Definition**

Removing or disabling programs that automatically start with the system but are not required, improving boot time and reducing resource usage.

### **Ubuntu/Linux**

- **View Startup Applications:**
    - Use **Startup Applications** utility or check `.config/autostart/`.
- **Disable Startup Programs:**
    - Uncheck programs in **Startup Applications**.
    - Remove unnecessary entries from `/etc/rc.local` or cron jobs.
- **Systemd Services:**
    - List services with `systemctl list-unit-files --type=service`.
    - Disable with `sudo systemctl disable servicename`.

### **Windows**

- **Use Task Manager:**
    - Press Ctrl+Shift+Esc, go to **Startup** tab.
    - Right-click and disable unnecessary programs.
- **System Configuration:**
    - Run `msconfig`, navigate to **Startup** tab.
- **Startup Folder:**
    - Remove shortcuts from **C:\Users\Username\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup**.

### **Advantages**

- **Faster Boot Times:** Reduces system startup duration.
- **Improved Performance:** Frees up RAM and CPU resources.

### **Disadvantages**

- **Missing Functionality:** Disabling essential programs may affect system operations.
- **User Inconvenience:** Some programs might be needed immediately after startup.

### **Related Notes**

- [[Check for Unauthorized Services and Processes]]
- [[Audit Installed Applications]]
- [[Enable Logging and Auditing]]