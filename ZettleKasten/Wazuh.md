**Tags:** #security #siem #ids #hids #open-source #monitoring

---

### **Definition**

**Wazuh** is a free, open-source security platform that provides unified XDR (Extended Detection and Response) and SIEM capabilities. It offers host-based intrusion detection (HIDS), log analysis, file integrity monitoring, vulnerability detection, configuration assessment, and incident response capabilities.

### **Core Functions**

- **Host Intrusion Detection (HIDS)**: Monitors system activities and detects anomalies
- **Log Data Analysis**: Collects and analyzes logs from multiple sources
- **File Integrity Monitoring (FIM)**: Detects unauthorized file changes
- **Vulnerability Detection**: Identifies software vulnerabilities
- **Configuration Assessment**: Checks for security misconfigurations
- **Incident Response**: Automated threat response and remediation
- **Regulatory Compliance**: Assists with PCI-DSS, HIPAA, GDPR, SOC 2

### **Architecture Components**

1. **Wazuh Agent**:
   - Installed on monitored endpoints
   - Collects system and application data
   - Executes remote commands from manager
   - Available for Windows, Linux, macOS, Solaris

2. **Wazuh Manager**:
   - Central server receiving data from agents
   - Analyzes data using rules and decoders
   - Triggers alerts based on patterns
   - Stores alerts and archives

3. **Wazuh Indexer**:
   - Based on OpenSearch (Elasticsearch fork)
   - Stores and indexes security events
   - Provides search and analytics

4. **Wazuh Dashboard**:
   - Web interface for visualization
   - Based on OpenSearch Dashboards
   - Security analytics and reporting
   - Agent management interface

### **Key Capabilities**

#### **Intrusion Detection**
- Rootkit detection
- System call monitoring
- Process monitoring
- Registry monitoring (Windows)
- Real-time alerting

#### **Log Analysis**
- Syslog collection
- Windows Event Log analysis
- Application log parsing
- Custom log formats
- Log forwarding from network devices

#### **File Integrity Monitoring**
- Real-time file and directory monitoring
- Registry monitoring (Windows)
- Detects additions, deletions, modifications
- Reports who, what, when for changes

#### **Vulnerability Detection**
- CVE scanning
- Package vulnerability assessment
- Integration with vulnerability databases
- Automatic inventory of installed software

#### **Configuration Assessment**
- CIS benchmarks
- PCI-DSS requirements
- HIPAA compliance checks
- Custom policy enforcement
- Security best practices validation

#### **Cloud Security**
- AWS, Azure, GCP monitoring
- Container security (Docker, Kubernetes)
- Cloud infrastructure monitoring
- Cloud compliance assessment

### **Rule-Based Detection**

- **Decoders**: Parse incoming logs
- **Rules**: Define detection logic
- **Rule Levels**: Severity classification (0-15)
- **Custom Rules**: User-defined detection patterns
- **Rule Groups**: Organize rules by category

### **Integration Capabilities**

- **SIEM**: Can feed data to other SIEM platforms
- **VirusTotal**: Malware detection integration
- **MISP**: Threat intelligence platform
- **Slack/PagerDuty**: Alert notifications
- **Shuffle/TheHive**: SOAR integration
- **Fortigate, Cisco, Palo Alto**: Firewall log ingestion
- **Suricata/Snort**: IDS integration
- **YARA**: Malware scanning rules

### **Use Cases**

- Endpoint Detection and Response (EDR)
- Security Operations Center (SOC) operations
- Threat hunting and investigation
- Compliance monitoring and reporting
- Cloud workload protection
- Container and Kubernetes security
- Incident response automation
- Security configuration management

### **Advantages**

- Completely free and open-source
- No agent licensing costs
- Active community support
- Comprehensive documentation
- Supports multiple platforms
- Scalable architecture
- Extensive integration options
- Regular updates and improvements
- Built-in compliance frameworks

### **Deployment Options**

- **Standalone**: Single-server deployment
- **Distributed**: Separate manager, indexer, dashboard
- **Clustered**: Multiple managers for high availability
- **Cloud**: AWS, Azure, GCP deployments
- **Kubernetes**: Container-based deployment

### **Comparison with Commercial Solutions**

| Feature | Wazuh | Commercial SIEM |
|---------|-------|-----------------|
| Cost | Free | $$$$ |
| Agent Licensing | Free | Usually licensed |
| Customization | Full access | Limited |
| Community | Active | Vendor-only |
| Updates | Frequent | Scheduled |

### **Best Practices**

- Deploy agents on all critical systems
- Regularly update agents and manager
- Tune rules to reduce false positives
- Implement custom rules for specific environment
- Set up proper log retention policies
- Configure alert thresholds appropriately
- Integrate with ticketing systems
- Regular backup of configuration and data
- Monitor manager and indexer resources
- Use SSL/TLS for agent-manager communication

### **Common Configurations**

```xml
<!-- Enable FIM -->
<syscheck>
  <directories check_all="yes">/etc,/usr/bin</directories>
  <frequency>3600</frequency>
</syscheck>

<!-- Enable rootkit detection -->
<rootcheck>
  <frequency>3600</frequency>
</rootcheck>

<!-- Active response -->
<active-response>
  <command>firewall-drop</command>
  <location>local</location>
  <rules_id>5712</rules_id>
</active-response>
```

### **Performance Considerations**

- Agent resource usage: Minimal (typically <5% CPU, <100MB RAM)
- Manager sizing: Based on events per second (EPS)
- Indexer storage: Plan for log retention requirements
- Network bandwidth: Agent-manager communication
- Cluster for high-availability deployments

### **Limitations**

- Requires configuration and tuning
- Learning curve for rule creation
- Large deployments need clustering
- Dashboard can be complex for beginners
- Alert fatigue if not properly tuned

### **Related Notes**

- [[SIEM]]
- [[Intrusion Detection Systems (IDS)]]
- [[Splunk]]
- [[Snort]]
- [[Monitoring and Logging]]
- [[Incident Response Process]]
- [[Network Security Best Practices]]
- [[Enable Logging and Auditing]]

