# CheatSheet_Linux

# Help & Documentation

| Command | Description | Example |
| --- | --- | --- |
| `man <tool>` | Opens the manual page for a command. | `man ls` |
| `<tool> -h` | Displays a quick help menu. | `grep -h` |
| `<tool> --help` | Shows detailed help information. | `find --help` |
| `apropos <keyword>` | Searches manual pages for related commands. | `apropos network` |
| `which <tool>` | Displays the location of a command. | `which python3` |
| `whereis <tool>` | Finds binary, source, and man page files. | `whereis ssh` |

# System Information

| Command | Description | Example |
| --- | --- | --- |
| `whoami` | Shows the current user. | `whoami` |
| `id` | Displays user and group IDs. | `id` |
| `hostname` | Shows the system hostname. | `hostname` |
| `uname -a` | Displays kernel and OS information. | `uname -a` |
| `pwd` | Shows the current directory path. | `pwd` |
| `date` | Displays the current date and time. | `date` |
| `uptime` | Shows how long the system has been running. | `uptime` |
| `who` | Lists logged-in users. | `who` |
| `w` | Displays logged-in users and their activity. | `w` |
| `env` | Shows environment variables. | `env` |

# File & Directory Management

| Command | Description | Example |
| --- | --- | --- |
| `ls` | Lists files and directories. | `ls -la` |
| `cd` | Changes directory. | `cd Documents` |
| `mkdir` | Creates a directory. | `mkdir projects` |
| `rmdir` | Removes an empty directory. | `rmdir test` |
| `touch` | Creates an empty file. | `touch notes.txt` |
| `cp` | Copies files and directories. | `cp file.txt backup.txt` |
| `mv` | Moves or renames files. | `mv old.txt new.txt` |
| `rm` | Removes files or directories. | `rm file.txt` |
| `tree` | Displays directory structure. | `tree` |
| `stat` | Shows detailed file information. | `stat file.txt` |

# File Viewing & Text Processing

| Command | Description | Example |
| --- | --- | --- |
| `cat` | Displays file contents. | `cat notes.txt` |
| `more` | Views files page by page. | `more file.txt` |
| `less` | Advanced file viewer. | `less file.txt` |
| `head` | Displays first lines of a file. | `head file.txt` |
| `tail` | Displays last lines of a file. | `tail -f logs.txt` |
| `sort` | Sorts text lines. | `sort names.txt` |
| `grep` | Searches for text patterns. | `grep "root" /etc/passwd` |
| `cut` | Extracts columns from text. | `cut -d ":" -f1 file.txt` |
| `tr` | Replaces characters. | `echo hello | tr a-z A-Z` |
| `column` | Formats text into columns. | `column -t data.txt` |
| `awk` | Powerful text-processing utility. | `awk '{print $1}' file.txt` |
| `sed` | Stream editor for modifying text. | `sed 's/linux/Linux/g' file.txt` |
| `wc` | Counts lines, words, and characters. | `wc file.txt` |

# Searching Files

| Command | Description | Example |
| --- | --- | --- |
| `find` | Searches for files and directories. | `find . -name "*.txt"` |
| `locate` | Quickly finds files using a database. | `locate passwd` |
| `updatedb` | Updates the locate database. | `sudo updatedb` |
| `whereis` | Finds command-related files. | `whereis python` |

# User & Group Management

| Command | Description | Example |
| --- | --- | --- |
| `sudo` | Executes commands with elevated privileges. | `sudo apt update` |
| `su` | Switches users. | `su root` |
| `useradd` | Creates a user account. | `sudo useradd john` |
| `userdel` | Deletes a user account. | `sudo userdel john` |
| `usermod` | Modifies a user account. | `sudo usermod -aG sudo john` |
| `passwd` | Changes user passwords. | `passwd` |
| `addgroup` | Creates a group. | `sudo addgroup developers` |
| `delgroup` | Deletes a group. | `sudo delgroup developers` |
| `groups` | Displays user groups. | `groups` |

# Permissions & Ownership

| Command | Description | Example |
| --- | --- | --- |
| `chmod` | Changes file permissions. | `chmod 755 script.sh` |
| `chown` | Changes ownership. | `sudo chown user:user file.txt` |
| `chgrp` | Changes group ownership. | `sudo chgrp developers file.txt` |
| `umask` | Sets default permissions. | `umask 022` |

# Networking

| Command | Description | Example |
| --- | --- | --- |
| `ifconfig` | Displays network interfaces. | `ifconfig` |
| `ip` | Modern network configuration utility. | `ip a` |
| `ping` | Tests connectivity to a host. | `ping google.com` |
| `netstat` | Displays network connections. | `netstat -tuln` |
| `ss` | Displays socket information. | `ss -tuln` |
| `curl` | Transfers data from servers. | `curl https://example.com` |
| `wget` | Downloads files. | `wget https://example.com/file.zip` |
| `dig` | Performs DNS lookups. | `dig google.com` |
| `nslookup` | Queries DNS records. | `nslookup google.com` |
| `traceroute` | Shows packet routes. | `traceroute google.com` |

# Process Management

| Command | Description | Example |
| --- | --- | --- |
| `ps` | Shows running processes. | `ps aux` |
| `top` | Displays real-time process information. | `top` |
| `htop` | Interactive process viewer. | `htop` |
| `kill` | Terminates a process. | `kill 1234` |
| `killall` | Terminates processes by name. | `killall firefox` |
| `jobs` | Lists background jobs. | `jobs` |
| `bg` | Moves a job to the background. | `bg %1` |
| `fg` | Brings a job to the foreground. | `fg %1` |

# Package Management

| Command | Description | Example |
| --- | --- | --- |
| `apt` | Installs and manages packages. | `sudo apt install git` |
| `aptitude` | Alternative package manager. | `sudo aptitude install git` |
| `dpkg` | Manages Debian packages. | `sudo dpkg -i package.deb` |
| `snap` | Manages Snap packages. | `sudo snap install code` |
| `pip` | Python package manager. | `pip install requests` |
| `gem` | Ruby package manager. | `gem install rails` |

# Services & Logs

| Command | Description | Example |
| --- | --- | --- |
| `systemctl` | Manages system services. | `sudo systemctl status ssh` |
| `journalctl` | Views system logs. | `journalctl -xe` |
| `service` | Controls services on some systems. | `sudo service ssh restart` |

# **Disclaimer**

This repository is intended for educational and note-taking purposes. Some commands and concepts were learned from resources such as Hack The Box Academy, Linux manual pages, and official documentation. The content has been reorganized and rewritten in my own format as part of my learning journey.