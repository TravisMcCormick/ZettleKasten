**Tags:** #Security #FilePermissions #Sharing #Ubuntu #Windows

---

### **Definition**

Reviewing and securing shared folders by setting appropriate permissions to prevent unauthorized access.

### **Ubuntu/Linux**

- **List Shared Folders (Samba):**
    - Check `/etc/samba/smb.conf` for shared directories.
- **Modify Permissions:**
    - Use `chmod` to set permissions, e.g., `chmod 700 /folder`.
    - Change ownership with `chown`, e.g., `sudo chown user:user /folder`.
- **Disable Unnecessary Shares:**
    - Comment out or remove share definitions in `smb.conf`.
- **Restart Samba Service:**
    - Run `sudo systemctl restart smbd`.

### **Windows**

- **View Shared Folders:**
    - Use **Computer Management > Shared Folders > Shares**.
- **Adjust Permissions:**
    - Right-click the folder, select **Properties > Sharing > Advanced Sharing > Permissions**.
    - Set permissions for specific users or groups.
- **Stop Sharing:**
    - Unshare the folder by unchecking **Share this folder**.
- **NTFS Permissions:**
    - Under **Security** tab, configure permissions for users and groups.

### **Advantages**

- **Data Protection:** Prevents unauthorized access to sensitive files.
- **Access Control:** Allows only intended users to access shared resources.

### **Disadvantages**

- **Accessibility Issues:** Over-restriction may block legitimate access.
- **Administrative Effort:** Requires ongoing management as users change.

### **Related Notes**

- [[Implement File and Folder Permissions]]
- [[Disable Unnecessary Network Services]]
- [[Enable Logging and Auditing]]