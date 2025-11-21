**Tags:** #WebRTC #Networking #P2P #ICE #Connectivity

---

### Definition

An **ICE candidate** represents one possible “address” (IP address + port) that a peer can use to receive or send media/data. Each candidate offers a route through which two peers might communicate.

### Candidate Types

1. **Host Candidate:**
    
    - Derived from the client’s local network interfaces (e.g., `192.168.x.x:port`).
        
    - Lowest-latency route if both peers are on the same LAN.
        
2. **Server-Reflexive Candidate:**
    
    - Discovered by querying a [[STUN Server]].
        
    - Represents the client’s public IP address as seen by the STUN server (e.g., `203.0.113.45:34567`).
        
    - Useful when peers are behind NATs; often the best non-relay path through typical home/office NATs.
        
3. **Relay Candidate:**
    
    - Provided by a [[TURN Server]].
        
    - Falls back when direct connectivity fails (e.g., symmetric NAT, strict corporate firewall).
        
    - All media/data flows via the TURN server (higher latency, bandwidth cost).
        

### Gathering & Prioritization

- When an `RTCPeerConnection` is created, it immediately begins gathering host candidates from local interfaces.
    
- If a STUN server is configured, it also gathers server-reflexive candidates.
    
- If a TURN server is configured, relay candidates are requested.
    
- Each candidate is reported via the `onicecandidate` event.
    
- ICE prioritizes candidates in this order: host → server-reflexive → relay.
    

### Connectivity Checks

- Once both peers have exchanged SDP (offers/answers) and begun exchanging candidates via signaling, ICE connectivity checks (STUN binding requests) run in pairs: each local candidate is paired with each remote candidate.
    
- The first successful pair (where a STUN check succeeds) becomes the selected transport path (either direct P2P or via TURN).
    

### Why It Matters

- **Maximizing Direct Connections:** Host or server-reflexive candidates allow P2P paths, reducing latency and load.
    
- **Fallback Safety:** Relay candidates guarantee connectivity even under restrictive network conditions.
    
- **Dynamic Adaptation:** If network conditions change (e.g., Wi-Fi → cellular), ICE can perform a restart to gather new candidates.

---
### Related Notes:
- [[WebRTC]]
- [[STUN Server]]
- [[TURN Server]]
- [[P2P Connection]]