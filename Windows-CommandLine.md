# 🪟 Windows Command Line – CAPT Lab Writeup

## 👨‍💻 Author
Shaik Amanulla  
CAPT Certification Candidate  

---

## 📌 Lab Objective
The objective of this module was to gain hands-on experience using Windows Command Line and PowerShell for system administration and security-related tasks.  
The lab focused on user enumeration, services analysis, Active Directory queries, file permissions, and system information gathering using command-line tools.

---

## 🖥️ Lab Environment
- Platform: Hackviser CAPT (HackerBox)
- Access Method: SSH
- Username: Administrator
- Tools Used: PowerShell, Command Prompt

---

## 🔐 Initial Access
Connected to the Windows machine using SSH credentials provided in the lab environment and accessed PowerShell for command-line operations.

---

## 🔍 Tasks Performed

### 1. PowerShell Alias Enumeration
Identified the command behind a custom alias.

**Command used:**
```powershell
Get-Alias HoldenManeuver

Result:
Alias corresponded to:

Get-Runspace
2. File & Directory Enumeration

Counted number of files in Books directory.

(Get-ChildItem Documents\Books).Count

Result: 9 files found.

3. Process Enumeration

Identified cmdlet used to display running processes.

Get-Process

Used to monitor active processes on system.

4. Service Enumeration

Checked services containing specific keyword.

(Get-Service *MCRN*).Count

Result: 5 services found.

5. Active Directory User Enumeration

Identified number of active users in domain.

(Get-ADUser -Filter {Enabled -eq $True}).Count

Result: 10 active users.

6. Local Group Analysis

Identified local group related to certificates.

Get-LocalGroup | Where-Object {$_.Description -like "*cert*"}

Result: Cert Publishers group.

7. File Download Command

Identified PowerShell cmdlet used to download files.

Invoke-WebRequest
8. System Information Enumeration

Retrieved Windows build number.

(Get-CimInstance Win32_OperatingSystem).BuildNumber

Result: Build 17763.

9. Installed Updates Enumeration

Checked installed Windows updates.

Get-HotFix

Result: KB4464455 installed.

10. File Permission Analysis

Analyzed permissions of file "Abaddon's Gate".

(Get-Acl "Documents\Books\Abaddon's Gate*").Access

Identified user with read-only permission:

c.avasarala
🧠 Skills Gained

PowerShell command usage

Windows service enumeration

Active Directory user analysis

File permission investigation

System information gathering

Update and patch enumeration

Command-line based system administration

🎯 Conclusion

This module provided practical exposure to Windows command-line operations and PowerShell-based system investigation techniques.
The tasks performed are directly relevant to real-world system administration and cybersecurity environments, strengthening practical command-line proficiency in Windows systems.


---

# 📌 Add this in main README also (below modules list)
Add line:


✅ Windows Command Line
