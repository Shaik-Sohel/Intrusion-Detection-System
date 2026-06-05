# SOC Analyst Home Lab using Wazuh, Suricata, Kali Linux and Windows

## Project Overview

This project demonstrates a Security Operations Center (SOC) home lab built using:

- Wazuh SIEM/XDR
- Suricata IDS
- Kali Linux
- Ubuntu Linux

The objective is to simulate real-world cyber attacks, collect logs, detect threats, and investigate security incidents.

---

## Architecture

Kali Linux acts as the attacker machine.

Ubuntu hosts:
- Suricata IDS
- Wazuh Agent

Wazuh Server:
- Centralized log collection
- Threat detection
- Alert management
- Dashboard visualization

---

## Components

### Wazuh

Functions:
- Log Management
- File Integrity Monitoring
- Security Monitoring
- Threat Detection
- Active Response

### Suricata

Functions:
- Network Intrusion Detection System (IDS)
- Traffic Inspection
- Signature-based Detection
- Alert Generation

---

## Lab Environment

### Kali Linux

Role:
- Attacker Machine

Tools:
- Nmap
- Hydra
- Netcat

### Ubuntu Server

Role:
- Network Monitoring

Installed:
- Suricata
- Wazuh Agent

---

## Attack Simulations

### 1. Network Reconnaissance

Tool:

```bash
nmap -sS <target-ip>
```

Detection:
- Suricata Alerts
- Wazuh Alerts

---

### 2. SSH Brute Force

Tool:

```bash
hydra -l testuser -P passwords.txt ssh://<target-ip>
```

Detection:
- Failed SSH Logins
- Authentication Alerts

---

### 4. File Integrity Monitoring

Linux:

```bash
touch test.txt
echo "SOC Test" >> test.txt
```

Windows:
- Create and modify files

Detection:
- Wazuh FIM Alerts

---


## MITRE ATT&CK Techniques

| Technique | Description |
|------------|------------|
| T1595 | Active Scanning |
| T1110 | Brute Force |
| T1059 | Command Execution |
| T1078 | Valid Accounts |
| T1046 | Network Service Discovery |

---

## Detection Workflow

1. Generate attack traffic from Kali Linux
2. Suricata analyzes network traffic
3. Wazuh collects logs
4. Wazuh generates alerts
5. Analyst investigates alerts
6. Incident response actions performed

---

## Skills Demonstrated

- Security Monitoring
- Threat Hunting
- Log Analysis
- IDS Management
- SIEM Administration
- Incident Investigation
- MITRE ATT&CK Mapping
- Network Security

---

## Screenshots

Add screenshots for:

- Wazuh Dashboard
- Suricata Alerts
- Agent Management
- Threat Hunting
- Nmap Detection
- FIM Alerts
- Authentication Failures

---

## Future Improvements

- Active Response
- Shuffle SOAR Integration
- Email Alerting
- Sigma Rules
- Threat Intelligence Feeds
- Malware Analysis Integration

---

## Author

Sohel Shaik

SOC Analyst Home Lab Project
