
# 🪟 Windows-Fundamentals.md
Create file → paste:

```markdown
# 🪟 Windows Fundamentals Lab Writeup

## 📌 Objective
To perform Windows system investigation and understand core administrative and security features including users, services, startup programs, and firewall configurations.

---

## 🖥️ Lab Environment
- Platform: HackerBox
- Access: RDP (Remote Desktop)
- User: Administrator
- OS: Windows

---

## 🔍 Tasks Performed

### 1. User Enumeration
Accessed Local Users and Groups to identify system users.

**Tool Used:**
lusrmgr.msc


Analyzed available user accounts and their details.

---

### 2. Folder Permission Analysis
Checked folder permissions to identify users with read and execute access.

**Method:**
- Right-click folder → Properties
- Security tab → Check permissions

This helps in detecting unauthorized access.

---

### 3. Startup Program Investigation
Identified unusual startup programs configured to run during system boot.

**Tool Used:**
Task Manager → Startup tab


Detected suspicious executable configured for startup.

---

### 4. Service Monitoring
Analyzed Windows services and checked their operational status.

**Command:**
services.msc


Reviewed service configuration and status.

---

### 5. Process Enumeration
Listed running processes using command prompt.

**Command:**
```cmd
tasklist
Useful for monitoring system activity.

6. Firewall Configuration Review

Checked applications allowed through Windows Defender Firewall.

Path:

Windows Defender Firewall → Allow an app

Identified unusual application allowed through firewall.

🧠 Skills Gained

Windows system enumeration

User & permission analysis

Startup persistence detection

Service monitoring

Firewall review

Process monitoring

🎯 Conclusion

This lab provided hands-on experience in Windows system administration and security analysis. These skills are essential for cybersecurity professionals in detecting misconfigurations, persistence mechanisms, and suspicious activities.


---

🚀 Documenting My CAPT Cybersecurity Lab Journey

I’ve started documenting my hands-on cybersecurity lab work from CAPT Certification on GitHub.

Completed so far:
• Linux Fundamentals Lab
• Windows Fundamentals Lab

These labs focus on real-world system investigation, enumeration, and security analysis using both Linux and Windows environments.

This repository will serve as my practical cybersecurity learning portfolio as I continue progressing in ethical hacking and security analysis.

GitHub Repository:
[Paste your GitHub link here]
