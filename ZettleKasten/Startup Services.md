**Native systemd service**
- **Pros**
    - Minimal extra dependencies (leverages built-in systemd)
    - Predictable startup ordering, restart/back-off behavior, and structured logging through `journalctl` (covered in [[systemd service features]])
    - Very low overhead and easy to configure
- **Cons**
    - No built-in clustering or load-balancing compared to dedicated supervisors
    - Log rotation is still your responsibility (often paired with [[logrotate]])
    - Fewer built-in health and reload workflows than a supervisor like [[PM2]] unless you compose units and timers yourself

---

**[[PM2]] (with systemd startup)**
- **Pros**
    - Built-in clustering and [[zero-downtime reloads]] for Node services
    - Integrated log rotation and basic inspection without extra daemons
    - Memory limits and process checks are first-class ([[Memory-limit enforcement]], process health checks)
    - Generates its own systemd unit files for boot integration (still summarized in [[systemd service features]])
- **Cons**
    - Adds PM2 + Node.js as runtime dependencies and usually a higher baseline memory footprint than plain systemd
    - The PM2 abstraction can distance you from raw journal-only workflows
    - You still need operational familiarity with PM2 upgrades and tuning

---

**[[Ansible-driven deployment]]**
- **Pros**
    - Idempotent, declarative configuration for OS packages, users, and unit files, usually stored in version control
    - Can fold build, deploy, and hardening into one [[CI - CD pipeline]]
    - Extends naturally to [[firewall rules management]], certificate lifecycle work, and monitoring agent rollout
- **Cons**
    - Ansible is not a [[runtime process manager]]; you still run systemd or PM2 on the host
    - Requires an [[Ansible control node]] (or ansible-pull on the device) and ongoing playbook maintenance
    - Heavier tooling for tiny fleets; pull-based boot paths can introduce [[boot-time network dependencies]]
