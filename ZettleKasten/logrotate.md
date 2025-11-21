**Tags:** #Linux #Logging #SystemAdministration #LogManagement #Utilities

---

### Definition

**logrotate** is a Linux utility to rotate, compress, and remove old log files on a schedule, preventing logs from growing indefinitely and consuming all available disk space.

### Key Features

- **Automatic Rotation**: Rotates logs based on size, time, or both
- **Compression**: Compresses old log files to save disk space
- **Retention Policies**: Automatically removes old logs after a specified period
- **Email Notifications**: Can email logs before deletion
- **Custom Scripts**: Execute pre/post-rotation scripts

### Configuration

- **Main Config**: `/etc/logrotate.conf`
- **Service Configs**: `/etc/logrotate.d/` directory for individual service configurations
- **Cron Integration**: Typically run daily via cron (`/etc/cron.daily/logrotate`)

### Common Options

- `daily/weekly/monthly`: Rotation frequency
- `rotate N`: Keep N rotated logs
- `compress`: Compress rotated logs with gzip
- `delaycompress`: Delay compression until next rotation
- `missingok`: Don't error if log file is missing
- `notifempty`: Don't rotate if log is empty

### Example Configuration

```
/var/log/myapp/*.log {
    daily
    rotate 7
    compress
    delaycompress
    missingok
    notifempty
}
```

### Personal Insight

logrotate is essential for any production Linux system. Proper log rotation prevents disk space exhaustion while maintaining enough historical data for troubleshooting. Understanding logrotate configuration is a fundamental system administration skill.

---

### Related Notes

- [[Integrated log management]]
- [[Linux Command Line Basics]]
- [[Monitoring and Logging]]