
---

WebRTC (Web Real-Time Communication) is an open-standard suite of browser APIs and protocols designed to create real-time, encrypted, peer-to-peer connections for audio, video, and arbitrary data—without requiring plugins. By offloading media/data exchange directly between clients, WebRTC minimizes latency and server costs.

---
## Definition & Goals
- **What It Is:**  
    A set of standardized browser interfaces (W3C) and communication protocols (IETF) that allow two (or more) endpoints to negotiate and maintain a secure P2P link for media and data.
	
- **Why It Exists:**
    1. **Plugin-Free Experience:** No need for Flash, Java applets, or proprietary software.
    2. **Low-Latency, Real-Time Streams:** Ideal for voice/video calls, screen sharing, live collaboration.
    3. **Built-In Security:** SRTP/DTLS encryption ensures confidentiality and integrity.
    4. **Peer-to-Peer:** Reduces server bandwidth by connecting endpoints directly (see [[P2P Connection]]).
    
- **Key Properties:**
    - **Peer-to-Peer:** Once signaling and NAT traversal are complete, media and data flow directly.
    - **Built-In Encryption:** All audio, video, and data channels use SRTP/DTLS by default—no unencrypted transport.
    - **Low Latency:** Designed for real-time interaction.
    - **Cross-Platform:** Supported by modern browsers (Chrome, Firefox, Edge, Safari) and many mobile clients.

---
## Core Components & Workflow

### 1. Media Capture (`getUserMedia()`)
- **Purpose:** Obtain the user’s camera and microphone streams.
- **Outcome:** A `MediaStream` object containing one or more `MediaStreamTrack` objects (audio & video).
- **Next Step:** Attach these tracks to a peer connection to send over the network.

### 2. Signaling (App-Defined)
- **Role:** Exchange Session Description Protocol (SDP) “offers”/“answers” and ICE candidates between peers.
- **Mechanism:** You choose or implement a lightweight server (e.g., WebSocket, HTTP API).
- **Note:** Signaling is separate from WebRTC’s core; it merely carries negotiation data so peers know how to connect.

### 3. Peer Connection (`RTCPeerConnection`)
#### **Instantiation:**
```js
const pc = new RTCPeerConnection({
  iceServers: [
    { urls: "stun:stun.l.google.com:19302" },  
    {
      urls: "turn:turn.mycompany.com:3478",
      username: "user",
      credential: "pass"
    }
  ]
});
```

#### **Responsibilities:**
1. **NAT Traversal:** Orchestrates ICE gathering (host, server-reflexive, relay) to traverse NATs (see [[NAT]] and [[ICE Candidate]]).
2. **Media/Data Transport:** Once ICE negotiation succeeds, uses SRTP for audio/video and DTLS/SCTP for data channels.
3. **Muxing:** Combines multiple media tracks and data channels over a single transport (see [[MUX & DemUX]]).
4. **Security:** Auto-generates ephemeral DTLS certificates; fingerprints are exchanged via SDP.
    
#### **Typical Connection Flow:**
1. **Add Local Tracks:**
```js
const localStream = await navigator.mediaDevices.getUserMedia({ video: true, audio: true });
localStream.getTracks().forEach(track => pc.addTrack(track, localStream));
```

2. **Create & Send Offer:**
```js
const offer = await pc.createOffer();
await pc.setLocalDescription(offer);
// Send `offer.sdp` + `offer.type` via signaling
```

3. **Receive & Apply Answer:**
```js
// When signaling delivers peer’s answer SDP:
await pc.setRemoteDescription(answer);
```

4. **Exchange ICE Candidates (Trickle ICE):**
```js
pc.onicecandidate = event => {
  if (event.candidate) {
    // Send candidate via signaling
  }
};
// When a remote candidate arrives via signaling:
await pc.addIceCandidate(new RTCIceCandidate(remoteCandidate));
```

5. **ICE Checks & Connection Establishment:**
	- ICE pairs host ↔ host, host ↔ server-reflexive (via [[STUN Server]]), then host ↔ relay (via [[coTURN]]) based on priority.
	- Once a valid path is found (even through a [[Proxy]] if necessary), `pc.onconnectionstatechange` moves to “connected.”

### 4. Data Channels (`RTCDataChannel`)
#### **Creation:**
- **Initiator:**
```js
const dc = pc.createDataChannel("chat");
```

- **Receiver:**
```js
pc.ondatachannel = event => {
  const dc = event.channel;
  dc.onopen = () => { /* ready to send/receive */ };
};
```

- **Multiplexing:** Multiple data channels share the same SCTP/DTLS tunnel, which in turn rides on ICE’s single UDP transport (see [[MUX & DemUX]]).
- **Use Cases:** File transfer, text chat, game state sync, IoT telemetry.

---
## NAT & Proxy Considerations
- **NAT Types (see [[Full Cone NAT]]):**
    - Full Cone NAT is the most permissive: once a mapping is established, any external host can send packets back.
    - Other NAT types (restricted or symmetric) may block unsolicited traffic, requiring a TURN relay (see [[coTURN]]).
    
- **Proxy Servers:**
    - May intercept HTTP/WebSocket-based signaling traffic.
    - UDP-based media may be blocked by certain forward or reverse proxies, forcing WebRTC to rely on [[coTURN]] for relay.
    - Proper network configuration (e.g., HTTP CONNECT or TURN over TCP/TLS) can help WebRTC traverse proxies.
    

---
## P2P Transport & Multiplexing
- **Peer-to-Peer Connection (see [[P2P Connection]]):**
    - After ICE negotiation, media (RTP/RTCP) and data (SCTP) flow directly between peers under DTLS encryption.
    - No central media server required (unless building an SFU/MCU for group calls).
    
- **MUX & DemUX (see [[MUX & DemUX]]):**
    - One UDP/TCP/TLS port carries:
        1. RTP packets for audio/video (tagged by SSRC).
        2. SCTP packets for data channels (tagged by stream IDs).
        
    - The DTLS layer ensures all packets remain encrypted in transit.

---
## Security & Deployment
- **Encrypted by Default:** SRTP and DTLS protect confidentiality and integrity.
- **Certificates:** Each `RTCPeerConnection` auto-generates an ephemeral cert; its fingerprint is embedded in SDP.
- **Secure Context Required:** Browsers allow `getUserMedia()` and `RTCPeerConnection` only on HTTPS or `localhost`.
- **TURN Server (coTURN):**
    - Acts as a relay if direct P2P fails.
    - Avoids “ICE timeout” scenarios within restrictive corporate networks or symmetric NATs.
    

---
## Related Notes:

- **[[WebRTC Metaphor]]** – A step-by-step analogy illustrating how peers meet in a hidden gazebo (signaling, ICE, STUN, TURN, P2P, etc.).
    
- **[[ICE Candidate]]** – Details on how WebRTC gathers and prioritizes host, server-reflexive (STUN), and relay (coTURN) candidates.
    
- **[[STUN Server]]** – Explains how STUN servers help peers discover their public IP/port behind a NAT.
    
- **[[coTURN]]** – A popular TURN server implementation providing relay candidates when direct connectivity fails.
    
- **[[P2P Connection]]** – Describes what happens once ICE and DTLS complete, establishing the direct transport channel.
    
- **[[MUX & DemUX]]** – Shows how multiple media tracks and data channels share a single encrypted transport.
    
- **[[NAT]]** & **[[Full Cone NAT]]** – Offer background on Network Address Translation types and their impact on connectivity.
    
- **[[Proxy]]** – Covers how HTTP/SOCKS proxies differ from NAT and how they can affect WebRTC traffic.