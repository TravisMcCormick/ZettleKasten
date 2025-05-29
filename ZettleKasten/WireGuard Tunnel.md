
---
All EPNs and Transit Nodes establish a site-to-site WireGuard VPN for secure overlay. Key points:
- Peer keys managed by Intelenet initialization servers
- Config pushed dynamically when EPN boots
- Persistent keep-alive to maintain NAT mappings

This tunnel carries both control (API calls, metrics) and data plane (customer traffic).

---
### **Related Notes:**
- [[Wireguard]]