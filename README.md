# wireshark-network-analysis
## 📌 Project Overview
This project demonstrates basic network traffic analysis using Wireshark, focusing on DNS resolution and ICMP communication. 

## Objective
Analyze DNS and ICMP traffic using Wireshark to understand network communication.

## Tools Used
- Wireshark
- Kali Linux
- Ping utility

## Process
- Captured live network traffic
- Generated traffic using `ping google.com`
- Filtered packets using:
  - dns
  - icmp

## Observations
- DNS queries were generated for google.com
- ICMP echo request and reply packets were observed
- Confirmed active network communication

## Key Learnings
- DNS resolves domain names to IP addresses
- ICMP is used for connectivity testing
- Packet analysis helps understand network behavior

- ## Skills Demonstrated
- Network traffic analysis
- Packet filtering (DNS, ICMP)
- Basic troubleshooting of network issues
- Understanding client-server communication

## SOC Relevance
This helps in understanding real-time network monitoring and basic incident analysis.

## Author
Tarun Kumar Domakonda
---
## 🛡️ Project 2: Port Scan Detection

## 📌 Project Overview
This project simulates a network reconnaissance attack using Nmap and analyzes the traffic using Wireshark to detect port scanning behavior.

---

## 🎯 Objective
To understand how port scanning works and how SOC analysts detect suspicious scanning activity in network traffic.

---

## 🛠️ Tools Used
- Wireshark
- Nmap
- Kali Linux

---

## ⚙️ Methodology

### 1. Target Selection
A safe test target was used:
- scanme.nmap.org

### 2. Port Scanning
Performed SYN stealth scan:
```bash
nmap -sS scanme.nmap.org
```

## 🔍 Observations :

Multiple ports were scanned in sequence
Open ports detected:
22/tcp (SSH)
80/tcp (HTTP)
Filtered port detected:
25/tcp (SMTP)
SYN packets observed in Wireshark during scan

## 📊 Wireshark Analysis

Filters used:

tcp.flags.syn == 1

## Findings:

Multiple SYN packets sent to different ports
No full TCP handshake for most ports
Clear pattern of reconnaissance activity

## 🧠 Skills Demonstrated

- Network reconnaissance analysis
- Packet capture and inspection using Wireshark
- TCP/IP protocol understanding
- Identification of SYN scanning behavior
- Basic threat detection techniques
- Command-line usage of Nmap for security testing
- Network traffic filtering and analysis (TCP flags)

## 🚨 SOC Relevance

This project simulates real-world SOC (Security Operations Center) activity where analysts monitor and detect early-stage attacker behavior.

## Key SOC use cases demonstrated:

- Detection of port scanning (reconnaissance phase of attack lifecycle)
- Identification of abnormal SYN packet patterns
- Analysis of exposed services (SSH, HTTP)
- Understanding attacker mapping techniques before exploitation

## In real SOC environments, this type of activity is flagged as:

- Suspicious scanning behavior
- Potential intrusion reconnaissance
- Pre-attack network probing

## Early detection of such activity helps prevent further exploitation attempts.

Author :
Tarun Kumar Domakonda
