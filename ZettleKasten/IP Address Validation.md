
---
IP address validation rules:
1. Must contain exactly 4 octets
2. Each octet must be:
	- A number between 0-255
	- Not empty
	- Valid integer
3. Auto-formatting:
	- Only allows digits and dots
	- Auto-adds dots after 3 digits
4. Error messages for:
	- Missing octets
	- Invalid numbers
	- Out of range values

---