**Tags:** 

---

### **Definition**

Cache poisoning is a type of cyberattack where an attacker injects false or malicious data into a cache, causing the system to serve incorrect information to users. In the context of DNS (Domain Name System), DNS cache poisoning involves corrupting the DNS resolver's cache with incorrect IP addresses, leading users to malicious websites instead of legitimate ones.

### **Types**

- **DNS Cache Poisoning:** Alters DNS records to redirect traffic.
- **Web Cache Poisoning:** Injects malicious content into web caches to serve compromised pages to users.

### **Prevention**

- **DNSSEC:** Adds cryptographic signatures to DNS data to ensure integrity.
- **Randomized Source Ports:** Makes it harder for attackers to predict transaction IDs.
- **Strict Validation:** Ensure that only legitimate data is cached.

### **Impact**

- **Phishing Attacks:** Redirect users to fake websites to steal credentials.
- **Malware Distribution:** Serve malicious software from trusted domains.
- **Service Disruption:** Cause denial of service by redirecting traffic.

### **Real-World Examples**

- **Kaminsky Attack (2008):** Exploited DNS vulnerabilities to perform cache poisoning.
- **Cloudflare Incident (2017):** Highlighted the importance of DNS security measures.

### **Related Notes**

- DNS Zone Transfer
- Firewalls and Network Security
- Google Dorking