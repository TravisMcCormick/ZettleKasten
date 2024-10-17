**Tags:** #Security #Encryption #Ubuntu #Windows

---

### **Definition**

Protecting data by converting it into a coded format, making it unreadable without the proper decryption key.

### **Ubuntu/Linux**

- **Encrypt Files with GnuPG:**
    - Encrypt: `gpg -c filename`.
    - Decrypt: `gpg filename.gpg`.
- **Use LUKS for Disk Encryption:**
    - Install: `sudo apt install cryptsetup`.
    - Encrypt Partition:
        - Unmount the partition.
        - Run `sudo cryptsetup luksFormat /dev/sdX`.
        - Open with `sudo cryptsetup luksOpen /dev/sdX name`.
- **Encrypt Home Directory:**
    - Use `ecryptfs-utils` to encrypt `/home` directories.

### **Windows**

- **Use BitLocker:**
    - Available on Pro and Enterprise editions.
    - Enable BitLocker:
        - Go to **Control Panel > System and Security > BitLocker Drive Encryption**.
        - Turn on BitLocker for desired drives.
- **Encrypt Files and Folders:**
    - Use **Encrypting File System (EFS)**:
        - Right-click the file/folder, select **Properties > Advanced**.
        - Check **Encrypt contents to secure data**.
- **Third-Party Tools:**
    - Use software like **VeraCrypt** for container encryption.

### **Advantages**

- **Data Protection:** Prevents unauthorized access to sensitive information.
- **Compliance:** Meets regulatory requirements for data security.

### **Disadvantages**

- **Performance Overhead:** May slightly reduce system performance.
- **Recovery Challenges:** Lost encryption keys can render data inaccessible.

### **Related Notes**

- [[Implement Two-Factor Authentication (2FA)]]
- [[Secure Database Services]]
- [[Backup Configurations]]