
---

Multiplexing (MUX) and demultiplexing (DemUX) are techniques for combining multiple data streams into a single channel and then separating them at the receiver. In WebRTC, these concepts appear in two main contexts:

1. **Media Multiplexing (RTP):**
    - Multiple media tracks (e.g., audio + video) can be sent over a single RTP/UDP flow by using synchronization source (SSRC) identifiers.
    - **Muxing**: The sender tags each RTP packet with an SSRC.
    - **Demuxing**: The receiver inspects the SSRC field to route each packet to the appropriate media decoder (audio vs. video).
    
2. **DataChannel Multiplexing (SCTP over DTLS):**
    - WebRTC’s `RTCDataChannel` streams run over an SCTP association, which itself is tunneled over a single DTLS connection on top of the ICE‐negotiated transport.
    - **MUX:** Multiple independent data channels (each with its own stream ID) share the same SCTP association and DTLS session.
    - **DemUX:** On receipt, the SCTP layer reads the stream ID from packet headers and delivers payloads to the correct `RTCDataChannel` instance.


- **Why It Matters:**
    - **Efficiency:** One UDP port and one DTLS handshake suffice for multiple media tracks and data channels.
    - **Simplicity:** Firewalls/NATs see only a single transport flow for all WebRTC traffic per peer connection.

---
### Related Notes:
- [[P2P Connection]] to understand how, once ICE negotiation completes, all the multiplexed streams share that secure, peer-to-peer channel.