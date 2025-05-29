**Native systemd service**
- **Pros**
    - Minimal extra dependencies (leverages built-in systemd)
    - Precise startup ordering ([[systemd service features]])
    - Automatic restart/back-off ([[systemd service features]])
    - Centralized, structured logging via `journalctl` ([[systemd service features]])
    - Very low overhead and easy to configure
- **Cons**
    - No native clustering or load-balancing ([[clustering]], [[load-balancing]])
    - You must implement log rotation separately (e.g. with [[logrotate]])
    - Lacks higher-level process-management features ( [[health checks]], [[auto-reload]] )

---

**[[PM2]] (with systemd startup)**
- **Pros**
    - Built-in clustering and zero-downtime reloads ([[clustering]], [[zero-downtime reloads]])
    - Integrated log management (rotation, [[inspection]]) ([[Integrated log management]])
    - Memory-limit enforcement and process health checks ([[Memory-limit enforcement]], [[process health checks]])
    - Automatically generates and manages its own systemd unit ([[systemd service features]])
- **Cons**
    - Introduces an additional runtime dependency (PM2 + Node.js) ([[runtime dependency]])
    - Higher memory footprint compared to plain systemd ([[memory footprint]])
    - PM2’s abstraction can obscure [[raw systemd logs]] ([[abstraction]])
    - Requires familiarity with the [[PM2]] ecosystem for upgrades and tuning

---

**Ansible-driven deployment**
- **Pros**
    - Fully automated, [[idempotent provisioning]] of OS, packages, users and service units
    - [[Declarative playbooks]], version-controlled, ensure consistency across many devices
    - Can integrate build, deployment and configuration in one [[CI - CD pipeline]]
    - Easily extendable to manage [[firewall rules management]], [[certificates management]], [[monitoring agents]]
- **Cons**
    - Not a [[runtime process manager]]—you still need systemd (or PM2) underneath
    - Requires maintaining [[Ansible control node]] or using [[ansible-pull]] on the target
    - Overhead: learning curve and extra tooling for small fleets or single-device setups
    - If using pull-based approach, [[boot-time network dependencies]] can delay startup