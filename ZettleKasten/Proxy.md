
---

A proxy server is an intermediary that forwards requests from clients to target servers and returns responses back to clients. Unlike NAT—which rewrites IP headers at the network layer—proxies typically operate at higher protocol layers (HTTP, HTTPS, SOCKS). Key aspects:

- **Types of Proxies:**
    1. **Forward Proxy:**
        - Clients explicitly configure or direct traffic to the proxy (e.g., HTTP proxy at corporate networks).
        - Proxy receives a request from a client, fetches resources from the internet, then forwards them back.
        
    2. **Reverse Proxy:**
        - Sits in front of one or more servers; external clients connect to the proxy, which then forwards to backend servers (e.g., load balancers).
        
    3. **SOCKS Proxy (v5):**
        - Tunnels arbitrary TCP (and sometimes UDP) traffic, not limited to HTTP/HTTPS.
        
- **Differences from NAT:**
    - NAT translates and forwards IP packets without requiring client awareness (transparent).
    - Proxy generally requires client configuration or explicitly supports certain protocols (e.g., HTTP CONNECT).
    
- **Interaction with WebRTC:**
    - Signaling messages often pass through HTTP or WebSocket-based proxies without issue.
    - Media traffic (RTP/ICE) may be blocked if proxies do not support UDP or port forwarding.
    - In restrictive environments, WebRTC may need a [[TURN Server]] relay to bypass proxy restrictions.
    

---
### Related Notes:
- [[NAT]] for IP‐level address translation; proxies operate above that layer and often require special handling.