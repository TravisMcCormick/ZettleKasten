
---
systemd units can enhance service behavior through directives such as:
- **Dependency Management** (`After=…`, `Requires=…`): Control startup order and prerequisites (e.g. wait for network).
- **Restart Policies** (`Restart=…`, `RestartSec=…`): Automatically restart failed or exited services with configurable back-off.
- **Resource Control** (`CPUQuota=…`, `MemoryLimit=…`): Constrain CPU or memory usage per service.
- **Logging Integration** (`StandardOutput=journal`, `StandardError=journal`): Route output into the centralized journal.
- **User/Group Settings** (`User=…`, `Group=…`): Run under specific unprivileged accounts for isolation.
- **Environment Management** (`Environment=…`, `EnvironmentFile=…`): Define or load environment variables.
- **Timeouts & Watchdogs** (`TimeoutStartSec=…`, `WatchdogSec=…`): Fail or restart unresponsive services within a timeframe.
- **Target Binding** (`WantedBy=…`, `Alias=…`): Hook services into boot targets (e.g. `multi-user.target`).  

---
### **Related Notes:** 
- [[Native systemd service]]