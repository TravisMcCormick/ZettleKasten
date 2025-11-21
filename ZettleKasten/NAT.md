**Tags:** #networking #nat #ip-addressing #router #network-address-translation

---

### **Definition**

**Network Address Translation (NAT)** is a method by which a router or firewall rewrites the IP headers of packets as they pass between a private (internal) network and a public (external) network.

### **Purpose**

1. **IPv4 Address Conservation**: Allows multiple hosts on a private LAN to share a single public IP address
2. **Basic Security**: Hides internal IP addresses from the outside world
3. **Network Flexibility**: Enables private network reorganization without external IP changes

### **Basic Operation**

- A private-addressed packet (e.g., 192.168.1.10:5000) is sent to the NAT device
- The NAT device replaces the source IP/port with its own public IP/port (e.g., 203.0.113.5:62000) and records the mapping
- When a reply arrives at 203.0.113.5:62000, NAT consults its table and forwards the packet back to 192.168.1.10:5000

### **Interaction with WebRTC**

- NAT complicates direct peer-to-peer connections because peers behind different NATs may not know each other's real public-facing addresses
- WebRTC uses ICE Candidate gathering (host, server-reflexive via STUN Server, and relay via TURN Server) to traverse NATs
- Types of NATs (e.g., Full Cone NAT) affect how easily peers can connect

---

### **Related Notes**

- [[Network Address Translation (NAT)]]
- [[Full Cone NAT]]
- [[ICE Candidate]]
- [[STUN Server]]
- [[TURN Server]]
- [[What is an IP Address]]
- [[Private IP Address]]
- [[Default Gateway]]
- [[WebRTC]]
- [[P2P Connection]]
