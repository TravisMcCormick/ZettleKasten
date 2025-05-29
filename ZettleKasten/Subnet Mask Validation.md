
---
Subnet mask validation rules:
1. Must contain exactly 4 octets
2. Each octet must be 0-255
3. Binary validation:
	- Converts to 32-bit binary
	- Must have continuous 1s followed by 0s
	- No 1s after 0s allowed
4. Error messages for:
	- Invalid subnet pattern
	- Invalid octet values
	- Missing octets

---