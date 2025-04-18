# Security Projects

## Introduction

Welcome to my portfolio! I'm an Aspiring Cybersecurity Analyst passionate about Threat Hunting, OSINT, Phishing Analysis, and Strengthening IT Security. This portfolio showcases my practical skills and projects related to security operations.

## Projects

-   [Basic Log Analysis with grep](#basic-log-analysis-with-grep)
-   [File Integrity Monitoring with sha256sum](#file-integrity-monitoring-with-sha256sum)
-   [Basic Network Scanning with nmap](#basic-network-scanning-with-nmap)
-   [Vulnerability Scanning and Remediation with Nessus Essentials](#vulnerability-scanning-and-remediation-with-nessus-essentials)
-   [Home Network Security Assessment and Hardening](#home-network-security-assessment-and-hardening)
-   [Educational Phishing Simulation](#educational-phishing-simulation)
-   [Wireshark Traffic Analysis Lab](#wireshark-traffic-analysis-lab)
  
## Tools and Technologies

-   Splunk
-   Wireshark
-   Kali Linux
-   Nessus
-   CyberPhish
-   Nmap
-   Python

## Certifications and Training

-   `Blue Team Level 1 (BTL1)` `Certified Network Security Practitioner (CNSP)` `CompTIA Security+`
-   `Google Cybersecurity Specialization Course`

## Contact

-   LinkedIn Profile - http://www.linkedin.com/in/cristopher-de-guzman-17a241268

---

## Basic Log Analysis with `grep`

### Description

This project involved analyzing a sample web server access log to identify common HTTP status codes and IP addresses using `grep` and `awk`. The goal was to demonstrate basic log analysis skills.

### Tools Used

-   `grep`
-   `awk`

### Key Findings

-   The log file contained [216] 404 error code.
-   The amount of unique IP addresses that accessed the server is
    [1753].
-   The log file contained [9152] 200 OK status code.

### Example Commands

```bash
grep "404" access.log | wc -l
awk '{print $1}' access.log | sort -u | wc -l
grep "200" access.log | wc -l
```

---

## File Integrity Monitoring with `sha256sum`

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
nmap -v -sS scanme.nmap.org
```

## Vulnerability Scanning and Remediation with Nessus Essentials

### Description

Conducted comprehensive vulnerability scans of a virtual network using Nessus Essentials to identify critical security vulnerabilities. Developed a detailed vulnerability report and implemented remediation steps to mitigate identified risks. This project demonstrates my ability to perform vulnerability assessments and improve the security posture of systems.

### Tools Used

-   Nessus Essentials
-   VirtualBox

### Key Findings

-   Identified critical vulnerabilities, such as outdated software and missing security patches.
-   Developed a vulnerability report with detailed descriptions and remediation steps.
-   Successfully remediated identified vulnerabilities and verified the results with re-scans.

### Remediation Process

The remediation process involved patching operating systems, updating vulnerable software, and hardening system configurations. Re-scans were performed to verify that the vulnerabilities were successfully remediated.


## Home Network Security Assessment and Hardening

### Description

Conducted a comprehensive security assessment on my home network to identify potential vulnerabilities and implemented hardening measures to improve its security posture. This project demonstrates my ability to analyze network security, identify risks, and apply practical security configurations.

### Tools Used

-   nmap
-   Linux
-   VirtualBox

### Key Findings

-   No default passwords were identified.
-   Discovered open and unused ports on IoT devices.
-   No vulnerabilites were found.

### Hardening Measures Implemented

-   Closed unnecessary open ports on IoT devices.
-   Ensured all OS and applications were up to date.

### Example Commands

```bash
nmap -v -sV -O <ip_addr>
nmap --script vuln <ip_addr>
```

# Educational Phishing Simulation

## Description

This project is an enhanced educational phishing simulation designed to demonstrate the mechanics of phishing attacks and promote awareness of cybersecurity best practices. It builds upon the CyberPhish concept, incorporating modular code, dynamic templating, and a local web server to improve the simulation's realism and effectiveness.

**Disclaimer:** This project is intended for educational and ethical testing purposes only. Do not use this tool for any illegal or malicious activities.

## Features

* **Modular Code:** Organized into separate Python modules for better maintainability and scalability.
* **Jinja2 Templating:** Uses Jinja2 for dynamic email template generation, allowing for personalized phishing scenarios.
* **Local Web Server (Python `http.server`):** Hosts the "phished" confirmation page, enabling realistic simulation of external phishing links.
* **ngrok Integration:** Exposes the local web server to the internet, providing a public URL for the phishing link.
* **Mailtrap Integration:** Uses Mailtrap for safe email testing and simulation.
* **Command-Line Arguments:** Allows specifying the recipient email address when running the script.
* **Configuration File (`config.json`):** Stores Mailtrap credentials and other configurable parameters.
* **HTML Email Rendering:** Correctly formats the email as HTML, ensuring it is displayed as intended in email clients.
* **Enhanced Error Handling:** Implements robust error handling to catch exceptions and provide informative error messages.
* **Realistic Phishing Scenarios:** Provides a foundation for creating more complex and tailored phishing simulations.
* **Clear Educational Content:** The "phished" confirmation page provides details about phishing attacks and preventative measures.

## Getting Started

### Prerequisites

* Python 3.x installed on your system.
* Git installed on your system.
* Mailtrap account (for email testing).
* ngrok (to expose the local web server).
* Jinja2 library (install with `pip install Jinja2`).

### Installation

1.  Install CyberPhish:

    ```bash
    pip install colorama
    git clone https://lnkd.in/dcHU8ivq
    cd CyberPhish
    pip install -r requirements.txt
    python3 CyberPhish.py
    ```

2.  Install the required Python library:

    ```bash
    pip install Jinja2
    ```

3.  Configure `config.json`:
    * Open `config.json` and replace the placeholders with your Mailtrap credentials and the ngrok URL.
    * Start the local web server: `python -m http.server 8000`
    * Start ngrok: `ngrok http 8000`
    * Copy the ngrok forwarding URL, and add `/phished.html` to the end.
    * Update the `phished_url` value in your `config.json` file.

### Usage

1.  Run the `main.py` script, providing the recipient email address as a command-line argument:

    ```bash
    python main.py recipient@example.com
    ```

2.  Check your Mailtrap inbox to view the simulated phishing email.
3.  Click the link in the email to see the "phished" confirmation page.

## Configuration (`config.json`)

```json
{
  "mailtrap_username": "YOUR_MAILTRAP_USERNAME",
  "mailtrap_password": "YOUR_MAILTRAP_PASSWORD",
  "mailtrap_smtp_server": "smtp.mailtrap.io",
  "mailtrap_smtp_port": 2525,
  "sender_email": "phishing@example.com",
  "phished_url": "YOUR_NGROK_URL/phished.html"
}
```

# Wireshark Traffic Analysis Lab

**A hands-on project demonstrating basic network traffic analysis using Wireshark and Zeek, mimicking a Tier 1 SOC Analyst workflow.**

## Objective

Capture live network traffic from your computer, log that data using Zeek, and analyze it to understand network connections and DNS queries.

## Tools Used

* **Wireshark:** For capturing network packets.
* **Zeek:** For parsing raw packet captures into structured logs.
* **Terminal:** For executing commands and exploring the generated logs.

### Step 1: Capturing Traffic with Wireshark

1.  **Run Wireshark** 
2.  **Select my Wi-Fi interface (en0)** as the network interface to monitor.
3.  **Start the capture** and then spent about 30-60 seconds browsing various websites to generate some network activity.
4.  **Stop the capture** once I had gathered enough traffic.
5.  **To focus on relevant data, I applied the filter `http || dns`** in Wireshark. This helped to clean up the view and concentrate on web and DNS-related packets.
6.  **Finally, I saved the captured data as `test_capture.pcapng` on my Desktop.**

### Step 2: Parse with Zeek

1.  **Open Terminal:** 
2.  **Create and move into a Zeek logs folder:** Execute the following command to create a directory for Zeek logs and navigate into it:
    ```bash
    mkdir ~/zeek_logs && cd ~/zeek_logs
    ```
3.  **Run Zeek on your capture file:** Use the following command to process the Wireshark capture file with Zeek:
    ```bash
    zeek -r ~/Desktop/test_capture.pcapng
    ```
    * **Note:** Ensure that Zeek is installed on your system. If not, you may need to install it using your preferred package manager.
4.  **View the logs created:** List the files in the `~/zeek_logs` directory using the `ls` command. You should see several log files, including:
    * `conn.log`: Contains information about network connections.
    * `dns.log`: Contains details about DNS queries and responses.
    * `http.log`: Contains information about HTTP traffic.

### Step 3: Analyze the Logs

1.  **Explore `conn.log`:**
    * Use the following command to view the contents of the connection log, allowing you to scroll through it:
        ```bash
        cat conn.log | less
        ```
    * Inside `conn.log`, you can observe key details about network connections, such as:
        * Source and destination IP addresses (`id.orig_h`, `id.resp_h`)
        * Source and destination port numbers (`id.orig_p`, `id.resp_p`)
        * The network protocol used (`proto`)
        * The duration of the connection (`duration`)

2.  **Explore `dns.log`:**
    * Use the following command to view the contents of the DNS log:
        ```bash
        cat dns.log | less
        ```
    * Inside `dns.log`, you can find information about DNS queries, including:
        * The timestamp of the query (`ts`)
        * The domain name queried (`query`)
        * The type of DNS query (e.g., A, AAAA) (`qtype_name`)
        * The resolved IP address (if successful) (`answers`)

## What I Learned and Future Steps

Through this exercise, I gained a basic understanding of how Wireshark can capture network traffic and how Zeek can transform that raw data into structured logs for analysis. I was able to identify the source and destination of network connections and see the DNS queries my system made while browsing.
