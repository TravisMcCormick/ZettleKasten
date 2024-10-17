**Tags:** #Security #BIOS #UEFI #Ubuntu #Windows

---

### **Definition**

Protecting the system's firmware settings to prevent unauthorized changes that could compromise system security.

### **Ubuntu/Linux and Windows**

- **Access BIOS/UEFI Settings:**
    - Restart the computer and press the key indicated (e.g., F2, Del) during boot.
- **Set Administrator Password:**
    - Navigate to the security tab and set a strong password.
- **Disable Boot from External Devices:**
    - Change boot order to prioritize internal drives.
- **Enable Secure Boot:**
    - Activates firmware-level validation of bootloaders and OS kernels.
- **Enable TPM (if available):**
    - Trusted Platform Module can enhance security features like BitLocker.

### **Advantages**

- **Prevents Unauthorized Access:** Stops attackers from altering boot settings.
- **Enhances Boot Security:** Secure Boot helps prevent rootkits and bootkits.

### **Disadvantages**

- **Risk of Lockout:** Forgotten BIOS passwords can be difficult to reset.
- **Compatibility Issues:** Secure Boot may prevent booting of unsigned operating systems.

### **Related Notes**

- [[Encrypt Sensitive Data]]
- [[Set Account Lockout Policies]]
- [[Disable Auto-Run and Auto-Play Features]]