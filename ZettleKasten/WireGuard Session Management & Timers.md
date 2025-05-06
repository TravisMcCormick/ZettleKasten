
---
WireGuard appears stateless externally; internal timers manage handshake retries (every 5 s), keepalives (every 10 s), initiation if silent (120 s), and reinitiation if no authenticated packets (15 s). All events are deterministic and fully defined.

---
### **Related notes:**  
- [[WireGuard Key Exchange – Noise_IK Handshake]]