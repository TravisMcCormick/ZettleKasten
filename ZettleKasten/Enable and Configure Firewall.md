**Tags:** #Security #Firewall #Ubuntu #Windows

---

### **Definition**

Activating and setting up the system's firewall to control incoming and outgoing network traffic based on predetermined security rules.

### **Ubuntu/Linux**

- **Enable UFW (Uncomplicated Firewall):**
    - Activate with `sudo ufw enable`.
- **Check Status:**
    - Run `sudo ufw status` to view current settings.
- **Allow Specific Ports:**
    - Allow SSH with `sudo ufw allow ssh` or `sudo ufw allow 22`.
- **Deny Incoming Traffic by Default:**
    - Set default policies with `sudo ufw default deny incoming` and `sudo ufw default allow outgoing`.

### **Windows**

- **Access Windows Defender Firewall:**
    - Go to **Control Panel > System and Security > Windows Defender Firewall**.
- **Enable Firewall:**
    - Ensure it's turned on for **Domain**, **Private**, and **Public** networks.
- **Configure Inbound/Outbound Rules:**
    - Use **Advanced Settings** to create or modify rules.
- **Block All Incoming Connections:**
    - Check **Block all incoming connections** under firewall settings for stricter control.

### **Advantages**

- **Traffic Control:** Filters unauthorized access and potential threats.
- **Customization:** Tailor rules to fit specific security needs.

### **Disadvantages**

- **Complexity:** Improper configuration can block legitimate traffic.
- **Performance Overhead:** May slightly impact system performance.

### **Related Notes**

- [[Configure Firewall Rules]]
- [[Check Open Ports and Close Unused Ones]]
- [[Secure Remote Desktop Settings]]