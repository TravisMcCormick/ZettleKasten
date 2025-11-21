
----
### Definition

A **TURN (Traversal Using Relays around NAT) Server** is a relay server that passes audio, video, and/or data between two peers when direct P2P connectivity fails (e.g., symmetric NAT, strict firewall).

### Purpose
- Provides a **relay candidate** for ICE.
- Guarantees connectivity even if host or server-reflexive candidates don’t work.

### How It Works (Briefly)

1. Client sends an Allocate Request to the TURN server (with credentials).
2. TURN server responds with a relay address/port pair that the client can use.
3. Client includes that relay address as an ICE candidate.
4. If no direct route is possible, both peers send all media/data through this TURN relay.

### Configuration Example

```js
const iceConfig = {
  iceServers: [
    {
      urls: "turn:turn.example.com:3478",
      username: "username",
      credential: "password"
    }
  ]
};
const pc = new RTCPeerConnection(iceConfig);

```

- Credentials can be static or dynamically generated (e.g., time-limited tokens).

### Trade-Offs
- **Latency & Cost:** All packets go through the TURN server → higher ping and bandwidth usage (both CPU & network).
- **Reliability:** Ensures connectivity under almost any NAT/firewall scenario.
- **Security:** Data is relayed over DTLS, so it remains encrypted end-to-end (TURN only forwards encrypted packets).

---
## Related Notes:
- [[WebRTC]]
- [[ICE Candidate]]