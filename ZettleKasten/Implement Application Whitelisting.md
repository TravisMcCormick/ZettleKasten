**Tags:** #Security #ApplicationWhitelisting #Ubuntu #Windows

---

### **Definition**

Restricting system execution to only allow applications that are explicitly permitted, blocking all others by default.

### **Ubuntu/Linux**

- **Using AppArmor:**
    - Create strict profiles that only allow specific applications to run.
- **Using SELinux:**
    - Define policies that restrict executable files to a whitelist.
- **Third-Party Tools:**
    - Employ tools like **OSSEC** for additional control.

### **Windows**

- **Use AppLocker (Available in Enterprise and Education editions):**
    - Open **Local Security Policy** (`secpol.msc`).
    - Navigate to **Application Control Policies > AppLocker**.
    - Create rules for **Executable Rules**, **Windows Installer Rules**, **Script Rules**, and **DLL Rules**.
    - Set default policies to deny all, then create allow rules for trusted applications.
- **Software Restriction Policies:**
    - Use **Group Policy Editor** to set policies under **Computer Configuration > Windows Settings > Security Settings > Software Restriction Policies**.

### **Advantages**

- **Security Control:** Prevents unauthorized or malicious software from running.
- **Policy Enforcement:** Ensures only vetted applications are used.

### **Disadvantages**

- **Administrative Overhead:** Requires maintenance as applications update or change.
- **User Frustration:** May block legitimate software if not configured properly.

### **Related Notes**

- [[Implement SELinux or AppArmor (Linux)]]
- [[Audit Installed Applications]]
- [[Enable Logging and Auditing]]