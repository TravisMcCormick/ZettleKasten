**Tags:** #Security #UserManagement #Ubuntu #Windows

---

### **Definition**

Turning off guest accounts to prevent anonymous access to the system.

### **Ubuntu/Linux**

- **Check for Guest Session:**
    - Verify if guest sessions are enabled in the display manager settings.
- **Disable Guest Account (LightDM):**
    - Edit `/etc/lightdm/lightdm.conf` and add `allow-guest=false`.
- **Disable Guest Account (GDM):**
    - Modify configurations in `/etc/gdm3/` to disable guest access.

### **Windows**

- **Disable Guest Account:**
    - Navigate to **Computer Management > Local Users and Groups > Users**.
    - Right-click **Guest** account and select **Properties**.
    - Check **Account is disabled**.
- **Group Policy Method:**
    - Use **gpedit.msc** and go to **Computer Configuration > Windows Settings > Security Settings > Local Policies > Security Options**.
    - Set **Accounts: Guest account status** to **Disabled**.

### **Advantages**

- **Enhanced Security:** Prevents unauthorized access without credentials.
- **Resource Management:** Reduces unnecessary system resource usage.

### **Disadvantages**

- **User Convenience:** May inconvenience legitimate users needing temporary access.
- **Administrative Overhead:** Requires alternative methods for guest access if needed.

### **Related Notes**

- [[Remove Unauthorized Users and Groups]]
- [[Configure Password Policies]]
- [[Set Account Lockout Policies]]