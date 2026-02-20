# 🌐 Network Scanning with Nmap – CAPT Lab Writeup

## 👨‍💻 Author
Shaik Amanulla  
CAPT Certification Candidate  

---

## 📌 Objective
The objective of this lab was to perform network scanning and service enumeration using Nmap.  
This module focused on identifying open ports, running services, service versions, and understanding various Nmap scanning parameters used in real-world network reconnaissance.

---

## 🖥️ Lab Environment
- Platform: Hackviser CAPT (HackerBox)
- Tool Used: Nmap
- Access: Linux Terminal
- Target: Provided lab machine

---

## 🔍 Tasks Performed

### 1. Service Version Detection
Performed detailed service scan to identify running services and versions.

**Command used:**
```bash
nmap -sV <target-ip>

Identified Apache service and its version running on a custom port.

Result:
Apache httpd 2.4.56 ((Debian))

2. Specific Port Service Identification

Scanned specific port to identify service version.

nmap -sV -p 48390 <target-ip>

Result:
nginx 1.18.0

3. Top 100 Ports Scan

Scanned most common ports and identified highest open port.

nmap --top-ports 100 <target-ip>

Result:
Highest open port: 3306 (MySQL)

4. FTP Service Identification

Detected FTP service running on target system.

nmap <target-ip>

Result:
FTP running on port 21

🧠 Nmap Parameters Learned
Parameter	Function
-sn	Disable port scan (host discovery only)
--top-ports	Scan most common ports
-p	Specify port(s)
-A	Aggressive scan
-sT	TCP Connect scan
-sI	Idle scan
-T0	Paranoid timing
-sV	Version detection
🧠 Skills Gained

Network reconnaissance using Nmap

Service and version detection

Port enumeration techniques

Understanding scanning parameters

Identifying running network services

Practical network investigation

🎯 Conclusion

This lab provided hands-on experience in network scanning and service enumeration using Nmap.
The tasks performed helped in understanding how security professionals identify open ports, running services, and system information during network reconnaissance.
These skills are essential for cybersecurity analysis, vulnerability assessment, and network monitoring.


---

# 📌 Also update main README
Add line under modules:


✅ Network Scanning with Nmap
