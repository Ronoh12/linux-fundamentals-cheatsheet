<# Linux Fundamentals Cheatsheet
**Author:** Rodgers Kiptoo Rono • **Location:** Berlin, Germany 
**Project:** Hands-on Linux command practice on Ubuntu Server and Kali Linux.

---

## 📌 Overview
This repo documents fundamental Linux commands and small exercises I performed in my VirtualBox lab (Ubuntu Server as target, Kali as attacker). It demonstrates file management, users & permissions, process monitoring, networking, and package management skills — useful for sysadmin and blue-team roles.

---

## 🛠️ Tools & Environment
- Virtualization: Oracle VirtualBox (Internal Network `lab-net`) 
- VMs: **Ubuntu Server** (IP: **192.168.56.10**) • **Kali Linux** (IP: **192.168.56.105**) 
- OS: Ubuntu 20.04 LTS (Server), Kali Linux 2023.x

---

## ✅ What I did
1. Practiced basic filesystem and directory ops. 
2. Managed users and file permissions. 
3. Monitored processes and system health. 
4. Performed basic network checks and package management.

---

## 🔧 Key Commands (examples)

### File & Directory
pwd
ls -la
cd /etc
mkdir test_dir
touch test.txt
cp test.txt test_copy.txt
mv test_copy.txt moved.txt
rm moved.txt

### User & Permission
whoami
id
sudo adduser testuser
sudo chown testuser:testuser test.txt
chmod 644 test.txt

### Processes & System
ps aux | head -n 10
top -b -n 1 | head -n 20
kill -9 <PID>
df -h
free -m
uptime

### Networking
ip a
ping -c 3 192.168.56.10
curl -I http://example.com
ss -tulpn

### Package Management (Ubuntu)
sudo apt update
sudo apt install -y htop
dpkg -l | grep htop
sudo apt remove -y htop
# 🐧 Linux Fundamentals Cheatsheet

**Project Goal:**  
Document key Linux commands and collect system evidence from both Kali and Ubuntu environments.

---

## 📂 Evidence

- screenshots/ubuntu-ip-a.txt
- screenshots/ubuntu-etc-ls.txt
- screenshots/ubuntu-pwd-whoami.txt

---

## 🧪 How to Reproduce

1. Create Ubuntu Server and Kali Linux VMs in VirtualBox on the same **Internal Network (lab-net)**.
2. SSH from Kali into Ubuntu:
   ```bash
   ssh rkruser@192.168.56.10
