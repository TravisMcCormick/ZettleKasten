
---

### Definition

A **STUN (Session Traversal Utilities for NAT) Server** is a publicly reachable server that helps a client discover its public-facing IP address and port as seen from outside its network (i.e., beyond NAT).

### Purpose
- Generates **server-reflexive candidates** by replying to a STUN binding request.
- Tells a client “This is your IP:port as seen by me.”

### How It Works (Briefly)
1. Client sends a STUN Binding Request to the STUN server.
2. STUN server replies with a Binding Response containing the client’s public IP/port (the “mapped address”).
3. That mapped address is packaged as a server-reflexive ICE candidate.

### Typical Usage
- A typical `RTCPeerConnection` configuration:
```js
const iceConfig = {
  iceServers: [
    { urls: "stun:stun.l.google.com:19302" }
  ]
};
const pc = new RTCPeerConnection(iceConfig);
```
- The above STUN server tells your browser what your “public” IP looks like so ICE can share it with the remote peer.

### Limitations
- **No Relay:** If two peers are behind symmetric NATs, STUN won’t suffice → must use a [[TURN Server]].
- **No Authentication:** Public STUN servers are free and unauthenticated; they simply reply with your public-facing address.

---
### Related Notes:
- [[WebRTC]]
- [[ICE Candidate]]