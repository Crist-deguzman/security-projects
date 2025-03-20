# security-projects

## Introduction

Welcome to my portfolio! I'm an Aspiring Cybersecurity Analyst passionate about Threat Hunting, OSINT, Phishing Analysis, and Strengthing IT Security. This portfolio showcases my practical skills and projects related to security operations.

## Projects

-   [Basic Log Analysis with grep](#basic-log-analysis-with-grep)
-   [File Integrity Monitoring with sha256sum](#file-integrity-monitoring-with-sha256sum)
-   [Basic Network Scanning with nmap](#basic-network-scanning-with-nmap)

## Tools and Technologies

-   Splunk
-   Wireshark
-   Kali Linux
-   Snort/Suricata
-   Python
-   Bash/PowerShell
-   Linux/Windows administration

## Certifications and Training

-   `Blue Team Level 1 (BTL1)` `Certified Network Security Practitioner (CNSP)` `CompTIA Security+`
-   `Google Cybersecurity Specialization Course`

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

### Tools Used

-   `sha256sum`
-   `diff`

### Key Findings

-   The `diff` command identified that `files/file1.txt` had been modified.
-   The hash for `files/file1.txt` in `current_hashes.txt` was different from the hash in `initial_hashes.txt`.
-   This project demonstrates how file integrity monitoring can be used to detect unauthorized changes to files.

### Example Commands

```bash
sha256sum files/* > initial_hashes.txt
echo "Modified content" >> files/file1.txt
sha256sum files/* > current_hashes.txt
diff initial_hashes.txt current_hashes.txt
```

## Basic Network Scanning with `nmap`

### Description

This project demonstrates basic network scanning using the `nmap` command-line tool. The goal was to identify open ports and services running on a target system.

### Tools Used

-   `nmap`

### Key Findings

-   The `nmap` scan identified the following open ports:
    -   Port 22 (SSH)
    -   Port 80 (HTTP)
    -   Port 9929 (NPING-ECHO)
    -   Port 31337 (ELITE)
-   This project demonstrates how `nmap` can be used to identify open ports and services, which is a crucial step in network security assessments.

### Example Commands

```bash
nmap -v -sS <target_IP_address>
```
