**Tags:** #Security #GroupPolicy #Windows

---

### **Definition**

Using Group Policy to enforce security settings and configurations across multiple computers in a Windows environment.

### **Windows**

- **Access Group Policy Editor:**
    - Open **gpedit.msc**.
- **Configure Policies:**
    - Navigate through **Computer Configuration** and **User Configuration** to set policies.
- **Common Security Policies:**
    - Password policies, account lockout, software restrictions, and audit policies.
- **Apply Policies:**
    - Policies are applied automatically; use `gpupdate /force` to enforce immediately.
- **Group Policy Management:**
    - In domain environments, use **Group Policy Management Console (GPMC)**.

### **Advantages**

- **Centralized Management:** Easily enforce settings across multiple systems.
- **Consistency:** Ensures all systems adhere to security policies.

### **Disadvantages**

- **Complexity:** Requires understanding of Group Policy mechanics.
- **Potential Conflicts:** Improper settings can cause system issues.

### **Related Notes**

- [[Configure Password Policies]]
- [[Implement Application Whitelisting]]
- [[Disable Unnecessary Network Services]]