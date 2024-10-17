**Tags:** #Security #SELinux #AppArmor #Ubuntu #Linux

---

### **Definition**

Using Mandatory Access Control (MAC) systems like SELinux or AppArmor to enforce security policies that limit what resources applications can access.

### **SELinux (CentOS/RedHat)**

- **Check SELinux Status:**
    - Run `sestatus`.
- **Enable SELinux:**
    - Edit `/etc/selinux/config` and set `SELINUX=enforcing`.
- **Configure Policies:**
    - Use predefined policies or create custom ones.
- **Manage Booleans:**
    - Adjust settings with `setsebool`.

### **AppArmor (Ubuntu/Debian)**

- **Check AppArmor Status:**
    - Run `sudo apparmor_status`.
- **Enable AppArmor:**
    - Install with `sudo apt install apparmor apparmor-utils`.
- **Configure Profiles:**
    - Profiles are located in `/etc/apparmor.d/`.
    - Enforce a profile: `sudo aa-enforce /path/to/profile`.
- **Create Custom Profiles:**
    - Use `aa-genprof` to generate new profiles.

### **Advantages**

- **Enhanced Security:** Limits the damage from compromised applications.
- **Policy Enforcement:** Controls application behavior at a granular level.

### **Disadvantages**

- **Complexity:** Requires understanding of policy configurations.
- **Potential Compatibility Issues:** May interfere with normal application operations.

### **Related Notes**

- [[Implement Application Whitelisting]]
- [[Configure Firewall Rules]]
- [[Enable Logging and Auditing]]