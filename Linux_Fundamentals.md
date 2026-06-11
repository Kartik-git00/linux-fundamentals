## Linux Fundamentals 

## About Linux 

What is Linux? Why Learn Linux? List of Linux Distributions 

Lab 01 ] Linux Navigation Commands Absolute Path vs Relative Path Practical 

Lab 02 ^ File Management Commands Covered Practical 

Lab 03 ^ Users & Groups Commands Covered Practical 

Lab 04 ^ File Permissions Commands Covered Practical 

Lab 05 ^ Networking Basics Commands Covered Practical 

Lab 06 ] Processes & Services Commands Covered Practical 

Lab 07 ] Package Management Commands Covered 

Lab 08 ] Log Analysis 

Commands Covered 

Lab 9 ^ SSH LSecure Shell) 

Commands Covered 

Lab 10 ^ Bash Scripting Basics 

Commands & Concepts Covered 

Help commands 

Note: Some Command need sudo if permission denied. 

Linux Fundamentals 

1 

## About Linux 

## What is Linux? 

## Linux is a free, open-source operating system LOS) based on Unix. 

What makes Linux uniquely powerful and distinct from proprietary systems like Microsoft Windows or macOS include the following traits: 

## - Fully Open Source 

- Multi Platform 

## Highly Customizable & Lightweight 

- Secure and stable 

- 

- Community Driven 

- 

- Kernel Based 

## Why Learn Linux? 

Industry Standard 

- Career Opportunity 

- Security and Stability 

- Customizable 

- Efficient 

## List of Linux Distributions 

- Debian Based 

Ubuntu 

- Kali Linux ( for pentesting ) 

- Linux Mint ( Ubuntu based ) 

Parrot OS 

Kali Purple ( for both Blue & Red ) 

Red Hat Enterprise Linux 

- Fedora Linux 

Linux Fundamentals 

2 

Rocky Linux Alma Linux CentOS 

Arch Linux Manjaro 

openSUSE SUSE Linux Enterprise 

Gentoo 

Slackware 

## Lab 01 - Linux Navigation 

## Commands 

**==> picture [468 x 297] intentionally omitted <==**

**----- Start of picture text -----**<br>
Command Definition Example<br>Prints the current working<br>pwd pwd<br>directory.<br>ls Lists files and directories. ls<br>Lists files in long format with<br>ls -l ls -l<br>permissions and ownership.<br>Shows hidden files and<br>ls -a ls -a<br>directories.<br>cd Changes the current directory. cd Documents<br>cd .. Moves one directory up. cd ..<br>Moves to the user's home<br>cd ~ cd ~<br>directory.<br>cd / Moves to the root directory. cd /<br>Displays the directory structure<br>tree tree<br>as a tree.<br>**----- End of picture text -----**<br>


Linux Fundamentals 

3 

|Command|Definition|Example|
|---|---|---|
|`clear`|Clears the terminal screen.|`clear`|
|`history`|Shows previously executed<br>commands.|`history`|



## Absolute Path vs Relative Path 

|cd/home/Documents|Absolute Path|
|---|---|
|cd Documents|Relative Path|



## Practical 

```
pwd
ls
cd ~
pwd
cd /
pwd
cd ~
ls-a
history
clear
```

## Lab 02 – File Management 

This is where you learn how to create, copy, move, view, and delete files. 

## Commands Covered 

|Command|Definition|Example|
|---|---|---|
|`touch`|Creates an empty file.|`touch notes.txt`|



Linux Fundamentals 

4 

**==> picture [468 x 358] intentionally omitted <==**

**----- Start of picture text -----**<br>
Command Definition Example<br>mkdir Creates a directory. mkdir projects<br>Removes an empty<br>rmdir rmdir projects<br>directory.<br>cp Copies files or directories. cp notes.txt backup.txt<br>mv notes.txt<br>mv Moves or renames files.<br>linux_notes.txt<br>rm Removes files. rm notes.txt<br>Removes directories<br>rm -r rm -r testfolder<br>recursively.<br>cat Displays file contents. cat notes.txt<br>Views file contents page by<br>less less notes.txt<br>page.<br>head Shows first 10 lines of a file. head notes.txt<br>tail Shows last 10 lines of a file. tail notes.txt<br>Outputs text or writes to<br>echo echo "Hello" > notes.txt<br>files.<br>file Identifies file type. file notes.txt<br>**----- End of picture text -----**<br>


## Practical 

```
mkdir linux-lab
cd linux-lab
touch notes.txt
echo"Linux Fundamentals"> notes.txt
cat notes.txt
cp notes.txt backup.txt
mv backup.txt notes_backup.txt
ls
head notes.txt
tail notes.txt
file notes.txt
rm notes_backup.txt
```

