**Tags:** #Security #AnonymousAccess #Ubuntu #Windows

---

### **Definition**

Limiting or disabling anonymous access to services and resources to prevent unauthorized activities.

### **Ubuntu/Linux**

- **Samba Shares:**
    - Edit `/etc/samba/smb.conf` and set `guest ok = no` for shares.
- **FTP Services:**
    - Configure `/etc/vsftpd.conf` or equivalent to disable anonymous FTP.
- **System Settings:**
    - Ensure services do not allow guest or anonymous logins.

### **Windows**

- **Local Security Policy:**
    - Open **secpol.msc**, navigate to **Local Policies > Security Options**.
- **Restrict Anonymous Access:**
    - Set **Network access: Do not allow anonymous enumeration of SAM accounts and shares** to **Enabled**.
- **Registry Edit:**
    - Modify `HKLM\SYSTEM\CurrentControlSet\Control\Lsa` and set `RestrictAnonymous` to `1` or `2`.

### **Advantages**

- **Security Enhancement:** Prevents unauthorized users from accessing system information.
- **Compliance:** Meets security standards requiring authenticated access.

### **Disadvantages**

- **Service Interruption:** May affect legitimate services relying on anonymous access.
- **Configuration Complexity:** Requires careful planning to avoid disruptions.

### **Related Notes**

- [[Disable Guest Accounts]]
- [[Implement Account Auditing]]
- [[Secure Shared Folders and Permissions]]