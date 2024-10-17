**Tags:** #Security #Services #Processes #Ubuntu #Windows

---

### **Definition**

Identifying and stopping services and processes that are not authorized or necessary, which could pose security risks.

### **Ubuntu/Linux**

- **List Running Processes:**
    - Use `ps aux` or `top` to view processes.
- **Identify Unfamiliar Processes:**
    - Research unknown processes to determine legitimacy.
- **Manage Services:**
    - List services with `sudo systemctl list-units --type=service`.
    - Stop a service using `sudo systemctl stop servicename`.
    - Disable a service with `sudo systemctl disable servicename`.

### **Windows**

- **View Processes:**
    - Open **Task Manager** (Ctrl+Shift+Esc) and review running processes.
- **Check Services:**
    - Use **services.msc** to view and manage services.
- **Research Unknown Entries:**
    - Investigate unfamiliar services or processes online.
- **Disable Unwanted Services:**
    - Right-click the service, select **Properties**, and set **Startup type** to **Disabled**.

### **Advantages**

- **Reduces Attack Surface:** Eliminates potential backdoors and malicious programs.
- **Improves Performance:** Frees up system resources.

### **Disadvantages**

- **System Instability:** Disabling essential services can cause issues.
- **Time-Consuming:** Requires careful analysis of each service and process.

### **Related Notes**

- [[Disable Unnecessary Network Services]]
- [[Audit Installed Applications]]
- [[Perform Vulnerability Scanning]]