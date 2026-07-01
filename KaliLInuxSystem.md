# Kali Linux System & Networking Exercise

## Overview

Hands-on Linux exercise covering essential system administration and networking
tasks on Kali Linux, including file management, permissions, user management,
and network reconnaissance commands.

**Category:** Linux System Administration

**Tools:** Kali Linux, Bash

**OS:** Kali GNU/Linux 2025.4 (kali-rolling)

---

## Part 1 — Folder, File, and Encoding Task

### Objectives

- Create directories and files using CLI
- Encode data using Base64
- Move files between directories
- Check disk usage

### Commands Used

```bash
# Create a new directory
mkdir Assignment_20260302

# Create a text file using nano
nano mission.txt

# Encode a string using Base64
echo "Oscar" | base64
# Output: T3NjYXIK

# Save encoded output to a file
nano encoded_name.b64

# Move file to home directory
mv encoded_name.b64 ~

# Check disk usage
df -h

# List files in directory
ls
```

### Key Takeaways

- `mkdir` creates directories; `nano` is a basic text editor in Linux
- `base64` encodes strings — widely used in data transmission and obfuscation
- `df -h` shows disk usage in human-readable format
- `mv` moves files between directories

---

## Part 2 — System Information

### Objectives

- Retrieve OS and kernel information
- Identify current user and session details

### Commands Used

```bash
# Display OS release information
cat /etc/os-release

# Display distribution information
lsb_release -a

# Display kernel version
uname -r

# Display hostname
hostname

# Display current user
whoami

# Display logged-in users
who
```

### Output Summary

| Command | Output |
| --- | --- |
| `uname -r` | 6.17.10+kali-amd64 |
| `hostname` | kali |
| `whoami` | student |

### Key Takeaways

- `cat /etc/os-release` and `lsb_release -a` provide detailed OS information
- `uname -r` identifies the kernel version — useful for vulnerability assessment
- `whoami` and `who` help identify active sessions during incident response

---

## Part 3 — File Permissions

### Objectives

- Understand Linux permission structure
- Modify file permissions using `chmod`
- Check system uptime

### Commands Used

```bash
# Check system uptime
uptime

# Create a new file
touch 043679.txt

# List files with permissions
ls -l

# Set permissions to owner read/write only (600)
chmod 600 043679.txt

# Create a shared file with read/write for all (666)
touch shared.txt
chmod 666 shared.txt
```

### Permission Reference

| Permission | Numeric | Description |
| --- | --- | --- |
| `rw-------` | 600 | Owner read/write only |
| `rw-rw-rw-` | 666 | Read/write for all users |
| `rwxrwxr-x` | 775 | Full owner/group, read/execute others |

### Key Takeaways

- Linux permissions follow owner/group/others structure
- `chmod 600` restricts access to owner only — important for sensitive files
- `chmod 666` allows all users to read and write — use with caution
- `ls -l` reveals permission strings for all files in a directory

---

## Part 4 — User Management

### Objectives

- Create and manage user accounts
- Assign and update passwords
- Verify user information

### Commands Used

```bash
# Add a new user
sudo adduser Oscar

# Change user password
sudo passwd Oscar

# Display user ID and group membership
id Oscar

# Search for user in passwd file
grep Oscar /etc/passwd
```

### Output Summary