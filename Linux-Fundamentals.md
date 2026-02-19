# 🐧 Linux Fundamentals Lab Writeup

## 📌 Objective
The objective of this lab was to gain practical experience in Linux system navigation, file handling, permissions, and basic enumeration techniques used in cybersecurity and penetration testing.

---

## 🖥️ Lab Environment
- Platform: HackerBox
- OS: Debian Linux
- Access: Terminal-based
- User: captain

---

## 🔍 Tasks Performed

### 1. Hidden File Discovery
Identified hidden files within directories and accessed sensitive information using Linux commands.

**Command Used:**
```bash
ls -la
cat .filename

This demonstrated how attackers or analysts locate hidden configuration files.

2. Word Count Analysis

Analyzed file content and counted words using Linux utilities.

Command:
wc -w filename
Useful for log analysis and content inspection.

3. Credential Enumeration

Extracted email and password combinations stored in system files.

Command:

tail -n 1 filename
grep "keyword" filename

Shows importance of securing credential files.

4. File Permission Modification

Modified file permissions to access restricted files.

Command:

chmod +r filename

Demonstrates Linux permission handling and privilege concepts.

5. File Location Enumeration

Searched entire system for configuration files.

Command:

find / -name filename 2>/dev/null

Common technique in penetration testing.

6. User Enumeration

Identified UID and user details.

Command:

id username

Useful in privilege escalation and system auditing.

🧠 Skills Gained

Linux command-line navigation

File permission analysis

Credential discovery techniques

System enumeration

Security awareness in Linux

🎯 Conclusion

This lab provided foundational knowledge of Linux system operations and security investigation techniques used in real-world cybersecurity scenarios.


---


#CyberSecurity #EthicalHacking #Linux #WindowsSecurity #CAPT #HandsOnLearning
