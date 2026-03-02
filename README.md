### SSH Incident Response Simulation
## Project Overview

This project simulates a brute-force SSH authentication attack and demonstrates a structured incident response workflow.
The lab covers detection, investigation, evidence collection, and containment actions using system logs and firewall rules.
The objective was to replicate real-world Security Operations Center (SOC) incident handling procedures.

## Lab Environment

Operating System: Kali Linux (Virtual Machine)
Service Analyzed: OpenSSH (sshd)
Log Source: systemd journal

Tools Used:

journalctl
grep
wc
iptables

## Incident Scenario

Multiple failed SSH login attempts were detected targeting a non-existent user account. The repeated authentication failures simulated brute-force attack behavior.

## Incident Response Phases
1️ Detection

Repeated “Failed password” entries were identified in SSH logs.

2 Investigation

Total failed attempts identified
Source IP address extracted
Targeted username identified
Timeline of activity reviewed

3 Containment

A firewall rule was added using iptables to block the source IP address.

## Key Findings

32 failed SSH login attempts detected
Source IP: 127.0.0.1 (lab simulation)
Targeted user: fakeuser
No successful login occurred

## Security Recommendations

Implement Fail2Ban
Use SSH key-based authentication
Disable password authentication
Enable automated alerting for failed login thresholds

## Skills Demonstrated

Incident detection
Log investigation
Timeline reconstruction
Threat pattern recognition
Firewall-based containment
Structured incident reporting

## Repository Structure

SSH-Incident-Response-Simulation/
│
├── README.md
├── screenshots/
│ ├── failed_attempts.png
│ ├── log_analysis.png
│ ├── failed_count.png
│ ├── ip_extraction.png
│ └── firewall_rule.png
├── report/
│ └── SSH_Incident_Response_Report.pdf
└── logs/
└── failed_attempts.txt
