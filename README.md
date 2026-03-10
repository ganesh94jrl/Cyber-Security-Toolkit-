# 🔐 Cyber Security Toolkit (Python)

## 📌 Project Overview

The **Cyber Security Toolkit** is a Python-based command-line security tool that demonstrates fundamental cybersecurity and network security techniques.

This toolkit integrates multiple modules that simulate basic penetration testing and network monitoring tasks such as:

* Web vulnerability scanning
* Website link crawling
* Packet sniffing
* Directory discovery
* Network information collection
* Port scanning

The project is designed mainly for **learning cybersecurity concepts, building a portfolio project, and explaining practical security concepts during interviews.**

---

# 🎯 Objectives

The primary objectives of this project are:

* Understand **web security vulnerabilities**
* Learn **network monitoring techniques**
* Implement **basic penetration testing tools**
* Practice **Python networking and security libraries**
* Demonstrate cybersecurity knowledge in interviews

---

# 🧰 Technologies Used

| Technology          | Purpose                               |
| ------------------- | ------------------------------------- |
| Python              | Main programming language             |
| requests            | Send HTTP requests                    |
| BeautifulSoup (bs4) | Parse HTML and extract links          |
| Scapy               | Packet sniffing                       |
| socket              | Network communication & port scanning |
| urllib.parse        | URL handling                          |

---

# 🏗 System Architecture

The project follows a **modular architecture** where each security function works as an independent module controlled by a central menu system.

```
                 +----------------------+
                 |   User / Security    |
                 |        Analyst       |
                 +----------+-----------+
                            |
                            v
                 +----------------------+
                 |   Cyber Security     |
                 |      Toolkit         |
                 |     (Main Menu)      |
                 +----------+-----------+
                            |
      -----------------------------------------------------
      |          |           |          |         |        |
      v          v           v          v         v        v

+------------+ +------------+ +------------+ +------------+ +------------+ +------------+
|Vulnerability| |   Link     | |  Packet    | | Directory  | |  Network   | |   Port     |
|  Scanner    | |  Crawler   | |  Sniffer   | |  Scanner   | |Information | |  Scanner   |
+------------+ +------------+ +------------+ +------------+ +------------+ +------------+
      |              |              |              |              |              |
      v              v              v              v              v              v

HTTP Requests   HTML Parsing    Network Packet    URL Requests   System Info   TCP Socket
 & Payloads     with BS4        Monitoring        & Wordlist     Retrieval     Connection
```

---

# ⚙️ Toolkit Features

The toolkit contains **six main security modules**.

---

# 1️⃣ Vulnerability Scanner

This module checks websites for basic web application vulnerabilities.

### SQL Injection Test

The program sends a malicious SQL payload to test database security.

Payload used:

```
' OR '1'='1
```

If the website returns database-related error messages, the scanner detects possible SQL injection.

Example Output:

```
[SQL Injection Possible] http://example.com/page?id=1
```

---

### Cross-Site Scripting (XSS) Test

The scanner sends a JavaScript payload to check if user input is properly sanitized.

Payload:

```
<script>alert('XSS')</script>
```

If the script appears in the response page, the application might be vulnerable to XSS attacks.

Example Output:

```
[XSS Vulnerable] http://example.com/search?q=test
```

---

# 2️⃣ Link Crawler

The link crawler scans a webpage and extracts all hyperlinks.

The tool reads HTML `<a>` tags and collects their `href` values.

Example Output:

```
Links discovered: 18

http://example.com/login
http://example.com/products
http://example.com/cart
```

This simulates the **reconnaissance phase of ethical hacking**, where attackers analyze website structure.

---

# 3️⃣ Packet Sniffer

The packet sniffer captures network packets traveling through the local system.

It uses the **Scapy library** to inspect network traffic.

Example Output:

```
Packet: 192.168.1.78 -> 172.64.146.215
Packet: 172.64.146.215 -> 192.168.1.78
```

### Meaning

| Component      | Description                 |
| -------------- | --------------------------- |
| Source IP      | Device sending the packet   |
| Destination IP | Device receiving the packet |

This demonstrates how network monitoring tools analyze real-time communication.

---

# 4️⃣ Directory Scanner

Many websites hide administrative or sensitive directories.

This module tries to discover common hidden directories such as:

```
/admin
/login
/dashboard
/backup
/uploads
/config
```

Example Output:

```
Scanning Directories...

[FOUND] http://example.com/admin
```

This technique is widely used in **web penetration testing**.

---

# 5️⃣ Network Information Module

This module collects basic system network information.

Example Output:

```
System Network Information

Hostname: Dell-PC
Local IP: 192.168.1.78
```

### Explanation

| Information | Meaning                             |
| ----------- | ----------------------------------- |
| Hostname    | Name of the computer                |
| Local IP    | Device address inside local network |

Private IP ranges include:

```
192.168.x.x
10.x.x.x
172.16.x.x
```

---

# 6️⃣ Port Scanner

The port scanner checks if specific network ports are open on a target system.

Example ports scanned:

| Port | Service |
| ---- | ------- |
| 21   | FTP     |
| 22   | SSH     |
| 80   | HTTP    |
| 443  | HTTPS   |
| 3306 | MySQL   |

Example Output:

```
Scanning Ports...

Open Port: 80 (HTTP)

Scan Completed
```

If a TCP connection is successful, the port is considered **open**.

---

# 🗂 Project Structure

```
CyberSecurityToolkit/
│
├── cyber_security_toolkit.py
└── README.md
```

---

# 🖥 Installation Guide

## Step 1 — Install Python

Check Python installation:

```
python --version
```

---

## Step 2 — Install Required Libraries

Install dependencies using pip:

```
pip install requests
pip install beautifulsoup4
pip install scapy
```

---

# ▶️ Running the Program

Run the toolkit using terminal or VS Code:

```
python cyber_security_toolkit.py
```

Main menu appears:

```
Cyber Security Toolkit

1. Vulnerability Scanner
2. Link Crawler
3. Packet Sniffer
4. Directory Scanner
5. Network Information
6. Port Scanner
7. Exit
```

---

# 🧪 Safe Testing Website

You can test this project on intentionally vulnerable websites like:

testphp.vulnweb.com

These platforms are designed for learning cybersecurity safely.

---

# 📚 Security Concepts Demonstrated

This project demonstrates several cybersecurity techniques:

* Web vulnerability scanning
* SQL Injection testing
* Cross-site scripting detection
* Web crawling and reconnaissance
* Packet sniffing
* Network monitoring
* Directory enumeration
* Port scanning

---

# ⚠️ Ethical Usage Disclaimer

This toolkit is intended **only for educational purposes**.

Do NOT use this tool against:

* Government websites
* Corporate networks
* Websites without permission

Unauthorized scanning may violate cybersecurity laws.

---

# 🚀 Future Improvements

The toolkit can be enhanced by adding:

* Subdomain enumeration
* Login brute force testing
* Password strength analyzer
* Automated vulnerability report generation
* GUI interface using Python
* Integration with advanced security tools

---

# 👨‍💻 Author

Ganesh Kuppasta
Electronics and Communication Engineering Student

Areas of Interest:

* Cybersecurity
* Networking
* Ethical Hacking
* Python Security Tools

---

# 📌 Conclusion

The **Cyber Security Toolkit** demonstrates how common penetration testing techniques work internally using Python.

This project helps beginners gain **hands-on experience with cybersecurity concepts, network analysis, and vulnerability detection** while also serving as a strong portfolio project for cybersecurity and network engineering roles.

