**Tags:** #Security #HostsFile #DNS #Ubuntu #Windows

---

### **Definition**

Reviewing and cleaning the hosts file to remove malicious entries that redirect traffic to undesirable sites.

### **Ubuntu/Linux**

- **Location of Hosts File:**
    - Located at `/etc/hosts`.
- **Edit Hosts File:**
    - Open with `sudo nano /etc/hosts`.
- **Identify Malicious Entries:**
    - Look for unfamiliar IP addresses or domains.
- **Clean Entries:**
    - Remove any unauthorized lines.
- **Save Changes:**
    - Save and exit the editor.

### **Windows**

- **Location of Hosts File:**
    - Found at `C:\Windows\System32\drivers\etc\hosts`.
- **Edit Hosts File:**
    - Open Notepad as administrator.
    - Open the hosts file and review contents.
- **Remove Unwanted Entries:**
    - Delete lines that are not default or recognized.
- **Save File:**
    - Save changes ensuring the file remains without an extension.

### **Advantages**

- **Corrects DNS Hijacking:** Ensures correct domain name resolutions.
- **Improves Security:** Prevents redirection to malicious sites.

### **Disadvantages**

- **Requires Caution:** Incorrect edits can disrupt network access.
- **Not a Permanent Solution:** Does not prevent future modifications by malware.

### **Related Notes**

- [[Run Antivirus Scan]]
- [[Configure DNS Settings to Use Trusted Servers]]
- [[Enable Logging and Auditing]]