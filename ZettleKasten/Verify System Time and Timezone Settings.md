**Tags:** #SystemConfiguration #TimeSettings #Ubuntu #Windows

---

### **Definition**

Ensuring that the system's date, time, and timezone settings are correct for proper logging, updates, and network operations.

### **Ubuntu/Linux**

- **Check Current Time and Timezone:**
    - Run `timedatectl` to display settings.
- **Set Timezone:**
    - Use `sudo timedatectl set-timezone Region/City`, e.g., `sudo timedatectl set-timezone America/New_York`.
- **Synchronize Time:**
    - Enable NTP with `sudo timedatectl set-ntp on`.
- **Manually Set Time:**
    - Use `sudo date -s "YYYY-MM-DD HH:MM:SS"`.

### **Windows**

- **Access Date and Time Settings:**
    - Right-click the clock on the taskbar and select **Adjust date/time**.
- **Set Timezone:**
    - Choose the correct timezone from the dropdown menu.
- **Synchronize with Internet Time Server:**
    - Under **Internet Time** tab, click **Change settings** and ensure synchronization is enabled.
- **Manually Adjust Time:**
    - Turn off **Set time automatically** and click **Change** to set manually.

### **Advantages**

- **Accurate Logging:** Essential for troubleshooting and security audits.
- **Network Compatibility:** Prevents issues with time-sensitive protocols.

### **Disadvantages**

- **Potential Conflicts:** Incorrect settings can cause authentication failures.
- **User Confusion:** Time changes might affect scheduled tasks.

### **Related Notes**

- [[Enable Logging and Auditing]]
- [Review Scheduled Tasks(Cron) Jobs](Review%20Scheduled%20Tasks(Cron)%20Jobs.md)
- [[Secure Remote Desktop Settings]]