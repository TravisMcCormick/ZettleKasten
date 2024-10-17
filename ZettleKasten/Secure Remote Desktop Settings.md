**Tags:** #Security #RemoteDesktop #RDP #Ubuntu #Windows

---

### **Definition**

Configuring remote desktop settings to enhance security, including disabling if unnecessary or enforcing strong authentication.

### **Ubuntu/Linux**

- **Disable Remote Desktop Services:**
    - If using VNC or similar, stop and disable the service.
- **Secure VNC Connections:**
    - Use encrypted protocols like SSH tunneling.
- **Restrict Access:**
    - Configure firewall rules to limit access to trusted IPs.

### **Windows**

- **Disable Remote Desktop if Not Needed:**
    - Go to **System Properties > Remote** tab and select **Don't allow remote connections**.
- **Enforce Network Level Authentication (NLA):**
    - Ensure **Allow connections only from computers running Remote Desktop with Network Level Authentication** is checked.
- **Change Default RDP Port:**
    - Modify the port in the registry under `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Terminal Server\WinStations\RDP-Tcp\PortNumber`.
- **Restrict Users:**
    - Limit Remote Desktop access to specific user accounts.

### **Advantages**

- **Prevents Unauthorized Access:** Secures a common attack vector.
- **Enhanced Authentication:** NLA adds an extra layer of security.

### **Disadvantages**

- **Configuration Complexity:** Changing default ports and settings can be error-prone.
- **Accessibility Issues:** Over-restriction may block legitimate access.

### **Related Notes**

- [[Check for Unsecured Remote Connections]]
- [[Configure Firewall Rules]]
- [[Implement Two-Factor Authentication (2FA)]]