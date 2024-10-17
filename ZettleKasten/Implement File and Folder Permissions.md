**Tags:** #Security #Permissions #FileSystem #Ubuntu #Windows

---

### **Definition**

Setting appropriate permissions on files and directories to control access and prevent unauthorized actions.

### **Ubuntu/Linux**

- **View Permissions:**
    - Use `ls -l` to list files with permissions.
- **Change Permissions:**
    - Use `chmod`, e.g., `chmod 750 filename`.
- **Change Ownership:**
    - Use `chown`, e.g., `sudo chown user:group filename`.
- **Set Default Permissions with umask:**
    - Configure `umask` in `/etc/profile` or user-specific shell profiles.

### **Windows**

- **View Permissions:**
    - Right-click the file/folder, select **Properties > Security** tab.
- **Modify Permissions:**
    - Click **Edit** to change permissions for users or groups.
- **Advanced Settings:**
    - Use **Advanced** options to change ownership or set special permissions.
- **Inheritance:**
    - Configure whether permissions are inherited from parent folders.

### **Advantages**

- **Access Control:** Ensures only authorized users can access or modify files.
- **Data Integrity:** Protects sensitive information from unauthorized changes.

### **Disadvantages**

- **Complexity:** Misconfigurations can lead to access issues.
- **Administrative Overhead:** Requires ongoing management as users and files change.

### **Related Notes**

- [[Secure Shared Folders and Permissions]]
- [[Enable Logging and Auditing]]
- [[Implement Application Whitelisting]]