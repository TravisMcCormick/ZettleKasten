**Tags:** 

---

### **Definition**

A DNS Zone Transfer is the process of copying DNS records from a primary DNS server to a secondary DNS server. This ensures consistency and redundancy in DNS data across multiple servers, enhancing reliability and load distribution.

### **How It Works**

- **AXFR (Full Zone Transfer):** Transfers the entire DNS zone file from primary to secondary server.
- **IXFR (Incremental Zone Transfer):** Transfers only the changes made since the last update.

### **Security Risks**

- **Information Disclosure:** Attackers can obtain detailed DNS records, aiding in reconnaissance.
- **Amplification Attacks:** Misconfigured servers can be used in DNS amplification for DDoS attacks.

### **Prevention**

- **Restrict Zone Transfers:** Limit transfers to authorized secondary DNS servers.
- **Use TSIG (Transaction SIGnature):** Authenticate DNS messages to secure zone transfers.
- **Firewall Rules:** Block unauthorized access to DNS servers on port 53.

### **Tools**

- **dig:** Command-line tool to perform DNS queries and zone transfers.
- **host:** Simplified DNS lookup utility.
- **dnssec-tools:** Suite for securing DNS operations.

### **Related Notes**

- DNS Cache Poisoning
- Firewalls and Network Security
- Top-Level Domains (TLDs)