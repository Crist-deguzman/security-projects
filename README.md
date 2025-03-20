# security-projects

## Introduction

Welcome to my portfolio! I'm an Aspiring Cybersecurity Analyst passionate about Threat Hunting, OSINT, Phishing Analysis, and Strengthing IT Security. This portfolio showcases my practical skills and projects related to security operations.

## Projects

-   [Basic Log Analysis with grep](#basic-log-analysis-with-grep)
-   [File Integrity Monitoring with sha256sum](#file-integrity-monitoring-with-sha256sum)
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

-   `grep`
-   `awk`

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

## File Integrity Monitoring with sha256sum

### Description

This project demonstrates basic file integrity monitoring using the `sha256sum` command-line tool. The goal was to detect unauthorized changes to critical system files by comparing file hashes.


