# Blue Team Incident Investigation Report

## Overview
This repository contains my Blue Team investigation reports completed as part of the **R.I.S.K. Company CTF 2026 Internship**. The objective was to investigate network traffic, Windows event logs, and phishing incidents to identify attacker activities and document the complete attack timeline.

---

## Objectives

- Investigate network traffic using Wireshark
- Analyze Windows Event Logs
- Detect attacker techniques and persistence
- Investigate phishing email activity
- Document Indicators of Compromise (IOCs)
- Recommend containment actions

---

## Investigation Tasks

### Task 1 – Network Traffic Analysis (Wireshark)

**File:** `attack.pcap`

Performed:

- HTTP traffic analysis
- Directory enumeration detection (Gobuster)
- HTTP status code analysis
- Credential exposure identification
- Git repository exposure detection
- Login attempt investigation
- Malware download verification
- DNS traffic analysis
- SMB traffic analysis
- HTTP POST request analysis

**Key Findings**

- Gobuster directory enumeration detected
- Exposed backup file containing credentials
- Publicly accessible `.git` repository
- Multiple unauthorized login attempts
- No malware download observed
- No SMB communication
- No DNS activity

---

### Task 2 – Windows Event Viewer Investigation

**File:** `CTF-AttackTimeline.evtx`

Analyzed Windows Security Logs including:

- Event ID 4625 – Failed Logon
- Event ID 4624 – Successful Logon
- Event ID 4672 – Special Privileges
- Event ID 4688 – Process Creation
- Event ID 4698 – Scheduled Task Creation
- Event ID 4720 – User Account Creation
- Event ID 1102 – Audit Log Cleared

**Key Findings**

- Multiple RDP brute-force attempts
- Successful attacker login
- System discovery commands executed
- Scheduled task created
- New user account created
- Audit logs cleared

---

### Task 3 – Phishing Investigation

Performed:

- Email header analysis
- SPF, DKIM and DMARC validation
- Malicious URL investigation
- ZIP attachment analysis
- Web proxy log analysis
- DNS investigation
- EDR event correlation
- IOC collection
- Containment recommendation

**Key Findings**

- Phishing email delivered
- Fake onboarding website detected
- Malicious ZIP attachment opened
- Suspicious domains accessed
- WIN-A017 identified as the first host for containment

---

## MITRE ATT&CK Techniques

- Reconnaissance
- Credential Access
- Discovery
- Persistence
- Defense Evasion

---

## Tools Used

- Wireshark
- Windows Event Viewer
- HTTP Filters
- Security Event Logs
- Web Proxy Logs
- DNS Logs
- EDR Logs

---

## Skills Demonstrated

- Network Traffic Analysis
- Threat Hunting
- Digital Forensics
- Log Analysis
- Incident Response
- IOC Extraction
- Windows Security Investigation
- Phishing Investigation
- SOC Analysis

---

## Repository Contents

```
├── Incident Investigation Report.pdf
├── Screenshots/
├── README.md
```

---

## Author

**Risha Gupta**

MCA (Cybersecurity)

Aspiring SOC Analyst | Blue Team | Digital Forensics | Threat Detection
