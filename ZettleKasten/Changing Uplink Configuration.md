
---

##### To change the uplink configuration in our system:
1. Navigate to Network Configuration page
2. Select "Uplink Config" from the left panel
3. Fill in the required fields:
	- IP Address (xxx.xxx.xxx.xxx format)
	- Subnet Mask (xxx.xxx.xxx.xxx format)
	- Default Gateway (must be in same network as IP)
	- Primary DNS
	- Secondary DNS (must be different from Primary)

##### The system validates:
- IP format and range (0-255 for each octet)
- Subnet mask validity (continuous 1s followed by 0s)
- Gateway compatibility with IP and subnet
- DNS format and uniqueness

##### After submission:
1. System applies configuration to enp1s0 interface
2. 5-second countdown for connectivity testing
3. Redirects to new IP address if successful

---
## Related Notes
- [[Network Configuration Layout]]
- [[IP Address Validation]]
- [[Subnet Mask Validation]]
- [[Gateway Validation Rules]]
- [[DNS Configuration]]
- [[Network Interface Management]]
- [[Configuration Error Handling]]