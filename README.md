# security-projects

## Introduction

Welcome to my portfolio! I'm an Aspiring Cybersecurity Analyst passionate about Threat Hunting, OSINT, Phishing Analysis, and Strengthing IT Security. This portfolio showcases my practical skills and projects related to security operations.

## Projects

-   [Basic Log Analysis with grep](#basic-log-analysis-with-grep)
-   [Project 2 Title](#project-2-title)
-   [Project 3 Title](#project-3-title)

## Tools and Technologies

-   Splunk
-   Wireshark
-   Nessus Essentials
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
    1753
-   The log file contained 9152 200 OK status codes.

### Example Commands

```bash
grep "404" apache.logs | wc -l
awk '{print $1}' apache.logs | sort -u | wc -l
grep "200" apache.logs | wc -l

---

## Project 2 Title

### Description

[Detailed description of your second project.]

... (Continue with the rest of the project structure)
