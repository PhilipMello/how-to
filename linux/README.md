# Linux Commands Cheatsheet

## 🖥️ Basic Commands

### 📁 `ls` - List directory contents
List the files and directories in the current directory.

```bash
ls
```
### Example:
```bash
$ ls
Desktop  Documents  Downloads  Music  Pictures  Videos
```
---
## 📂 cd - Change directory
Change the current working directory.
```bash
cd <directory_path>
```
### Example:
```bash
$ cd /home/user/Downloads
```
---
## ⚙️ File Operations
📝 touch - Create a new empty file
Create an empty file.
```bash
touch <filename>
```
### Example:
```bash
$ touch newfile.txt
```
---
## 🛠️ System Management
🔍 top - Task manager
Display running processes.
```bash
top
```
### Example:
```bash
$ top
```
---
## 💾 df - Disk space usage
Show disk space usage of mounted filesystems.
```bash
df -h
```
### Example:
```bash
$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1       100G  30G  65G  32% /
```
---
## 🔒 Permissions and Ownership
🔐 chmod - Change file permissions
Change the permissions of a file or directory.
```bash
chmod <permissions> <filename>
```
### Example:
```bash
$ chmod 755 script.sh
```
---
## 👥 chown - Change file ownership
Change the ownership of a file or directory.
```bash
chown <user>:<group> <filename>
```
### Example:
```bash
$ chown user:admin myfile.txt
```
---
## 🌐 Networking
🌐 ping - Send ICMP echo requests
Test network connectivity to a host.
```bash
ping <hostname>
```
### Example:
```bash
$ ping google.com
```
---
## 🌍 ifconfig - Display network interface configuration
Show network interface configuration.
```bash
ifconfig
```
### Example:
```bash
$ ifconfig
```
---
## 📦 Package Management
🔽 apt-get - Install packages (Debian-based systems)
Install a package using apt-get.
```bash
sudo apt-get install <package_name>
```
### Example:
```bash
$ sudo apt-get install curl
```
## 🛠️ yum - Install packages (Red Hat-based systems)
Install a package using yum.
```bash
sudo yum install <package_name>
```
### Example:
```bash
$ sudo yum install wget
```
---
## 🗃️ File Searching
🔍 find - Search for files in a directory hierarchy
Search for files matching a pattern.
```bash
find <directory> -name <filename>
```
### Example:
```bash
$ find /home/user/Documents -name "*.txt"
```
---
🚀 Process Management
🔄 ps - Report process status
Show information about running processes.
```bash
ps aux
```
### Example:
```bash
$ ps aux
```
---
## 🛑 kill - Terminate processes
Terminate a process by its PID.
```bash
kill <PID>
```
### Example:
```bash
$ kill 12345
```
---
## 📋 Clipboard
📑 xclip - Copy to clipboard
Copy text to the clipboard.
```bash
echo "<text>" | xclip -selection clipboard
```
### Example:
```bash
$ echo "Hello World" | xclip -selection clipboard
```
---
## 🔄 Compression
📦 tar - Archive files
Create a tarball archive.
```bash
tar -cvf <archive_name.tar> <files_or_directories>
```
### Example:
```bash
$ tar -cvf backup.tar Documents/
```
🗜️ gzip - Compress files
Compress a file using gzip.
```bash
gzip <filename>
```
### Example:
```bash
$ gzip myfile.txt
```
---
⏳ System Information
⏱️ uptime - System uptime
Display the system uptime.
```bash
uptime
```
### Example:
```bash
$ uptime
 17:24:09 up 10 days,  3:56,  3 users,  load average: 0.08, 0.10, 0.09
```
---
## 🖧 netstat - Network statistics
Display network connections, routing tables, and interface statistics.
```bash
netstat -tuln
```
### Example:
```bash
$ netstat -tuln
```

