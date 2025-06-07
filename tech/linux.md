# Linux & Bash Quick Reference

## Basic Commands

| Task                        | Bash Command                | DOS Command         |
|-----------------------------|-----------------------------|---------------------|
| Change Directory            | `cd`                        | `cd`, `chdir`       |
| List Directory Contents     | `ls`                        | `dir`               |
| Move/Rename File            | `mv`                        | `move`, `rename`    |
| Copy File                   | `cp`                        | `copy`              |
| Delete File                 | `rm`                        | `del`, `erase`      |
| Create Directory            | `mkdir`                     | `mkdir`             |
| Text Editor                 | `vi`, `nano`                | `edit`              |

## File & Directory Operations

- `ls` - list files/folders
- `mkdir` - create directory
- `rmdir` - remove directory
- `cp` - copy files/folders
- `rm` - remove files
- `chmod` - change permissions
- `cat` - view file contents
- `head`/`tail` - first/last 10 lines of file
- `grep` - search text in file
- `sed` - replace text

## Package Management (APT)

- Update package info: `sudo apt update`
- Upgrade installed packages: `sudo apt upgrade`
- Install package: `sudo apt install <package>`
- Remove package: `sudo apt remove <package>`
- Search packages: `sudo apt search <word>`
- Full upgrade: `sudo apt-get dist-upgrade`
- Clean up: `sudo apt-get autoremove -y && sudo apt-get autoclean -y`

## System Info

- Memory: `free -h`
- CPU: `cat /proc/cpuinfo`
- Disk: `df -h`
- Folder size: `sudo du / -hdl`
- Network: `ifconfig -a`
- Uptime: `uptime`
- Manual pages: `man <command>`

## Permissions

- Change permissions: `chmod 777 <path> -R`
- Superuser: `sudo su -`
- Make file executable: `chmod +x <filename>`

## Services

- List processes: `top`
- Start/stop service: `systemctl start|stop <service>`
- Restart service: `systemctl restart <service>`
- Legacy: `service <service> start|restart`

## Updates & Maintenance

```bash
sudo -s -- <<EOF
apt-get update
apt-get upgrade -y
apt-get dist-upgrade -y
apt-get autoremove -y
apt-get autoclean -y
EOF
```

## Storage Management

- Disk usage: `df -h`
- Find large files: `sudo find ./ -type f -size +50M`
- List largest folders: `sudo du -sh * | sort -hr | head -n10`
- Clean apt cache: `sudo apt-get clean`
- Journal logs: `journalctl --disk-usage`
- Empty trash: `trash-empty` (install with `sudo apt install trash-cli`)

## Git

- List config: `git config -l`
- Set line endings: `git config --global core.autocrlf input`

## SSH

- Connect: `ssh user@host`
- SSH config: `~/.ssh/config` (chmod 600)
- Example:
	```
	Host dev
	  HostName dev.example.com
	  User john
	  Port 2322
	```

## Troubleshooting

- Permission issues: `sudo chmod 777 <path> -R`
- Patch management: `sudo dpkg-reconfigure --priority=low unattended-upgrades`
- Remove unattended upgrades: `sudo apt remove unattended-upgrades`
- Truncate Docker logs: `truncate -s 0 /var/lib/docker/containers/*/*-json.log`

## VI Shortcuts

- `:q!` - quit without saving
- `:w` - save changes
- `Ctrl-A` - start of line
- `Ctrl-E` - end of line
- `Ctrl-U` - delete to start of line
- `Ctrl-K` - delete to end of line

---

**Tip:** For WSL, set VS Code terminal to default to WSL and install Ubuntu.

