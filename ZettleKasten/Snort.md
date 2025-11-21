**Tags:** #security #ids #ips #network-security #intrusion-detection

---

### **Definition**

**Snort** is an open-source network intrusion detection and prevention system (IDS/IPS) that performs real-time traffic analysis and packet logging on IP networks. It uses a rule-based language combining signature, protocol, and anomaly inspection methods to detect various attacks and probes.

### **Core Functions**

- **Packet Sniffing**: Captures network traffic in real-time
- **Packet Logging**: Records packets for later analysis
- **Intrusion Detection**: Identifies malicious traffic patterns
- **Intrusion Prevention**: Blocks detected threats (IPS mode)
- **Protocol Analysis**: Deep packet inspection
- **Content Matching**: Searches for specific patterns in packets

### **Operating Modes**

1. **Sniffer Mode**: Displays packets on the console
2. **Packet Logger Mode**: Logs packets to disk
3. **Network Intrusion Detection System (NIDS) Mode**: Analyzes traffic against rules
4. **Inline Intrusion Prevention System (IPS) Mode**: Actively blocks threats

### **Key Components**

- **Packet Decoder**: Processes different protocol layers
- **Preprocessors**: Normalize and prepare traffic for detection engine
- **Detection Engine**: Matches traffic against rule database
- **Logging and Alerting System**: Records and reports findings
- **Output Modules**: Formats output to various systems

### **Snort Rules**

- **Rule Header**: Action, protocol, source/destination IP and ports
- **Rule Options**: Detailed detection criteria
- **Community Rules**: Free community-maintained ruleset
- **Registered Rules**: Available 30 days after release
- **Subscriber Rules**: Real-time commercial ruleset

### **Rule Example Structure**
```
alert tcp any any -> any 80 (msg:"HTTP Traffic Detected"; sid:1000001;)
```

### **Preprocessors**

- **frag3**: IP fragmentation reassembly
- **stream5**: TCP stream reassembly
- **http_inspect**: HTTP protocol normalization
- **sfPortscan**: Port scan detection
- **reputation**: IP reputation-based filtering

### **Integration Capabilities**

- **SIEM Systems**: Splunk, QRadar, ArcSight
- **Databases**: MySQL, PostgreSQL
- **BASE**: Basic Analysis and Security Engine (web interface)
- **Snorby**: Ruby on Rails frontend
- **Barnyard2**: Output processor for fast logging

### **Advantages**

- Free and open-source
- Highly flexible rule language
- Extensive preprocessor support
- Active community support
- Cross-platform compatibility
- Lightweight and efficient
- Extensive documentation

### **Limitations**

- Requires tuning to reduce false positives
- Can be complex to configure properly
- Performance limitations on high-speed networks
- Rule management can be time-consuming
- Cannot detect encrypted traffic content
- Needs regular rule updates

### **Deployment Scenarios**

- **Network Tap**: Passive monitoring without impacting traffic
- **Inline Mode**: Active blocking as IPS
- **DMZ Monitoring**: Protecting public-facing services
- **Internal Network Monitoring**: Detecting lateral movement
- **Cloud Deployments**: Virtual instances for cloud infrastructure

### **Best Practices**

- Keep rules updated regularly
- Tune rules for your specific environment
- Use preprocessors appropriate for your traffic
- Monitor Snort performance and resource usage
- Implement proper logging and alerting
- Review alerts regularly to identify false positives
- Combine with other security tools (firewall, SIEM)
- Use IDS mode first, then transition to IPS when tuned

### **Snort 3**

The latest major version includes:
- Multi-threaded processing
- Improved plugin architecture
- Enhanced Lua scripting
- Better performance on modern hardware
- Simplified configuration

### **Related Notes**

- [[Intrusion Detection Systems (IDS)]]
- [[SIEM]]
- [[Firewalls and IDS Integration]]
- [[Network Traffic Analysis]]
- [[Packet Filtering Firewall]]
- [[Network Security Best Practices]]
- [[Splunk]]
- [[Wazuh]]
- [[Monitoring and Logging]]

