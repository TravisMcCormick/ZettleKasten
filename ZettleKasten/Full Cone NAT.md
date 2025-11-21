**Tags:** #Networking #NAT #WebRTC #Connectivity

---

### Definition

A **Full Cone NAT** (sometimes called "oneâ€toâ€one NAT") is the least restrictive NAT behavior. Its characteristics include:

- **Static Mapping:**  
    Once an internal host (e.g., 192.168.1.10:5000) sends a packet to any destination, the NAT device creates a publicâ€facing mapping (e.g., 203.0.113.5:62000). All external hosts can use that single mapping (203.0.113.5:62000) to send data back to the internal host.
    
- **Behavior:**
    1. _Internalâ†’External:_ 192.168.1.10:5000 â†’ NAT â†’ 203.0.113.5:62000 â†’ external server=
    2. _Externalâ†’Internal:_ Any external IP can send to 203.0.113.5:62000 and the NAT device will forward it to 192.168.1.10:5000.
    
- **Implications for WebRTC:**
    - Easiest NAT type for WebRTC P2P: once a [[STUN Server]] reveals the serverâ€reflexive candidate, peers can often connect directly.
    - No need for a [[TURN Server]] fallback if both ends are behind full cone NATs.

Contrast this with more restrictive NAT types (e.g., symmetric NAT), which block unsolicited inbound packets and often require a TURN relay.

### Personal Insight

Full Cone NAT is the most WebRTC-friendly NAT type, as it allows direct peer-to-peer connections without relays. However, it's also less secure than more restrictive NAT types, which is why it's becoming less common in modern networks.

---

### Related Notes

- [[NAT]]
- [[STUN Server]]
- [[TURN Server]]
- [[Network Address Translation (NAT)]]
- [[ICE Candidate]]
