
---
## Global Options
- `-V`, `--version`  
    Output the PM2 version number.
- `-s`, `--silent`  
    Suppress all messages.
- `--ext <extensions>`  
    Only watch files with these extensions.
- `-n`, `--name <name>`  
    Assign a custom name to the process.
- `-m`, `--mini-list`  
    Show a compact process list without formatting.
- `--interpreter <interpreter>`  
    Specify the interpreter (default: `node`).
- `--interpreter-args <args>`  
    Arguments to pass to the interpreter (alias: `--node-args`).
- `--node-args <args>`  
    Space-delimited arguments for Node.js.
- `--env <environment>`  
    Inject environment variables from the named ecosystem section.
- `-a`, `--update-env`  
    Reload environment variables on restart/reload.
- `-f`, `--force`  
    Force an action.
- `--no-color`  
    Disable colored output.
- `-h`, `--help`  
    Show usage information.

---
## Logging Options
- `-o`, `--output <path>`  
    Stdout log file.
- `-e`, `--error <path>`  
    Stderr log file.
- `-l`, `--log [path]`  
    Combined stdout & stderr log file.
- `--log-type <raw|json>`  
    Log format (default: `raw`).
- `--log-date-format <format>`  
    Prefix logs with a custom timestamp.
- `--time`  
    Enable time-stamped logging.
- `--disable-logs`  
    Turn off log storage.
- `--merge-logs`  
    Merge logs from all instances (errors & output remain separate).

---
## Watch & Auto-Restart
- `--watch [paths]`  
    Watch files/folders for changes.
- `--ignore-watch <patterns>`  
    Comma-separated list of paths or regexes to ignore.
- `--watch-delay <ms|s>`  
    Debounce restart delay after file changes.
- `--cron <pattern>`  
    Restart processes on a cron schedule
- `--restart-delay <ms>`  
    Delay between restarts.
- `--max-restarts [count]`  
    Maximum automatic restarts.
- `--max-memory-restart <bytes>`  
    Restart if memory exceeds this threshold.

---
## Cluster & Scaling
- `-i`, `--instances <number>`  
    Number of instances to launch (cluster mode).
- `--parallel <number>`  
    Number of parallel actions for restarts/reloads.

---
## Startup & Daemon
- `pm2 startup <platform>`  
    Generate startup script (e.g. `launchd`, `systemd`).
- `-u`, `--user <username>`  
    User for startup script.
- `--hp <home path>`  
    Home path for startup script.
- `--service-name <name>`  
    Custom service name.
- `--no-daemon`  
    Run PM2 in the foreground.
- `--shutdown-with-message`  
    Use `process.send('shutdown')` instead of `SIGINT`.

---
## Process Management
- `start [options] <app|json|id|name|namespace>`  
    Start and daemonize an app.
- `stop [options] <app|id|name|namespace|all>`  
    Stop a process.
- `restart [options] <app|id|name|namespace|all>`  
    Restart a process.
- `reload <app|id|name|namespace|all>`  
    Graceful reload (HTTP/HTTPS apps).
- `delete <app|id|name|namespace|all>`  
    Stop and remove a process.
- `scale <app> <number>`  
    Scale cluster instances up/down.
- `trigger <id|name|namespace|all> <action> [params]`  
    Trigger a custom action on a process.
- `sendSignal <signal> <app|id|name>`  
    Send a system signal.
- `ping`  
    Ping the PM2 daemon (starts it if not running).
- `dump|save`  
    Save the process list for resurrection.
- `resurrect`  
    Restore the last dump.
- `list`, `ls`, `ps`, `status`  
    Show all processes.
- `logs [options] [app|id|name|namespace]`  
    Tail logs.
- `flush`  
    Clear all logs.
- `kill`  
    Stop the PM2 daemon.

---
## Modules & Ecosystem
- `install|module:install <module|git:/>`  
    Install or update a PM2 module.
- `uninstall|module:uninstall <module>`  
    Remove a module.
- `ecosystem|init [mode]`  
    Generate an ecosystem config file.
- `deploy <environment>`  
    Deploy using the ecosystem file.

---
## Monitoring & Profiling
- `monit`  
    Launch the PM2 terminal monitor.
- `monitor [app|id|name|namespace]`  
    Monitor a specific process.
- `profile:cpu [time]`  
    Profile CPU usage.
- `profile:mem [time]`  
    Profile memory usage.
- `open`  
    Open the PM2 web dashboard.

---
## Advanced Options
- `--cwd <path>`  
    Run the script from this working directory.
- `--namespace <ns>`  
    Start within the specified namespace.
- `--uid <uid>`, `--gid <gid>`  
    Run with these user/group IDs.
- `--source-map-support` / `--disable-source-map-support`  
    Enable or disable source-map support.
- `--wait-ready`  
    Wait for the app’s “ready” event before marking as online.
- `--attach`  
    Attach logs after start/restart/stop/reload.
- `--trace` / `--disable-trace`  
    Enable or disable transaction tracing.
- `--deep-monitoring`  
    Enable all monitoring tools (equivalent to `--v8 --event-loop-inspector --trace`).
- `--sort <field:order>`  
    Sort `pm2 ls` output by a given field and order.
- `--no-autostart` / `--no-autorestart` / `--no-vizion` / `--no-pmx` / `--no-automation` / `--no-treekill`  
    Disable various PM2 features on start.