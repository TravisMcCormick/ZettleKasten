**Tags:** #Security #PasswordPolicy #Ubuntu #Windows

---

### **Definition**

Setting rules for password complexity, expiration, and history to enforce the use of strong passwords.

### **Ubuntu/Linux**

- **Edit Login Definitions:**
    - Modify `/etc/login.defs` to set `PASS_MAX_DAYS`, `PASS_MIN_DAYS`, `PASS_WARN_AGE`.
- **Configure PAM Password Quality:**
    - Edit `/etc/pam.d/common-password`.
    - Use `pam_pwquality.so` with options like `minlen=12`, `dcredit=-1`, `ucredit=-1`, `ocredit=-1`, `lcredit=-1`.
- **Enforce Password History:**
    - Add `remember=5` to `pam_unix.so` in `common-password`.

### **Windows**

- **Access Local Security Policy:**
    - Open **secpol.msc**.
- **Navigate to Password Policy:**
    - Go to **Account Policies > Password Policy**.
- **Set Policies:**
    - **Enforce password history:** Set number of unique new passwords before reuse.
    - **Maximum/Minimum password age:** Define how long a password can be used.
    - **Minimum password length:** Set minimum character length.
    - **Password must meet complexity requirements:** Enable to enforce complexity.

### **Advantages**

- **Enhances Security:** Stronger passwords reduce risk of compromise.
- **Compliance:** Meets security standards and regulations.

### **Disadvantages**

- **User Inconvenience:** Complex passwords may be hard to remember.
- **Administrative Overhead:** May increase password reset requests.

### **Related Notes**

- [[Change Default Passwords]]
- [[Set Account Lockout Policies]]
- [[Disable Guest Accounts]]