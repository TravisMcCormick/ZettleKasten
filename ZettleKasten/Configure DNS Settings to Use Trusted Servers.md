**Tags:** #Security #DNS #Ubuntu #Windows

---

### **Definition**

Setting the system to use reliable and secure DNS servers to prevent DNS spoofing and improve security.

### **Ubuntu/Linux**

- **Edit Resolv.conf:**
    - Modify `/etc/resolv.conf` to include trusted DNS servers:
        - `nameserver 8.8.8.8` (Google Public DNS)
        - `nameserver 1.1.1.1` (Cloudflare DNS)
- **Make Changes Permanent:**
    - Since `/etc/resolv.conf` can be overwritten, edit `/etc/network/interfaces` or NetworkManager settings.
- **Use DNS over TLS/HTTPS:**
    - Install `stubby` or configure `systemd-resolved` for DNS over TLS.

### **Windows**

- **Change Adapter Settings:**
    - Go to **Control Panel > Network and Internet > Network Connections**.
    - Right-click the network adapter, select **Properties**.
    - Select **Internet Protocol Version 4 (TCP/IPv4)**, click **Properties**.
    - Under **Preferred DNS server**, enter trusted DNS IPs.
- **Use Secure DNS:**
    - Enable DNS over HTTPS in browsers or system settings if supported.

### **Advantages**

- **Security Improvement:** Protects against DNS spoofing and cache poisoning.
- **Reliability:** Trusted servers are more likely to be up-to-date and secure.

### **Disadvantages**

- **Dependency:** Relies on external DNS providers.
- **Privacy Concerns:** DNS queries may be logged by the DNS provider.

### **Related Notes**

- [[Update Hosts File]]
- [[Implement Network Segmentation]]
- [[Secure Remote Desktop Settings]]