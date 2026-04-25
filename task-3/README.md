# 🔐 Task-3: Web Application Security Testing (DVWA)

## 📌 Overview

This project demonstrates basic web application vulnerabilities using **DVWA (Damn Vulnerable Web Application)** on Kali Linux.
The goal is to understand how common attacks work and how they can be identified.

---

## 🛠️ Environment Setup

* OS: Kali Linux (VirtualBox)
* Tool: DVWA
* Web Server: Apache2
* Database: MySQL/MariaDB

---

## 🚀 Setup Steps

1. Clone DVWA:

```bash
cd /var/www/html
sudo git clone https://github.com/digininja/DVWA.git dvwa
```

2. Set permissions:

```bash
sudo chmod -R 777 /var/www/html/dvwa
```

3. Start services:

```bash
sudo service apache2 start
sudo service mysql start
```

4. Configure database:

```bash
sudo mysql
```

```sql
CREATE DATABASE dvwa;
CREATE USER 'dvwa'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON dvwa.* TO 'dvwa'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```

5. Open in browser:

```
http://localhost/dvwa
```

---

## 🔍 Vulnerabilities Tested

### 1️⃣ SQL Injection

* Input used:

```sql
1 OR 1=1
```

* Result: Bypassed authentication / retrieved data
* Impact: Unauthorized database access

---

### 2️⃣ Cross-Site Scripting (XSS)

* Payload:

```html
<script>alert('XSS')</script>
```

* Result: Popup alert executed
* Impact: Client-side script injection

---

### 3️⃣ CSRF (Cross-Site Request Forgery)

* Action: Changed password without proper validation
* Result: Password updated successfully
* Impact: Unauthorized actions on behalf of user

---

## 📸 Output

(Screenshots of each attack can be added here)

---

## 📚 Key Learnings

* Importance of input validation
* Secure authentication mechanisms
* Protection against client-side attacks
* Need for CSRF tokens

---

## ⚠️ Disclaimer

This project is for **educational purposes only**.
All testing was performed in a controlled lab environment.

---


