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
