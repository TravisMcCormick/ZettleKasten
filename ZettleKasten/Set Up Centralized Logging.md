**Tags:** #Security #Logging #CentralizedLogging #Ubuntu #Windows

---

### **Definition**

Collecting logs from multiple systems into a single location for easier monitoring, analysis, and correlation.

### **Ubuntu/Linux**

- **Install Log Management Tools:**
    - Use **syslog-ng**, **rsyslog**, or **Graylog**.
- **Configure Remote Logging:**
    - Edit `/etc/rsyslog.conf` to forward logs to a central server.
    - Use `$ActionForwardDefaultTemplate` to define the format.
- **Set Up Log Server:**
    - Configure the central server to receive and store logs.
- **Security Measures:**
    - Encrypt log transmission with TLS.
    - Implement access controls on the log server.

### **Windows**

- **Use Windows Event Forwarding:**
    - Configure source computers to forward events.
    - Set up a collector computer to receive events.
- **Third-Party Solutions:**
    - Implement tools like **Splunk**, **ELK Stack (Elasticsearch, Logstash, Kibana)**, or **SolarWinds**.
- **Configure Subscription:**
    - Define which events to collect and how often.

### **Advantages**

- **Simplifies Monitoring:** Central location for log analysis.
- **Correlation of Events:** Easier to detect patterns or coordinated attacks.

### **Disadvantages**

- **Storage Requirements:** Requires significant disk space.
- **Security Risks:** Centralizing logs can be a target if not secured properly.

### **Related Notes**

- [[Enable Logging and Auditing]]
- [[Set Up Intrusion Detection Systems (IDS)]]
- [[Implement Account Auditing]]