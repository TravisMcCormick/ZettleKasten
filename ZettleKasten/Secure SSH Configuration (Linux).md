**Tags:** #Security #SSH #Ubuntu

---

### **Definition**

Enhancing the security of SSH (Secure Shell) by modifying its configuration to prevent unauthorized access.

### **Ubuntu/Linux**

- **Edit SSH Configuration:**
    - Open `/etc/ssh/sshd_config` with a text editor.
- **Disable Root Login:**
    - Set `PermitRootLogin no`.
- **Change Default Port:**
    - Modify `Port 22` to another unused port.
- **Allow Specific Users:**
    - Add `AllowUsers username` to restrict access.
- **Disable Password Authentication:**
    - Set `PasswordAuthentication no` and use key-based authentication.
- **Restart SSH Service:**
    - Apply changes with `sudo systemctl restart sshd`.

### **Advantages**

- **Reduces Attack Surface:** Changing defaults makes it harder for attackers.
- **Enhanced Authentication:** Key-based authentication is more secure than passwords.

### **Disadvantages**

- **Accessibility:** May complicate legitimate remote access.
- **Configuration Errors:** Incorrect settings can lock out administrators.

### **Related Notes**

- [[Check for Unsecured Remote Connections]]
- [[Configure Firewall Rules]]
- [[Implement Two-Factor Authentication (2FA)]]