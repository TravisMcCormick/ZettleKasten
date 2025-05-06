
---
WireGuard exposes a standard network interface (e.g., wg0) managed via familiar tools (`ip link`, `ifconfig`, `iptables`). This breaks old layering assumptions by embedding cryptokey routing into the interface itself and avoiding complex transform tables.

---
### **Related notes:**  
- [[WireGuard Overview]]
- [[WireGuard Cryptokey Routing and Configuration]]