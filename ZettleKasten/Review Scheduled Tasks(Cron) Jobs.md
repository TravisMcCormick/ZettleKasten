**Tags:** #Security #ScheduledTasks #CronJobs #Ubuntu #Windows

---

### **Definition**

Examining automated tasks to ensure no unauthorized or malicious jobs are scheduled to run.

### **Ubuntu/Linux**

- **List User Cron Jobs:**
    - Run `crontab -l` for the current user.
- **List Root Cron Jobs:**
    - Use `sudo crontab -l`.
- **Check System-Wide Cron Directories:**
    - Review scripts in `/etc/crontab`, `/etc/cron.d/`, `/etc/cron.daily/`, etc.
- **Remove Unauthorized Jobs:**
    - Edit crontab with `crontab -e` and remove suspicious entries.

### **Windows**

- **Open Task Scheduler:**
    - Navigate to **Task Scheduler** via Start menu or **taskschd.msc**.
- **Review Task Library:**
    - Check tasks under **Task Scheduler Library** and its subfolders.
- **Identify Suspicious Tasks:**
    - Look for tasks with unknown origins or odd schedules.
- **Disable or Delete Tasks:**
    - Right-click the task and choose **Disable** or **Delete**.

### **Advantages**

- **Detects Malware:** Identifies scheduled tasks set by malware.
- **Optimizes Performance:** Removes unnecessary tasks consuming resources.

### **Disadvantages**

- **Risk of Disabling Critical Tasks:** May affect system functionality.
- **Requires Knowledge:** Needs understanding of normal system tasks.

### **Related Notes**

- [[Enable Logging and Auditing]]
- [[Audit Installed Applications]]
- [[Implement Account Auditing]]