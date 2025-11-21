**Tags:** #networking #webrtc #turn #nat #relay-server

---

### **Definition**

**coTURN** is a widely used, open-source implementation of a TURN (Traversal Using Relays around NAT) server. Acting as a relay for media and data when direct peer-to-peer (P2P) connectivity fails, coTURN provides reliable fallback connectivity.

### **Key Features**

- **Allocation of Relay Candidates:**  
    Clients request an address/port pair from coTURN, which becomes a "relay" ICE candidate in WebRTC.
- **Authentication & Permissions:**  
    Supports long-term credentials (username/credential) or short-lived tokens to secure TURN allocations.
- **Scalability & Configuration:**  
    Administrators can deploy coTURN on their own infrastructure, configure SSL/TLS, set bandwidth limits, and integrate with existing authentication backends.

### **Use Case**

Use coTURN when you need a reliable fallback for peers behind restrictive NATs or firewalls that prevent direct peer-to-peer connections.

---

### **Related Notes**

- [[TURN Server]]
- [[coTURN Metaphor]]
- [[NAT]]
- [[ICE Candidate]]
- [[STUN Server]]
- [[WebRTC]]
- [[P2P Connection]]
- [[Network Address Translation (NAT)]]
