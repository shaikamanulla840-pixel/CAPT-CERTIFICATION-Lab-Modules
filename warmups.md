# 🔰 CAPT Certification — Warmup Labs
## Author: Amanulla Shaik

This document contains warmup machines completed as part of the CAPT Certification practical labs.  
These exercises focus on basic service enumeration, remote access, and initial penetration testing techniques.

---

# 🖥️ Warmup 1 — Arrow (Telnet Basics)

## 🎯 Objective
Practice basic enumeration and remote access using the Telnet service.

---

## 🔎 Step 1 — Port Scanning
A network scan was performed to identify open ports on the target machine.

```bash
nmap -sV <target-ip>

✅ Finding

Open port discovered:

23/tcp open telnet

Answer: 23

🔎 Step 2 — Service Identification

Port 23 corresponds to the Telnet service.

Answer: telnet

📝 Explanation

Telnet is a remote login protocol that provides command-line access to systems over a network. It does not use encryption and is considered insecure.

🔎 Step 3 — Banner Grabbing & Hostname Enumeration

Connected to the Telnet service:

telnet <target-ip> 23

The login banner revealed the hostname.

Answer: arrow

📝 Explanation

Banner grabbing helps identify system information such as hostname, OS, or running services.

🔎 Step 4 — Telnet Login Credentials

Default credentials were tested and successful login was achieved.

Answer:

root:root
📝 Explanation

Weak or default credentials are a major security vulnerability and commonly exploited in penetration testing.

🔎 Step 5 — Working Directory Enumeration

After successful login, the working directory was identified.

pwd

Answer:

/root
📝 Explanation

The working directory shows the current location of the logged-in user. In this case, access was obtained directly to the root user's home directory.

🧠 Skills Practiced

Network scanning using Nmap

Service enumeration

Banner grabbing

Telnet remote access

Default credential testing

Basic Linux enumeration

🏁 Conclusion

The Arrow warmup machine demonstrated the risks associated with exposed Telnet services and weak authentication. Proper service configuration and secure credentials are essential to prevent unauthorized access.

This lab strengthened foundational penetration testing skills required for real-world cybersecurity assessments.

# 🔰 Warmup Lab — File Hunter (FTP Basics)
## CAPT Certification Practice

### 👨‍💻 Author
Amanulla Shaik  
CAPT Certification Candidate | Cybersecurity Enthusiast  

---

# 🧠 Lab Overview
This warmup focuses on understanding the FTP (File Transfer Protocol) service and practicing basic enumeration techniques. The objective of this lab was to identify open ports, connect to an FTP server, enumerate available files, and retrieve sensitive information.

---

# 🎯 Target Information
**Target IP:** 172.20.11.194  
**Service:** FTP  
**Difficulty:** Basic  

---

# 🔎 Q1. Which port(s) are open?

A network scan was performed using Nmap to identify open ports on the target system.

```bash
nmap -sV 172.20.11.194

Result
21/tcp open ftp
✅ Answer:

21

📝 Explanation

Port 21 is the default port used by the FTP service. Identifying open ports helps determine which services are exposed on the target machine and can be used for further enumeration.

🔎 Q2. What does FTP stand for?
✅ Answer:

File Transfer Protocol

📝 Explanation

FTP stands for File Transfer Protocol. It is used to transfer files between computers over a network. It allows users to upload, download, and manage files on remote servers.

🔎 Q3. What username did you connect to the FTP?

Connected to FTP server:

ftp 172.20.11.194

Anonymous login was allowed.

✅ Answer:

anonymous

📝 Explanation

Anonymous login allows users to access the FTP server without a specific account. This is often misconfigured and can expose sensitive data if not properly secured.

🔎 Q4. What command shows which commands we can use on the FTP server?

Inside FTP session:

help
✅ Answer:

help

📝 Explanation

The help command displays all available FTP commands such as upload, download, directory listing, and navigation. This helps in understanding server capabilities.

🔎 Q5. What is the name of the file on the FTP server?

Listed files using:

ls
Result
userlist
✅ Answer:

userlist

📝 Explanation

Directory listing revealed a file named userlist on the FTP server. Identifying available files is important during enumeration.

🔎 Q6. What is the command used to download a file from an FTP server?

To download file:

get userlist
✅ Answer:

get

📝 Explanation

The get command is used in FTP to download files from a remote server to the local machine. This allows attackers or testers to retrieve sensitive data.

🔎 Q7. Which users' information is in the file?

After downloading file:

cat userlist
Result
jack
root
✅ Answer:

jack, root

📝 Explanation

The downloaded file contained usernames stored on the FTP server. Such information can be used for further authentication attacks like brute-force or password guessing.

🧠 Skills Practiced

Network scanning with Nmap

FTP enumeration

Anonymous FTP login

File discovery on FTP server

Downloading files from FTP

Extracting user information

🏁 Conclusion

This lab demonstrated how misconfigured FTP services with anonymous login can expose sensitive information. By enumerating the FTP server and downloading available files, user account details were discovered. Proper authentication controls and restricted file access are essential to secure FTP services.
