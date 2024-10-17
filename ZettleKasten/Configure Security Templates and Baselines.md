**Tags:** #Security #Templates #Baselines #Windows

---

### **Definition**

Using predefined security templates to establish a baseline configuration that meets security policies and best practices.

### **Windows**

- **Use Security Compliance Toolkit:**
    - Download from Microsoft's official site.
- **Import Templates:**
    - Open **Security Configuration and Analysis** snap-in.
    - Right-click and select **Open Database** to create a new database.
    - Import templates like **MSFT Security Baseline**.
- **Analyze System:**
    - Right-click **Security Configuration and Analysis** and select **Analyze Computer Now**.
- **Apply Security Settings:**
    - After analysis, select **Configure Computer Now** to apply settings.
- **Group Policy Integration:**
    - Import templates into Group Policy Objects (GPOs) for domain environments.

### **Advantages**

- **Standardization:** Ensures consistent security settings across systems.
- **Efficiency:** Saves time by applying predefined configurations.

### **Disadvantages**

- **Overriding Settings:** May conflict with existing configurations.
- **Complexity:** Requires careful planning to avoid issues.

### **Related Notes**

- [[Set Up Group Policies (Windows)]]
- [[Implement Application Whitelisting]]
- [[Enable Logging and Auditing]]