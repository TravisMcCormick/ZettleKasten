**Tags:** #Security #Databases #Ubuntu #Windows

---

### **Definition**

Hardening database servers like MySQL or PostgreSQL to protect data and prevent unauthorized access.

### **Ubuntu/Linux**

- **Change Default Credentials:**
    - Set strong passwords for root and other database users.
- **Restrict Network Access:**
    - Configure database to listen only on localhost.
    - Edit MySQL's `my.cnf` and set `bind-address = 127.0.0.1`.
- **Manage User Permissions:**
    - Grant the least privileges necessary for database users.
- **Regular Updates:**
    - Keep the database software updated with `sudo apt update && sudo apt upgrade`.
- **Enable SSL Connections:**
    - Configure the database to use SSL/TLS for client connections.

### **Windows**

- **Secure SQL Server:**
    - Use **SQL Server Configuration Manager** to manage network protocols.
- **Change Default Ports:**
    - Modify the listening port to something other than the default.
- **Implement Firewall Rules:**
    - Allow database traffic only from trusted hosts.
- **Use Windows Authentication:**
    - Integrate with Active Directory for user authentication.
- **Encrypt Data:**
    - Enable **Transparent Data Encryption (TDE)** for databases.

### **Advantages**

- **Data Protection:** Safeguards sensitive information stored in databases.
- **Access Control:** Limits who can interact with the database and how.

### **Disadvantages**

- **Performance Impact:** Security measures may affect database performance.
- **Complexity:** Requires specialized knowledge to configure securely.

### **Related Notes**

- [[Encrypt Sensitive Data]]
- [[Configure Firewall Rules]]
- [[Implement Two-Factor Authentication (2FA)]]