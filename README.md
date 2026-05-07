# Cybersecurity Portfolio SOC(L1)

AD brute force, phishing, malware, Linux priv esc, honeypot, SSH attack - investigated and documented.

## 👁️ Overview

**Here's what I've done:**

➣ **Built an Active Directory lab** (Domain Controller, Windows 10, Kali, Splunk) and detected a brute force attack live - from failed logins to successful authentication.  
➣ **Tore apart a phishing email** that looked legitimate. Found the real attachment (ZIP inside a PDF), extracted metadata, and identified the attacker.  
➣ **Followed malware on the wire** using Wireshark: saw the download, the beacon, and the data being smuggled out via SMTP.  
➣ **Walked in an attacker's shoes** on a Linux server - from www‑data to root. Every bash command, every mistake they made.  
➣ **Investigated a honeypot** that got hit. Reconstructed the timeline using auth.log, Apache logs, and firewall changes.  
➣ **Responded to an SSH brute force** - traced the IP, the compromised account, persistence, and executed commands.
➣ **Tracked an attacker who needed no malware** - just PowerShell commands to gut Windows defenses. Found how they disabled LSA protection, killed Defender, patched AMSI, and wiped PowerShell history logging.


## 📂 Projects 

### 1. Active Directory Brute Force Detection (Splunk)
**What I built:** Complete SOC lab from scratch (Windows Server AD + Windows 10 + Kali + Splunk). Simulated brute force attack, forwarded Windows Event Logs via Universal Forwarder + Sysmon, detected the attack in Splunk, and documented full incident response.  
[<ins>**Read the full lab**</ins>](https://github.com/CybersecurityPaladin/AD-BruteForce-Detection) 

### 2. Phishing Email Investigation
**What I analyzed:** Suspicious email targeting a government representative. Extracted Reply-To deception, recovered ZIP masquerading as PDF, discovered attacker name from metadata, and decoded Base64 location from XML.  
[<ins>**Read the full lab**</ins>](https://github.com/CybersecurityPaladin/Phishing-Email-Analysis)

### 3. Malware Network Traffic Analysis (Wireshark)
**What I investigated:** PCAP from an accountant who clicked a malicious invoice link. Traced DNS behavior, HTTP payload delivery, and SMTP exfiltration.  
[<ins>**Read the full lab**</ins>](https://github.com/CybersecurityPaladin/Malware-Network-Analysis)

### 4. Privilege Escalation Log Analysis (Linux)
**What I analyzed:** Web server where sensitive data was leaked from root-only access. Examined www-data user activity, bash history, and system logs to identify how a PHP-based web server was escalated to full root.  
[<ins>**Read the full lab**</ins>](https://github.com/CybersecurityPaladin/Privilege-Escalation-Log-Analysis)

### 5. Honeypot Intrusion Detection (Linux Environment)
**What I analyzed:** Compromised webserver honeypot. Investigated auth.log, Apache access/error logs, and system logs to answer 8 specific detection tasks.  
[<ins>**Read the full lab**</ins>](https://github.com/CybersecurityPaladin/Honeypot-Intrusion-Linux-Analysis)

### 6. SSH Brute Force Detection & Incident Response
**What I analyzed:** SSH brute force attack leading to compromise. Identified attacker IP, compromised account, session details, persistence methods, and executed commands.  
[<ins>**Read the full lab**</ins>](https://github.com/CybersecurityPaladin/SSH-BruteForce-Analysis)

### 7. Suspicious PowerShell Commands (Defense Evasion)
**What I uncovered:** An attacker who didn't bother with malware - just used native PowerShell to tear down every security control in Windows. Disabled LSA protection, killed Windows Defender, patched AMSI, and even turned off PowerShell history logging. All without a single alert.
[<ins>**Read the full lab**</ins>](https://github.com/CybersecurityPaladin/Suspicious-PS-Commands)

## 🛠️ Core Skills

| Skill | Where I used it |
|:-------:|:-----------------:|
| Splunk (SIEM) | AD Brute Force lab - search queries, event correlation, alerting |
| Wireshark | Malware traffic analysis - DNS, HTTP, SMTP reconstruction |
| Linux Log Analysis | Privilege Escalation + Honeypot - auth.log, Apache logs, bash history |
| Windows Event Logs | AD Brute Force - 4625, 4624, Sysmon |
| MITRE ATT&CK | Mapping attack techniques across all investigations |
| CyberChef, VirusTotal | Phishing + Malware analysis |
| Active Directory | Domain controller setup, user auth logging |
| Atomic Red Team | (Reference from training) |
| Windows Event Logs (4657, 4104) | Suspicious PS Commands


## 📚 Learning Platforms
TryHackMe, Hack The Box, BlueTeam Labs, CyberDefenders

