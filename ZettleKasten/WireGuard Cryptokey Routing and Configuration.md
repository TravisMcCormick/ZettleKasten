
---
Cryptokey routing maps each peer’s public key to its allowed tunnel IPs. Config uses an INI format:

```
[Interface]
Address = 10.0.0.1/24
PrivateKey = <key>
ListenPort = 51820

[Peer]
PublicKey = <peer-key>
AllowedIPs = 10.0.0.0/24
Endpoint = peer.example.com:51820
PersistentKeepalive = 25
```

AllowedIPs serves as both routing and ACL; PersistentKeepalive counters NAT timeouts.

---
### **Related notes:**  
- [[WireGuard – Simplicity of Interface]]
- [[WireGuard – Static Structure]]