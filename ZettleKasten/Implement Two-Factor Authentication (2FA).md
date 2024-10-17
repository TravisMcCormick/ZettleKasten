**Tags:** #Security #Authentication #Ubuntu #Windows

---

### **Definition**

Adding an extra layer of security by requiring two forms of identification before granting access.

### **Ubuntu/Linux**

- **Install 2FA Module:**
    - Use `sudo apt install libpam-google-authenticator`.
- **Configure User Accounts:**
    - Run `google-authenticator` for each user to set up.
- **Modify PAM Configuration:**
    - Edit `/etc/pam.d/sshd` and add `auth required pam_google_authenticator.so`.
- **Configure SSH:**
    - Ensure `ChallengeResponseAuthentication yes` in `/etc/ssh/sshd_config`.
- **Restart SSH Service:**
    - Apply changes with `sudo systemctl restart sshd`.

### **Windows**

- **Use 2FA Solutions:**
    - Implement solutions like Microsoft Authenticator, Duo Security, or RSA SecureID.
- **Configure Remote Desktop:**
    - Integrate 2FA with RDP using third-party tools.
- **Active Directory:**
    - Enable 2FA for domain accounts using Azure AD or similar services.

### **Advantages**

- **Enhanced Security:** Significantly reduces risk of unauthorized access.
- **Compliance:** Meets higher security standards.

### **Disadvantages**

- **Complexity:** Requires additional setup and potential costs.
- **User Convenience:** May inconvenience users during authentication.

### **Related Notes**

- [[Secure SSH Configuration (Linux)]]
- [[Set Account Lockout Policies]]
- [[Implement Account Auditing]]