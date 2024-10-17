**Tags:** #Security #Passwords #Ubuntu #Windows

---

### **Definition**

Changing default passwords for all user accounts, especially administrative accounts, to prevent unauthorized access and enhance system security.

### **Ubuntu/Linux**

- **Change Root Password:**
    - Run `sudo passwd root` to set a new root password.
- **Change User Passwords:**
    - Use `sudo passwd username` to change a specific user's password.
- **Enforce Password Change:**
    - Force users to change passwords on next login with `sudo chage -d 0 username`.

### **Windows**

- **Using Computer Management:**
    - Navigate to **Computer Management > Local Users and Groups > Users**.
    - Right-click a user and select **Set Password**.
- **Using Command Prompt:**
    - Open CMD as administrator.
    - Execute `net user username newpassword` to change a user's password.
- **Force Password Change at Next Logon:**
    - In user properties, check **User must change password at next logon**.

### **Advantages**

- **Improves Security:** Eliminates default or weak passwords that are easily exploitable.
- **Compliance:** Meets security policies and regulatory requirements.

### **Disadvantages**

- **User Inconvenience:** May cause login issues if not communicated properly.
- **Administrative Overhead:** Requires time to change and manage multiple passwords.

### **Related Notes**

- [[Configure Password Policies]]
- [[Set Account Lockout Policies]]
- [[Disable Guest Accounts]]