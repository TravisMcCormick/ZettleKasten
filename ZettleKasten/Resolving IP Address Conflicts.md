**Tags**: #Networking #Troubleshooting

---

### Symptoms

- **Network Errors**: Messages about IP conflicts.
- **Connectivity Issues**: Unable to access network resources.

### Solutions

- **Renew IP Lease**:
    - **Windows**: `ipconfig /release` and `ipconfig /renew`.
    - **Linux/macOS**: `dhclient -r` and `dhclient`.
- **Restart Devices**: Reboot routers and computers.
- **Assign Static IPs**: Prevents conflicts by manual assignment.

### Related Notes

- [[Static IP Address]]
- [[Dynamic IP Address]]