# Network Traffic Analysis of Ransomware Activity in the Healthcare Sector

<p align="center">
  <img src="https://img.shields.io/badge/Conference-SAC%202025-red?style=for-the-badge&logo=academia&logoColor=white" />
  <img src="https://img.shields.io/badge/Tool-Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white" />
  <img src="https://img.shields.io/badge/Framework-MITRE%20ATT%26CK-E22C2C?style=for-the-badge&logo=target&logoColor=white" />
  <img src="https://img.shields.io/badge/Domain-Healthcare%20Security-green?style=for-the-badge&logo=health&logoColor=white" />
</p>

> **Presented at the 28th Student Academic Conference (SAC 2025)**  
> Minnesota State University Moorhead

---

## Overview

This research project investigates ransomware-related network activity in a **healthcare environment** through deep packet capture analysis using **Wireshark** and adversary behavior mapping using the **MITRE ATT&CK framework**.

Healthcare networks face unique ransomware risks due to critical patient data and operational dependencies. This study demonstrates how network traffic analysis can serve as an early warning system for ransomware intrusions by identifying Indicators of Compromise (IoCs) before significant damage occurs.

---

## Authors

| Name | Institution |
|------|------------|
| Hashan Kodippilige | Minnesota State University Moorhead |
| Dr. A. Nwaigwe | Minnesota State University Moorhead |

---

## Research Objectives

- Capture and analyze ransomware-related network traffic in a healthcare simulation
- Identify Indicators of Compromise (IoCs) from PCAP data
- Map observed adversary behaviors to MITRE ATT&CK tactics and techniques
- Demonstrate how Blue Team analysts can use traffic analysis for proactive threat detection

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Wireshark | Packet capture and traffic analysis |
| MITRE ATT&CK Framework | Adversary behavior mapping |
| PCAP Analysis | Network traffic examination |
| TCP Stream Analysis | Session reconstruction |
| FTP / HTTPS Protocol Analysis | C2 and exfiltration detection |

---

## Key Findings

### 1. Credential Exposure (Cleartext FTP)
FTP credentials were transmitted in plaintext — a critical security failure in a healthcare network:
```
USER: jane
PASS: pwd2345
```
**MITRE Technique:** T1078 — Valid Accounts | T1552.001 — Credentials in Files

---

### 2. Command & Control (C2) Activity
Observed suspicious HTTPS communication with an external IP address:
```
External C2 IP: 20.59.87.225
```
**MITRE Technique:** T1071.001 — Application Layer Protocol: Web Protocols

---

### 3. File Exfiltration
FTP `STOR` commands confirmed unauthorized file uploads indicating active data exfiltration:

**MITRE Technique:** T1048.003 — Exfiltration Over Alternative Protocol

---

### 4. Lateral Movement
Internal host communications indicated adversary movement between machines:
```
10.0.2.4 ↔ 10.0.2.15
```
**MITRE Technique:** T1021 — Remote Services

---

## MITRE ATT&CK Mapping

| Tactic | Technique ID | Technique Name | Observed Evidence |
|--------|-------------|----------------|-------------------|
| Initial Access | T1566 | Phishing | Inferred from traffic patterns |
| Credential Access | T1552.001 | Cleartext Credentials | FTP USER/PASS in plaintext |
| Command & Control | T1071.001 | Web Protocols (HTTPS) | Traffic to 20.59.87.225 |
| Lateral Movement | T1021 | Remote Services | Internal host hopping |
| Exfiltration | T1048.003 | Exfiltration via FTP | FTP STOR commands observed |

---

## Repository Contents

```
Ransomware-network-traffic-analysis-using-mitre-attack-Wireshark
├── 📄 README.md                              ← You are here
├── 📋 Abstract_Hashan Kodippilige_SAC.pdf    ← SAC 2025 Conference Abstract
└── 📊 Network Traffic Analysis_Hashan.pdf    ← Full Analysis Report
```

---

## Key Takeaways for Blue Team Analysts

1. **Monitor FTP traffic** — cleartext protocols should never be used in healthcare networks
2. **Baseline internal traffic** — lateral movement becomes visible when normal patterns are known
3. **Block unauthorized external IPs** — C2 communication can be disrupted at the perimeter
4. **Use MITRE ATT&CK actively** — mapping IoCs to techniques accelerates incident response

---

## Why Healthcare?

Healthcare organizations are among the most targeted ransomware victims due to:
- Critical patient data with high ransom value
- Operational pressure to restore services quickly
- Often-outdated network infrastructure
- Strict regulatory compliance requirements (HIPAA)

This study contributes to the growing body of research on sector-specific ransomware defense strategies.

---

## Conference

**28th Student Academic Conference (SAC 2025)**  
Minnesota State University Moorhead — Spring 2025

---

## Disclaimer

All traffic analysis was performed on authorized lab environments and public PCAP datasets for academic and cybersecurity research purposes only. No real patient data was used or accessed.

---

## Author

**Hashan Kodippilige**  
M.S. Cybersecurity — Minnesota State University Moorhead  
📧 hashansharindu@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/hashankodippilige/)  
🐙 [GitHub](https://github.com/hashan-kodippilige)
