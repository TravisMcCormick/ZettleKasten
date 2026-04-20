# transmission-remote on CachyOS

CachyOS is Arch-based, so the Arch Wiki is authoritative. This guide covers everything needed to get `transmission-remote` operational.

---

## 1. Installation

```bash
sudo pacman -S transmission-cli
```

This provides both `transmission-daemon` and `transmission-remote`.

---

## 2. Starting the Daemon

Start the daemon once, or enable it to autostart on boot:

```bash
# One-time start
transmission-daemon

# Autostart on boot
sudo systemctl enable --now transmission.service
```

> **Important:** Edit configuration files *before* starting the daemon — changes will not persist if the daemon is already running. Config lives at `~/.config/transmission-daemon/settings.json`.

---

## 3. Authentication

If a username and password are set, all `transmission-remote` commands must include `--auth`:

```bash
transmission-remote --auth username:password -l
```

---

## 4. Core Commands

By default, `transmission-remote` connects to `localhost:9091`. Remote sessions are controlled by specifying a different host and/or port.

### List all torrents

```bash
transmission-remote -l
```

### Add a torrent (file or magnet link)

```bash
transmission-remote -a /path/to/file.torrent
transmission-remote -a "magnet:?xt=urn:btih:..."
```

### Add with a specific download directory

```bash
transmission-remote -a file.torrent -w /mnt/downloads
```

### Get info on a torrent

```bash
transmission-remote -t1 -i
```

### List files in a torrent

```bash
transmission-remote -t1 -f
```

### Download only specific files (e.g., files 2 and 4)

```bash
transmission-remote -t1 -Gall -g2,4
```

### Start / Stop / Remove a torrent

```bash
transmission-remote -t1 --start
transmission-remote -t1 --stop
transmission-remote -t1 --remove
```

### Operate on all torrents

```bash
transmission-remote -tall --start
transmission-remote -tall --stop
```

---

## 5. Speed Limits

```bash
# Set download to 400 KB/s, upload to 60 KB/s
transmission-remote -d400 -u60

# Remove limits
transmission-remote -D -U
```

---

## 6. Remote Session

To control a remote machine:

```bash
transmission-remote host:9091 --auth username:password -l
```

---

## 7. Quality-of-Life Aliases

Typing `transmission-remote` repeatedly is tedious. Add these to `~/.bashrc` or `~/.zshrc`:

```bash
alias tr='transmission-remote'
alias tra='transmission-remote -a'
alias trl='transmission-remote -l'
```

---

## 8. Flag Reference

| Flag | Action |
|---|---|
| `-l` | List all torrents |
| `-a <file/URL>` | Add torrent |
| `-t <id>` | Target torrent by ID |
| `-tall` | Target all torrents |
| `-i` | Detailed info on torrent |
| `-f` | List files in torrent |
| `-s` / `-S` | Start / Stop |
| `-r` | Remove torrent |
| `-R` | Remove torrent + delete data |
| `-d` / `-u` | Down/Up speed limit (KB/s) |
| `-D` / `-U` | Remove Down/Up speed limit |
| `-w <dir>` | Set download directory |
| `--auth user:pass` | Authenticate |

For the full flag reference:

```bash
transmission-remote --help
```
---

### **Related Notes**

- [[Linux Command Line Basics]]

