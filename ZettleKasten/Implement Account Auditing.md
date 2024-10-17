**Tags:** #Security #Auditing #Ubuntu #Windows

---

### **Definition**

Monitoring and recording user account activities to detect unauthorized access or policy violations.

### **Ubuntu/Linux**

- **Configure Auditd:**
    - Ensure `auditd` is installed and running.
- **Set Audit Rules:**
    - Add rules in `/etc/audit/audit.rules` to monitor account-related files like `/etc/passwd` and `/etc/shadow`.
- **Monitor Login Events:**
    - Check logs in `/var/log/auth.log`.
- **Use Tools:**
    - Utilize `ausearch` and `auditctl` for analyzing audit logs.

### **Windows**

- **Set Audit Policies:**
    - Use **secpol.msc** and go to **Local Policies > Audit Policy**.
- **Enable Account Logon Events:**
    - Audit **Success** and **Failure** for **Audit Account Logon Events**.
- **Review Event Logs:**
    - Check **Security** logs in **Event Viewer** for Event IDs related to account activities.

### **Advantages**

- **Detects Unauthorized Access:** Alerts administrators to suspicious activities.
- **Compliance:** Meets regulatory requirements for monitoring.

### **Disadvantages**

- **Log Volume:** Generates large amounts of data to review.
- **Requires Analysis:** Needs tools or personnel to interpret logs.

### **Related Notes**

- [[Enable Logging and Auditing]]
- [[Set Account Lockout Policies]]
- [[Implement File and Folder Permissions]]