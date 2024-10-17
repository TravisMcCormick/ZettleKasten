**Tags:** #Security #AutoRun #AutoPlay #Ubuntu #Windows

---

### **Definition**

Turning off features that automatically execute programs from removable media to prevent malware infection.

### **Ubuntu/Linux**

- **Disable Auto-Mounting:**
    - Use **dconf-editor** to change settings under `org.gnome.desktop.media-handling`.
- **Modify fstab:**
    - Edit `/etc/fstab` to control mounting options.
- **Disable USB Autorun Scripts:**
    - Ensure no udev rules are set to execute scripts upon device insertion.

### **Windows**

- **Access AutoPlay Settings:**
    - Go to **Settings > Devices > AutoPlay**.
    - Turn off **Use AutoPlay for all media and devices**.
- **Group Policy Method:**
    - Open **gpedit.msc** and navigate to **Computer Configuration > Administrative Templates > Windows Components > AutoPlay Policies**.
    - Enable **Turn off AutoPlay** for all drives.
- **Registry Edit:**
    - Modify `NoDriveTypeAutoRun` value under `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer`.

### **Advantages**

- **Prevents Malware Execution:** Stops automatic running of potentially malicious programs.
- **Control:** Gives users choice over what runs on their system.

### **Disadvantages**

- **User Convenience:** May inconvenience users expecting automatic actions.
- **Complexity:** Registry edits can be risky if not done correctly.

### **Related Notes**

- [[Run Antivirus Scan]]
- [[Audit Installed Applications]]
- [[Configure Browser Security Settings]]