Linux Fundamentals 

5 

```
cd..
rm-r linux-lab
```

## Lab 03 – Users & Groups 

permissions and access control are built around users and groups. 

## Commands Covered 

**==> picture [468 x 353] intentionally omitted <==**

**----- Start of picture text -----**<br>
Command Definition Example<br>Shows the current logged-in<br>whoami whoami<br>user.<br>Shows user ID LUID) and group<br>id id<br>ID LGIDM.<br>Displays groups a user belongs<br>groups groups<br>to.<br>Runs a command with elevated<br>sudo sudo apt update<br>privileges.<br>useradd Creates a new user. sudo useradd user<br>Sets or changes a user's<br>passwd sudo passwd user<br>password.<br>sudo usermod -aG sudo<br>usermod Modifies a user account.<br>user<br>groupadd Creates a new group. sudo groupadd developers<br>groupdel Deletes a group. sudo groupdel developers<br>userdel Deletes a user. sudo userdel user<br>su Switches to another user. su user<br>**----- End of picture text -----**<br>


## Practical 

```
whoami
id
```

Linux Fundamentals 

6 

```
groups
sudogroupadd cyber
sudouseradd k-lab
sudousermod-aG cyber k-lab
id k-lab
su k-lab
whoami
```

## Lab 04 – File Permissions 

Many privilege escalation vulnerabilities happen because of misconfigured permissions. 

## Commands Covered 

|Command|Definition|Example|
|---|---|---|
|`ls -l`|View file permissions.|`ls -l file.txt`|
|`chmod`|Change file permissions.|`chmod 755 script.sh`|
|`chown`|Change file owner.|`sudo chown user file.txt`|
|`chgrp`|Change file group.|`sudo chgrp developers`<br>`file.txt`|
|`umask`|View/set default<br>permissions.|`umask`|



## -rw-r--r-- 

│ │ │ │ 

│ │ │ └── Others 

│ │ └──── Group 

│ └─────── Owner 

└───────── File Type 

Linux Fundamentals 

7 

|Number|Permission|
|---|---|
|777|rwxrwxrwx|
|755|rwxr-xr-x|
|700|rwx------|
|644|rw-r--r--|
|600|rw-------|



## Practical 

```
mkdir permission-lab
cd permission-lab
touch file1.txt
touch file2.txt
ls-l
chmod644 file1.txt
chmod777 file2.txt
ls-l
touch script.sh
chmod +x script.sh
ls-l
sudochown root file1.txt
ls-l
sudochgrp cyber file1.txt
ls-l
umask
```

## Lab 05 – Networking Basics 

## Commands Covered 

Linux Fundamentals 

8 

**==> picture [468 x 382] intentionally omitted <==**

**----- Start of picture text -----**<br>
Command Definition Example<br>Displays network<br>ip a interfaces and IP ip a<br>addresses.<br>ip route Shows routing table. ip route<br>Displays system<br>hostname hostname<br>hostname.<br>Tests connectivity to a<br>ping ping google.com<br>host.<br>Shows network<br>ss connections and listening ss -tuln<br>ports.<br>Displays network statistics<br>netstat netstat -tuln<br>and ports.<br>nslookup Queries DNS records. nslookup google.com<br>Advanced DNS lookup<br>dig dig google.com<br>tool.<br>curl Transfers data from URLs. curl https://google.com<br>Downloads files from the wget<br>wget<br>web. https://google.com/file.txt<br>**----- End of picture text -----**<br>


## Practical 

