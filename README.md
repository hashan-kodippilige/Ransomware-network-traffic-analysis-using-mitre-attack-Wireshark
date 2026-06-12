# Network Traffic Analysis of Ransomware Activity in the Healthcare Sector Using Wireshark and MITRE ATT&CK

## Conference Presentation

🎤 Presented at the 28th Student Academic Conference (SAC 2025)
Minnesota State University Moorhead

## Authors

- Hashan Kodippilige
- A. Nwaigwe

## Overview

This project investigates ransomware-related network activity in a healthcare environment through packet capture analysis using Wireshark and adversary behavior mapping using the MITRE ATT&CK framework.

The analysis focused on identifying Indicators of Compromise (IoCs), credential exposure, command-and-control communications, file exfiltration, and lateral movement behavior.

## Research Objectives

- Analyze ransomware-related network traffic
- Identify Indicators of Compromise (IoCs)
- Map observed activity to MITRE ATT&CK tactics and techniques
- Demonstrate how network traffic analysis can support threat detection

## Tools Used

- Wireshark
- MITRE ATT&CK Framework
- PCAP Analysis
- TCP Stream Analysis

## Key Findings

### Credential Exposure

FTP credentials were transmitted in cleartext:

USER: jane
PASS: pwd2345

### Command and Control Activity

Observed HTTPS communication with external IP:

20.59.87.225

### File Exfiltration

FTP STOR commands confirmed file uploads and potential data exfiltration.

### Lateral Movement

Internal communications indicated movement between hosts:

10.0.2.4 ↔ 10.0.2.15

## MITRE ATT&CK Mapping

- Initial Access
- Credential Access
- Command and Control
- Lateral Movement
- Exfiltration

## Skills Demonstrated

- Network Traffic Analysis
- Threat Hunting
- Cyber Threat Intelligence
- MITRE ATT&CK Mapping
- Incident Investigation
- Wireshark Analysis

## Conference

Presented at:

28th Student Academic Conference (SAC 2025)
Minnesota State University Moorhead

## Files

- SAC Abstract
- Presentation Slides
- Supporting Analysis Material

## Author

Hashan Kodippilige
Master of Science in Cybersecurity
Minnesota State University Moorhead
