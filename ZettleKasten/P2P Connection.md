
---
### Definition

A **Peer-to-Peer (P2P) Connection** in WebRTC is the direct data path between two browsers (or apps) once ICE negotiation and DTLS encryption are complete.

---
### Characteristics
- **Direct Transport:** Media (audio/video) and data flow directly between endpoints without a central server (beyond the initial signaling and, if needed, TURN relay).
- **Low Latency:** Because there’s no intermediary (server), P2P typically has minimal delay.
- **Encryption:** All P2P traffic is encrypted (SRTP for media, DTLS for data).
- **Dynamic Path Selection:** The underlying network path is chosen dynamically by ICE (host → server-reflexive → relay).

---
### Lifecycle in WebRTC
1. **ICE Gathering:** Browser collects all local addresses ([[ICE Candidate]]).
2. **Signaling Exchange:** SDP “offer/answer” is exchanged, including ICE candidates (via out-of-band channel).
3. **ICE Connectivity Checks:** Peers test candidate pairs until a working path is found.
4. **DTLS Handshake:** Peers exchange certificates (fingerprints in SDP), establish encryption keys.
5. **Media/Data Flow:** Once DTLS is established, SRTP or SCTP channels carry media or data directly P2P.

---
### Benefits
- **Scalability:** Offloads media & data traffic from central servers.
- **Performance:** Lower end-to-end latency for real-time audio/video or data.
- **Cost-Efficiency:** No need for media servers except for edge cases (large group calls → SFU/MCU).

---
### When P2P Is Not Possible
- **Symmetric NATs or Corporate Firewalls:** Direct host or server-reflexive paths fail → ICE falls back to [[TURN Server]] relay.
- **Strict Network Policies:** Some enterprise networks block STUN/UDP traffic entirely → TURN is mandatory.

---
### Related Notes

- **[[WebRTC]]** — parent protocol suite (signaling, ICE, transports, and security).
- **[[WebRTC Metaphor]]** — narrative walkthrough of how the pieces fit together.