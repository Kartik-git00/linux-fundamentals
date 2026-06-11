# Linux Fundamentals

## About Linux

### What is Linux?
Linux is a free, open-source operating system (OS) based on Unix.

**Key Features**
- Fully Open-Source
- Multi-Platform
- Highly Customizable & Lightweight
- Secure and Stable
- Community-Driven
- Kernel-Based

### Why Learn Linux?
- Industry Standard
- Career Opportunity
- Security and Stability
- Customizable
- Efficient

### Linux Distributions
#### Debian-Based
- Ubuntu
- Kali Linux (for pentesting)
- Linux Mint
- Parrot OS
- Kali Purple

#### Red Hat Family
- Red Hat Enterprise Linux
- Fedora Linux
- Rocky Linux
- Alma Linux
- CentOS

#### Others
- Arch Linux
- Manjaro
- openSUSE
- SUSE Linux Enterprise
- Gentoo
- Slackware

---

# Lab 01 - Linux Navigation

| Command | Definition | Example |
|----------|------------|---------|
| pwd | Prints current working directory | pwd |
| ls | Lists files and directories | ls |
| ls -l | Long listing format | ls -l |
| ls -a | Show hidden files | ls -a |
| cd | Change directory | cd Documents |
| cd .. | Move one directory up | cd .. |
| cd ~ | Home directory | cd ~ |
| cd / | Root directory | cd / |
| tree | Display directory tree | tree |
| clear | Clear terminal | clear |
| history | Show command history | history |

## Absolute vs Relative Path

```bash
cd /home/Documents   # Absolute Path
cd Documents         # Relative Path
```

## Practical

```bash
pwd
ls
cd ~
pwd
cd /
pwd
cd ~
ls -a
history
clear
```

---

# Lab 02 - File Management

| Command | Definition | Example |
|----------|------------|---------|
| touch | Create file | touch notes.txt |
| mkdir | Create directory | mkdir projects |
| rmdir | Remove empty directory | rmdir projects |
| cp | Copy files | cp notes.txt backup.txt |
| mv | Move/Rename file | mv notes.txt linux_notes.txt |
| rm | Remove file | rm notes.txt |
| rm -r | Remove directory recursively | rm -r testfolder |
| cat | Display file contents | cat notes.txt |
| less | View file page-by-page | less notes.txt |
| head | First 10 lines | head notes.txt |
| tail | Last 10 lines | tail notes.txt |
| echo | Output text | echo "Hello" > notes.txt |
| file | Identify file type | file notes.txt |

## Practical

```bash
mkdir linux-lab
cd linux-lab
touch notes.txt
echo "Linux Fundamentals" > notes.txt
cat notes.txt
cp notes.txt backup.txt
mv backup.txt notes_backup.txt
ls
head notes.txt
tail notes.txt
file notes.txt
rm notes_backup.txt
cd ..
rm -r linux-lab
```

---

# Lab 03 - Users & Groups

| Command | Definition |
|----------|------------|
| whoami | Current user |
| id | UID and GID |
| groups | User groups |
| sudo | Elevated privileges |
| useradd | Create user |
| passwd | Set password |
| usermod | Modify user |
| groupadd | Create group |
| groupdel | Delete group |
| userdel | Delete user |
| su | Switch user |

## Practical

```bash
whoami
id
groups
sudo groupadd cyber
sudo useradd k-lab
sudo usermod -aG cyber k-lab
id k-lab
su k-lab
whoami
```

---

# Lab 04 - File Permissions

| Command | Definition |
|----------|------------|
| ls -l | View permissions |
| chmod | Change permissions |
| chown | Change owner |
| chgrp | Change group |
| umask | Default permissions |

## Common Permissions

| Number | Permission |
|----------|------------|
| 777 | rwxrwxrwx |
| 755 | rwxr-xr-x |
| 700 | rwx------ |
| 644 | rw-r--r-- |
| 600 | rw------- |

## Practical

```bash
mkdir permission-lab
cd permission-lab
touch file1.txt
touch file2.txt
ls -l
chmod 644 file1.txt
chmod 777 file2.txt
ls -l
touch script.sh
chmod +x script.sh
ls -l
sudo chown root file1.txt
sudo chgrp cyber file1.txt
umask
```

---

# Lab 05 - Networking Basics

| Command | Definition |
|----------|------------|
| ip a | Show IP addresses |
| ip route | Routing table |
| hostname | System hostname |
| ping | Connectivity test |
| ss | Network sockets |
| netstat | Network statistics |
| nslookup | DNS lookup |
| dig | Advanced DNS lookup |
| curl | Transfer data |
| wget | Download files |

## Practical

```bash
ip a
ip route
hostname
ping google.com
ss -tuln
nslookup google.com
dig google.com
curl https://google.com
wget https://google.com
```

---

# Lab 06 - Processes & Services

| Command | Definition |
|----------|------------|
| ps | Running processes |
| ps aux | All processes |
| top | Real-time monitor |
| htop | Enhanced monitor |
| pgrep | Find PID |
| kill | Kill process |
| kill -9 | Force kill |
| jobs | Background jobs |
| bg | Send job to background |
| fg | Bring job to foreground |
| systemctl | Service management |
| service | Legacy service management |

---

# Lab 07 - Package Management

```bash
sudo apt update
sudo apt upgrade
sudo apt install tree
sudo apt remove tree
sudo apt purge tree
sudo apt autoremove
apt search nmap
apt show nmap
dpkg -l
```

---

# Lab 08 - Log Analysis

| File | Purpose |
|------|---------|
| /var/log/syslog | General system logs |
| /var/log/auth.log | Authentication logs |
| /var/log/kern.log | Kernel logs |
| /var/log/dpkg.log | Package logs |
| /var/log/boot.log | Boot logs |

---

# Lab 09 - SSH

```bash
ssh user@192.168.1.10
ssh-keygen
ssh-copy-id user@192.168.1.10
scp file.txt user@host:/home/user/
sftp user@host
```

---

# Lab 10 - Bash Scripting Basics

```bash
#!/bin/bash
echo "Hello, World!"
```

```bash
#!/bin/bash
name="User"
echo "Hello $name"
```

```bash
#!/bin/bash
echo "Enter your name:"
read name
echo "Welcome $name"
```

```bash
#!/bin/bash
num=10
if [ $num -eq 10 ]
then
 echo "Number is 10"
fi
```

```bash
#!/bin/bash
for i in {1..5}
do
 echo $i
done
```

```bash
#!/bin/bash
count=1
while [ $count -le 5 ]
do
 echo $count
 count=$((count+1))
done
```

## Project

```bash
#!/bin/bash
echo "===== SYSTEM INFO ====="
hostname
whoami
hostname -I
```
