**Tags:** #Linux #Systemd #ServiceManagement #DevOps #SystemAdministration

---

### Definition

**Installing Systemd Unit Files** is the process of deploying custom service definitions to systemd, the init system and service manager for Linux. This enables applications to run as system services with automatic startup, restart, and lifecycle management.

### Installation Process

Place your custom service unit (e.g. `app.service`) in `/etc/systemd/system/`, then set correct ownership and permissions so systemd can read it:

1. Copy the unit file:
```bash
sudo cp app.service /etc/systemd/system/
```

2. Ensure it’s owned by root and world-readable:
```bash
sudo chown root:root /etc/systemd/system/app.service
sudo chmod 644 /etc/systemd/system/app.service
```

3. Reload the systemd daemon to register new or updated units:
```bash
sudo systemctl daemon-reload
```

4. Enable the service to start on boot:
```bash
sudo systemctl enable app.service
```

5. Start the service immediately and verify its status:
```bash
sudo systemctl start  myapp.service
sudo systemctl status myapp.service
```

### Key Concepts

- **Unit Files**: Configuration files that define services, sockets, timers, etc.
- **daemon-reload**: Required after any unit file changes
- **enable vs start**: Enable sets startup on boot; start activates immediately
- **Permissions**: Files must be owned by root and readable (644)

### Personal Insight

Systemd unit files are the standard way to manage services on modern Linux distributions. Understanding systemd is essential for deploying and managing server applications reliably. Proper unit file configuration ensures services restart on failure and start automatically on boot.

---

### Related Notes

- [[Infrastructure as Code]]
- [[DevOps Practices]]