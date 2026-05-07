# 🐧 Linux Fundamentals – Structured Course Notes
---
## 👨‍💻 About the Instructor
- Final-year Engineering Student (Class of 2026)
- Background in **Computer Architecture & Embedded Systems**
- 3+ years experience in **C & Assembly Programming**
- Strong foundation in **Linux, Networking, and Cybersecurity**
- Completed Cisco Certified Network Associate (CCNA)
- Studied **CEH (Certified Ethical Hacker)** concepts
- Preparing for **OSCP (Offensive Security Certified Professional)**
- Ranked in the **Top 15% on TryHackMe**
- Hands-on experience with:
    - Network Design & Simulation (Packet Tracer)
    - Linux Systems & Command Line
- Participated in national EV competition (Top 5 in Egypt 🏆)
---
## 🎯 What I Focus On

- Simplifying complex technical concepts
- Practical, hands-on learning
- Real-world cybersecurity mindset
---
## **Steps to Install Linux (Ubuntu/Kali) on Windows 11 via WSL**
#### **1. Enable WSL and Virtual Machine Platform**
- Open the **Start Menu**, search for **PowerShell**, right-click it, and select **Run as Administrator**.
- Type the following command and press Enter:
```shell
wsl --install
```
- **Note:** If WSL is already installed, this command will show the help menu. If it's your first time, it will install the necessary components. **Restart your computer** if prompted.
#### **2. Choose and Install your Distribution**
You can install your preferred Linux distribution using the Terminal or the Microsoft Store.
**Option A: Via Terminal (Fastest)**
- List available distributions:
```shell
wsl --list --online
```
- To install **Ubuntu**:
```shell
wsl --install -d Ubuntu
```
- To install **Kali Linux**:
```shell
wsl --install -d kali-linux
```
---
## 📌 1. Introduction to Linux & Terminal
### What is Linux?
- Linux is an **Operating System** used to manage hardware and software resources.
### Terminal Basics
- The terminal allows you to interact with the system using commands.
---
## 📁 2. Navigation & File System Basics
### Key Concepts
- Linux uses a **hierarchical file system** starting from root `/`
### Paths
- **Absolute Path:**
    - Full path from root
    - Example: `/home/user/file.txt`
- **Relative Path:**
    - Based on current directory
    - Example: `documents/file.txt`
### Special Symbols
- `.` → Current directory
- `..` → Parent directory
---
## 📂 3. Basic Navigation Commands
- `pwd` → Show current directory
- `ls` → List files and directories
    - `ls -a` → Show hidden files
    - `ls -l` → Detailed view
- `cd <directory>` → Change directory
    - `cd ..` → Go back one level
    - `cd ../../` → Go back two levels
---
## 📄 4. File & Directory Management
### Create
- `touch <file>` → Create file
- `mkdir <folder>` → Create directory
### Delete
- `rm <file>` → Delete file
- `rm -r <folder>` → Delete folder recursively
- `rm -rf <folder>` → Force delete (⚠️ dangerous)
- `rmdir <folder>` → Delete empty folder
### Copy & Move
- `cp <src> <dest>` → Copy file
- `cp -r <folder>` → Copy directory
- `mv <src> <dest>` → Move or rename
---
## 📝 5. Viewing & Editing Files
- `cat <file>` → Show file content
- `nano <file>` → Edit file
### Useful Commands
- `head -n <num>` → First lines
- `tail -n <num>` → Last lines
- `wc <file>` → Count lines/words
- `sort <file>` → Sort content
- `uniq -u` → Unique lines
---
## 🔍 6. Searching in Linux
### grep (Search inside files)
- `grep "text" file`
- `grep -i` → Ignore case
- `grep -r` → Recursive
- `grep -n` → Show line numbers
### find (Advanced search)
- `find . -name "*.txt"`
- `find -type f` → Files
- `find -type d` → Directories
### locate (Fast search)
- `locate <file>`
- `updatedb` → Update database
---
## 🔗 7. Piping & Command Chaining
### Pipe
- `|` → Output → Input
    - Example:  
        `cat file.txt | grep "hello"`
### Conditional Execution
- `&&` → Run next if success
- `||` → Run if fail
### Background Execution
- `&` → Run in background
---
## 📤 8. Redirection & File Descriptors
### Output Redirection
- `>` → Overwrite
- `>>` → Append
### Example
- `echo hello > file.txt`
### File Descriptors
- STDIN → 0
- STDOUT → 1
- STDERR → 2
---
## 🔐 9. Users & Privileges
### What is root?
- Superuser with full permissions
### Commands
- `sudo <command>` → Run as root
- `sudo su` → Switch to root
- `su <user>` → Switch user
- `exit` → Exit session
---
## 🔑 10. File Permissions
### Types
- `-` → File
- `d` → Directory
### Format
``` shell
rwx rwx rwx  
Owner | Group | Others
```
- r = 4
- w = 2
- x = 1
### chmod
- `chmod u+x file`
- `chmod g-w file`
- `chmod o+r file`
- `chmod a+rwx file`
---
## 📦 11. Package Management (APT)
### Update & Upgrade
- `sudo apt update`
- `sudo apt full-upgrade`
- `sudo apt -y full-upgrade`
### Install
- `sudo apt install <package>`
---
## 🌐 12. SSH (Remote Access)
### What is SSH?
- Secure protocol to access remote systems
### Usage
1. `ssh username@ip`
2. Enter password
---
## 🗂️ 13. Important System Files
- `/etc/passwd` → User info
- `/etc/shadow` → Passwords
- `/etc/sudoers` → sudo permissions
- `/var/log` → Logs
### Important Logs
- `/var/log/auth.log` → Authentication
- `/var/log/syslog` → System events
---
## ⚙️ 14. Utility Commands
- `date` → Current date/time
- `cal` → Calendar
- `clear` → Clear terminal
- `Ctrl + L` → Clear view only
- `history` → Show commands
- `!<num>` → Repeat command
- `man <command>` → Manual
- `whatis <command>` → Short description
- `echo "text"` → Print text
---
