**Tags:** #nodejs #process-manager #devops #deployment #monitoring

---

### **Definition**

**PM2** is a production-grade process manager for Node.js applications. It runs as a daemon, keeps your apps alive forever, and provides a suite of features to make deploying and managing Node services in production easier and more reliable.

### **Key Features**

- **Process Management**
  - Automatically restarts crashed or unresponsive processes
  - Supports hot reloads and zero-downtime restarts via `pm2 reload`
  - Can run apps in cluster mode, spawning multiple worker processes to fully utilize multi-core CPUs

- **Logging & Monitoring**
  - Aggregates stdout/stderr logs, with built-in log rotation
  - Exposes a realtime monitoring dashboard (`pm2 monit`) showing CPU, memory, and uptime
  - Integrates with key metrics services and alerting tools

- **Deployment Automation**
  - Includes a simple zero-downtime deployment workflow (`pm2 deploy`) that can pull from git, build, and restart processes
  - Supports declarative "ecosystem" JSON/YAML files to define multiple apps, environment variables, and deployment targets

- **Ecosystem & Extensibility**
  - Plugins for metrics (Keymetrics), clustering, and watch-for-file-changes
  - Programmatic API for integrating process management into custom scripts or tooling

- **Integration with System Startup**
  - Generates and installs its own systemd (or upstart/launchd) startup script via `pm2 startup`, so your managed processes launch on machine boot

### **Summary**

PM2 sits between your Node processes and the OS's init system, providing advanced clustering, automatic recovery, logging, and deployment helpers—all in a single, easy-to-use tool.

---

### **Related Notes**

- [[zero-downtime reloads]]
- [[Integrated log management]]
- [[abstraction]]
- [[runtime process manager]]
- [[Monitoring and Logging]]
- [[DevOps Practices]]
- [[Continuous Deployment]]
- [[PM2 Help]]
