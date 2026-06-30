---
layout: page
title: Projects
permalink: /projects/
---

Hands-on cybersecurity projects focused on detection engineering, threat hunting, SIEM monitoring, vulnerability management, endpoint visibility, and security automation.

---

# ⭐ Featured Project

## Detection Engineering with Wazuh & MITRE ATT&CK

Designed, implemented, and validated custom Wazuh detection rules using Sysmon telemetry and Atomic Red Team attack simulations to improve visibility into attacker behavior.

### Project Overview

This project focuses on detection engineering rather than simply deploying a SIEM. After configuring Microsoft Sysmon on a Windows endpoint and forwarding telemetry into Wazuh, I simulated adversary techniques using Atomic Red Team, investigated the resulting telemetry, and developed custom detection logic mapped to the MITRE ATT&CK framework.

The first completed detection identifies PowerShell execution using the **-EncodedCommand** parameter, a commonly abused technique used to obfuscate malicious PowerShell commands.

---

## 1. Attack Simulation

To generate realistic telemetry, I executed an Atomic Red Team simulation for **MITRE ATT&CK T1059.001 (PowerShell)**. The test launched PowerShell using an encoded command, creating Sysmon process creation events that were forwarded into Wazuh for analysis.

![Atomic Red Team Simulation]({{ "/assets/images/AtomicRedTeam.png" | relative_url }})

---

## 2. Detection Development

After validating that Sysmon Event ID 1 process creation events were successfully being ingested by Wazuh, I created a custom local rule that extends Wazuh's built-in PowerShell detection.

The rule:

- Inherits from Wazuh's existing PowerShell rule
- Uses a unique Rule ID (**100100**)
- Raises the alert severity to **15**
- Maps the alert to **MITRE ATT&CK T1059.001**
- Generates a high-severity alert whenever an encoded PowerShell command is executed

![Custom Wazuh Rule]({{ "/assets/images/local_rules.png" | relative_url }})

---

## 3. Detection Validation

After deploying the rule, I executed the Atomic Red Team simulation again. Wazuh successfully generated my custom alert, confirming that the detection logic functioned as intended.

The resulting alert includes:

- Custom Rule ID **100100**
- Severity **15**
- MITRE ATT&CK mapping (**T1059.001**)
- PowerShell execution details
- Full Sysmon process telemetry

![Custom Detection Alert]({{ "/assets/images/EncodedPowerShell.png" | relative_url }})

---

### What I Built

- Installed and configured Microsoft Sysmon
- Integrated Sysmon telemetry into Wazuh
- Installed and executed Atomic Red Team attack simulations
- Investigated attack telemetry within Wazuh
- Authored custom Wazuh detection rules
- Validated detections against simulated attacker techniques
- Tuned alert severity and rule inheritance
- Mapped detections to the MITRE ATT&CK framework

### Skills Demonstrated

`Detection Engineering` · `Threat Hunting` · `Wazuh` · `Sysmon` · `Atomic Red Team` · `MITRE ATT&CK` · `PowerShell` · `Purple Teaming` · `Rule Development`

### Detection Library

| Detection | MITRE ATT&CK | Status |
|-----------|--------------|--------|
| Encoded PowerShell | T1059.001 | ✅ Completed |
| Certutil | T1105 | 🚧 Planned |
| MSHTA | T1218.005 | 🚧 Planned |
| Rundll32 | T1218.011 | 🚧 Planned |
| Regsvr32 | T1218.010 | 🚧 Planned |
| Windows Discovery Commands | TA0007 | 🚧 Planned |

---

## Wazuh SIEM Homelab

![Wazuh SIEM Dashboard]({{ "/assets/images/SIEM.png" | relative_url }})

Built a centralized Wazuh SIEM environment to monitor Windows and Linux endpoints from a dedicated Ubuntu Server.

### Project Overview

I repurposed an older gaming laptop into dedicated SIEM hardware by installing Ubuntu Server and deploying Wazuh Manager and the web dashboard. I then connected Windows and Linux endpoints, configured agents, and remotely administered the environment over SSH from my primary workstation.

### What I Built

- Repurposed a gaming laptop into dedicated SIEM hardware
- Installed Ubuntu Server
- Deployed Wazuh Manager and Dashboard
- Configured Windows endpoint monitoring
- Configured Linux endpoint monitoring
- Verified endpoint enrollment and log collection
- Enabled centralized security monitoring

### Skills Demonstrated

`Wazuh` · `SIEM` · `Ubuntu Server` · `Linux` · `SSH` · `Endpoint Monitoring` · `Log Analysis` · `System Administration`

[Read the full Wazuh SIEM Lab write-up](/projects/wazuh-siem-lab/)

---

## Python System Security Scan Report

![Python Security Report]({{ "/assets/images/VulnReport.png" | relative_url }})

![Python Security Report Details]({{ "/assets/images/Vuln2.png" | relative_url }})

Developed a Python-based security reporting tool that inventories a Windows system and generates an HTML report highlighting potential security concerns.

### Project Overview

The script gathers host information, inventories installed software, identifies outdated applications, enumerates listening ports, samples running processes, and produces an easy-to-read HTML security report. The goal is to provide a lightweight local assessment tool rather than replace enterprise vulnerability scanners.

### Capabilities

- System information collection
- Installed software inventory
- Available software update detection
- Open port enumeration
- Running process analysis
- HTML report generation
- Basic CVE reporting

### Skills Demonstrated

`Python` · `Security Automation` · `Windows Security` · `System Enumeration` · `Process Analysis` · `Port Enumeration` · `HTML Reporting`

### Source Code

[View Source Code on GitHub](https://github.com/afotouhi-cyber/Python-Vuln-scanner)

---

## Currently Expanding

I'm continuing to grow this portfolio through projects involving:

- LOLBin detection engineering
- Malware behavioral detection
- Windows Event Log analytics
- Threat hunting
- Incident response workflows
- Security automation with Python
- SOAR playbook development
- Cloud security monitoring