**Tags:** #Security #BruteForceProtection #Ubuntu #Windows

---

### **Definition**

Configuring policies that lock user accounts after a certain number of failed login attempts to protect against brute-force attacks.

### **Ubuntu/Linux**

- **Install Required Package:**
    - Ensure `libpam-pwquality` is installed using `sudo apt install libpam-pwquality`.
- **Configure PAM:**
    - Edit `/etc/pam.d/common-auth`.
    - Add `auth required pam_tally2.so deny=5 unlock_time=900` to lock out after 5 attempts for 15 minutes.
- **Reset Failed Login Attempts:**
    - Use `pam_tally2 --reset --user=username`.

### **Windows**

- **Access Local Security Policy:**
    - Open **secpol.msc**.
- **Navigate to Account Lockout Policy:**
    - Go to **Account Policies > Account Lockout Policy**.
- **Set Policies:**
    - **Account lockout threshold:** Set number of failed attempts (e.g., 5).
    - **Account lockout duration:** Define lockout period (e.g., 15 minutes).
    - **Reset account lockout counter after:** Set time to reset failed attempts.

### **Advantages**

- **Brute-Force Protection:** Mitigates risk of unauthorized access via password guessing.
- **Security Compliance:** Meets organizational security standards.

### **Disadvantages**

- **Denial of Service Risk:** Attackers could intentionally lock out accounts.
- **User Frustration:** May inconvenience users who forget passwords.

### **Related Notes**

- [[Configure Password Policies]]
- [[Implement Account Auditing]]
- [[Restrict Anonymous Access]]