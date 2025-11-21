**Tags:** #Linux #Flatpak #Permissions #Configuration #Tools

---

### Definition

**Flatseal** is a graphical permissions manager for Flatpak applications on Linux. It provides an intuitive interface to view and modify the permissions and environment variables of installed Flatpak apps, offering fine-grained control over application sandboxing.

### Use Cases

- **Permission Management**: Control filesystem access, network access, and device permissions for Flatpak apps
- **Environment Configuration**: Set custom environment variables for applications
- **Troubleshooting**: Fix application issues related to sandboxing or missing permissions
- **Security Hardening**: Restrict application capabilities beyond default settings

---

### ðŸ§­ Flatseal Setup Instructions

1. **Launch Flatseal**
    
    - Hit `Super` (Windows key) and type `Flatseal`
        
    - Open the app
        
2. **Select KTouch**
    
    - In the left sidebar, scroll and click on **`org.kde.ktouch`**
        
3. **Scroll to â€œEnvironmentâ€**
    
    - Look in the right pane
        
    - Scroll down until you see the **â€œEnvironmentâ€** section
        
4. **Add the Variable**
    
    - Click the **â€œAddâ€** button (+ icon)
        
    - In the **Name** field: type `QT_QPA_PLATFORM`
        
    - In the **Value** field: type `xcb`
        
    - Hit **Enter** or click outside the box to confirm
        
5. **Close Flatseal**
    
    - Just exit the application â€” it saves changes automatically
        
6. **Reboot or Log Out**
    
    - Restart your session (important, or the environment change wonâ€™t apply)
        

---

### ðŸ§ª Verification

After reboot:

bash

CopyEdit

`flatpak run org.kde.ktouch`

You should now be able to **type into KTouch** with no layout or input issues.

### Personal Insight

Flatseal is an essential tool for any Linux user running Flatpak applications. It demystifies the sandboxing model and provides the control needed to make applications work correctly while maintaining security boundaries.

---

### Related Notes

