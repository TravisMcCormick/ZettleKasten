
---
WireGuard ignores unauthenticated packets, responding only to valid crypto (mac1). Under DoS, it issues stateless cookies (mac2) derived from a rotating secret and initiator IP to prove liveness without storing per-peer state, preserving stealth and mitigating ECDH-based DoS.

---
### **Related notes:**  
