
---
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

---