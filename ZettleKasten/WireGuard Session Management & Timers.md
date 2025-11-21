
---
WireGuard appears stateless externally; internal timers manage handshake retries (everyÂ 5Â s), keepalives (everyÂ 10Â s), initiation if silent (120Â s), and reinitiation if no authenticated packets (15Â s). All events are deterministic and fully defined.

---
### **Related notes:**  
