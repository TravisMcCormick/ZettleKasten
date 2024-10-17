**Tags:** #Security #Antivirus #Malware #Ubuntu #Windows

---

### **Definition**

Using antivirus software to scan and remove malware, viruses, and other malicious programs from the system.

### **Ubuntu/Linux**

- **Install ClamAV:**
    - Run `sudo apt install clamav` to install.
- **Update Virus Definitions:**
    - Execute `sudo freshclam`.
- **Scan System:**
    - Use `clamscan -r /` for a recursive scan of the entire system.
- **Scan Specific Directory:**
    - Run `clamscan -r /path/to/directory`.

### **Windows**

- **Windows Defender:**
    - Open **Settings > Update & Security > Windows Security > Virus & threat protection**.
    - Click **Quick scan** or **Scan options** for a full scan.
- **Third-Party Antivirus:**
    - Ensure the software is up-to-date.
    - Run a full system scan from the antivirus dashboard.

### **Advantages**

- **Detects Malware:** Identifies and removes known threats.
- **Protects Data:** Prevents data loss and theft.

### **Disadvantages**

- **Performance Impact:** Scans can be resource-intensive.
- **False Positives:** Legitimate files may be flagged incorrectly.

### **Related Notes**

- [[Update the System]]
- [[Check for Unauthorized Services and Processes]]
- [[Secure Shared Folders and Permissions]]