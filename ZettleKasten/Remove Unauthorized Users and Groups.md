**Tags:** #Security #UserManagement #Ubuntu #Windows

---

### **Definition**

Identifying and deleting or disabling user accounts and groups that should not have access to the system.

### **Ubuntu/Linux**

- **List Users:**
    - View users with `cut -d: -f1 /etc/passwd`.
- **Delete User Accounts:**
    - Use `sudo deluser username` to remove a user.
- **Remove User and Home Directory:**
    - Execute `sudo deluser --remove-home username`.
- **List Groups:**
    - Check groups with `cut -d: -f1 /etc/group`.
- **Delete Groups:**
    - Remove a group using `sudo delgroup groupname`.

### **Windows**

- **Access Local Users and Groups:**
    - Open **Computer Management > Local Users and Groups**.
- **Delete Users:**
    - Right-click on the user and select **Delete**.
- **Disable Users:**
    - Right-click and choose **Properties**, then check **Account is disabled**.
- **Review Groups:**
    - Check group memberships and remove unauthorized users from groups like **Administrators**.

### **Advantages**

- **Reduces Risk:** Minimizes the attack surface by limiting access.
- **Compliance:** Aligns with the principle of least privilege.

### **Disadvantages**

- **Potential Lockouts:** Risk of removing necessary accounts if not carefully reviewed.
- **Administrative Effort:** Requires thorough verification of each account.

### **Related Notes**

- [[Disable Guest Accounts]]
- [[Implement Account Auditing]]
- [[Restrict Anonymous Access]]