```
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

t = TCP 

Linux Fundamentals 

9 

u = UDP 

l = Listening 

n = Numeric 

## Lab 06 - Processes & Services 

This lab teaches you how Linux runs programs and manages services. In cybersecurity, you'll often need to find, monitor, or stop processes. 

## Commands Covered 

**==> picture [468 x 300] intentionally omitted <==**

**----- Start of picture text -----**<br>
Command Definition Example<br>ps Displays running processes. ps<br>ps aux Shows all running processes. ps aux<br>top Real-time process monitor. top<br>Improved interactive process<br>htop htop<br>viewer.<br>pgrep Find process IDs by name. pgrep firefox<br>kill Terminates a process. kill 1234<br>kill -9 Forcefully kills a process. kill -9 1234<br>jobs Lists background jobs. jobs<br>bg Sends a job to background. bg %1<br>fg Brings a job to foreground. fg %1<br>systemctl Manages system services. systemctl status ssh<br>service Legacy service management. service ssh status<br>**----- End of picture text -----**<br>


## Practical 

```
ps
ps aux
top(q forexit)
```

Linux Fundamentals 

10 

```
htop(F10 forexit)
sleep300
kill1234
ps aux |grepsleep
sleep300&
jobs
fg&
systemctl status ssh
```

## Lab 07 - Package Management 

Package management is how Linux installs, updates, and removes software. 

## Commands Covered 

**==> picture [468 x 251] intentionally omitted <==**

**----- Start of picture text -----**<br>
Command Definition Example<br>apt update Updates package information. sudo apt update<br>apt upgrade Upgrades installed packages. sudo apt upgrade<br>apt install Installs a package. sudo apt install tree<br>apt remove Removes a package. sudo apt remove tree<br>Removes package and<br>apt purge sudo apt purge tree<br>configuration files.<br>Removes unused<br>apt autoremove sudo apt autoremove<br>dependencies.<br>apt search Searches for packages. apt search nmap<br>apt show Displays package information. apt show nmap<br>dpkg -l Lists installed packages. dpkg -l<br>**----- End of picture text -----**<br>


## Lab 08 - Log Analysis 

Linux Fundamentals 

11 

Logs are one of the most important sources of information for troubleshooting, incident response, and security investigations. 

## Commands Covered 

**==> picture [468 x 244] intentionally omitted <==**

**----- Start of picture text -----**<br>
Command Definition Example<br>View system logs managed by<br>journalctl journalctl<br>systemd.<br>View recent system events<br>journalctl -xe journalctl -xe<br>and errors.<br>dmesg View kernel messages. dmesg<br>tail View the end of a file. tail auth.log<br>tail -f Follow log updates in real time. tail -f auth.log<br>grep Search for text patterns. grep ssh auth.log<br>Read large log files page by<br>less less auth.log<br>page.<br>cat Display entire file contents. cat auth.log<br>**----- End of picture text -----**<br>


|File|Purpose|
|---|---|
|`/var/log/syslog`|General system logs|
|`/var/log/auth.log`|Authentication logs|
|`/var/log/kern.log`|Kernel logs|
|`/var/log/dpkg.log`|Package installation logs|
|`/var/log/boot.log`|Boot logs|



## Lab 9 – SSH (Secure Shell) 

SSH allows you to securely access another Linux machine remotely. 

## Commands Covered 

Linux Fundamentals 

12 

|Command|Definition|Example|
|---|---|---|
|`ssh`|Connect to a remote<br>machine.|`ssh user@192.168.1.10`|
|`ssh-keygen`|Generate SSH key pair.|`ssh-keygen`|
|`ssh-copy-id`|Copy public key to remote<br>machine.|`ssh-copy-id`<br>`user@192.168.1.10`|
|`scp`|Securely copy files.|`scp file.txt`<br>`user@host:/home/user/`|
|`sftp`|Secure file transfer session.|`sftp user@host`|



## Lab 10 – Bash Scripting Basics 

## Commands & Concepts Covered 

|Concept|Definition|Example|
|---|---|---|
|Variable|Store data in memory|`name="Kartik"`|
|echo|Display output|`echo $name`|
|read|Take user input|`read name`|
|if|Conditional statement|`if [ $a -eq $b ]`|
|for|Loop through items|`for i in {1..5}`|
|while|Run while condition is true|`while [ $x -lt 5 ]`|
|function|Reusable block of code|`greet(){}`|
|chmod+x|Make script executable|`chmod +x script.sh`|
|./|Execute script|`./script.sh`|



```
nano hello.sh
```

```
#!/bin/bash
```

```
echo"Hello, World!"
```

Linux Fundamentals 

13 

```
chmod +x hello.sh
./hello.sh
```

```
#!/bin/bash
name="User"
echo"Hello $name"
```

```
#!/bin/bash
```

```
echo"Enter your name:"
read name
echo"Welcome $name"
```

```
#!/bin/bash
num=10
if[$num-eq10]
then
echo"Number is 10"
fi
```

```
#!/bin/bash
foriin{1..5}
do
echo$i
done
```

Linux Fundamentals 

14 

```
#!/bin/bash
count=1
while[$count-le5]
do
echo$count
count=$((count+1))
done
```

```
#!/bin/bash
greet(){
echo"Welcome to Linux"
}
greet
Project:
nano system-info.sh
```

```
#!/bin/bash
echo"===== SYSTEM INFO ====="
echo"Hostname:"
hostname
echo""
echo"Current User:"
whoami
```

Linux Fundamentals 

15 

```
echo""
echo"IP Address:"
hostname-I
chmod +x system-info.sh
./system-info.sh
```

## **`#!/bin/bash`** 

```
echo"Current User: $(whoami)"
echo"Home Directory: $HOME"
echo"Current Directory: $(pwd)"
echo"Date: $(date)"
```

## Help commands 

<tool> —help 

<tool> -h 

- apropos <tool> 

## Note: Some Command need sudo if permission denied. 

Linux Fundamentals 

16 

