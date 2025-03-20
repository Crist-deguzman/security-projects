# security-projects

## Introduction

Welcome to my portfolio! I'm an Aspiring Cybersecurity Analyst passionate about Threat Hunting, OSINT, Phishing Analysis, and Strengthing IT Security. This portfolio showcases my practical skills and projects related to security operations.

## Projects

-   [Basic Log Analysis with grep](#basic-log-analysis-with-grep)
-   Simulated Phishing Incident Analysis and Reporting(#simulated-phishing-incident-analysis-and-reporting)
-   [Project 3 Title](#project-3-title)

## Tools and Technologies

-   Splunk
-   Wireshark
-   Kali Linux
-   Snort/Suricata
-   Python
-   Bash/PowerShell
-   Linux/Windows administration

## Certifications and Training

-   Blue Team Level 1 (BTL1), Certified Network Security Practitioner (CNSP), and CompTIA Security+
-   Google Cybersecurity Specialization Course

## Contact

-   LinkedIn Profile - http://www.linkedin.com/in/cristopher-de-guzman-17a241268

---

## Basic Log Analysis with grep

### Description

This project involved analyzing a sample web server access log to identify common HTTP status codes and IP addresses using `grep` and `awk`. The goal was to demonstrate basic log analysis skills.

### Tools Used

-   'grep'
-   'awk'

### Key Findings

-   The log file contained [216] 404 errors.
-   The amount of unique IP addresses that accessed the server were
    [1753].
-   The log file contained [9152] 200 OK status codes.

### Example Commands

```bash
grep "404" access.log | wc -l
awk '{print $1}' access.log | sort -u
grep "200" access.log | wc -l
```

---

## Simulated Phishing Incident Analysis and Reporting

### Description

Conducted a simulated phishing attack in a controlled virtual environment to analyze attack vectors, identify indicators of compromise (IOCs), and develop an incident response report. This project showcases my ability to simulate real-world security incidents, perform log analysis, and provide actionable recommendations.

... (Continue with the rest of the project structure)
