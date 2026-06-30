---
layout: page
title: Projects
permalink: /projects/
---

Hands-on cybersecurity projects focused on detection engineering, threat hunting, SIEM monitoring, vulnerability management, endpoint visibility, and security automation.

---

# ⭐ Featured Project

## Detection Engineering with Wazuh & MITRE ATT&CK

![Detection Engineering]({{ "/assets/images/EncodedPowerShell.png" | relative_url }})

Designed and validated custom Wazuh detection rules using Sysmon telemetry and Atomic Red Team attack simulations to improve visibility into attacker behavior.

### Project Overview

This project focuses on detection engineering rather than simply deploying a SIEM. After configuring Sysmon on Windows and forwarding telemetry into Wazuh, I simulated adversary techniques using Atomic Red Team, investigated the generated events, and developed custom detection logic mapped to the MITRE ATT&CK framework.

The first completed detection identifies PowerShell execution using the **-EncodedCommand** parameter, a common technique used by attackers to obfuscate malicious scripts.

### What I Built

- Installed and configured Microsoft Sysmon
- Integrated Sysmon telemetry into Wazuh
- Installed and executed Atomic Red Team simulations
- Investigated attack telemetry in Wazuh
- Created custom Wazuh detection rules
- Validated custom detections against live attack simulations
- Mapped detections to MITRE ATT&CK

### Skills Demonstrated

`Detection Engineering` · `Threat Hunting` · `Wazuh` · `Sysmon` · `Atomic Red Team` · `MITRE ATT&CK` · `PowerShell` · `Purple Teaming` · `Incident Detection`

**Current Detection Coverage**

✅ PowerShell EncodedCommand (MITRE T1059.001)

🚧 Additional detections currently in development:

- Certutil
- MSHTA
- Rundll32
- Regsvr32
- Discovery Commands
- LOLBins

---

## Wazuh SIEM Homelab

![Wazuh SIEM dashboard]({{ "/assets/images/SIEM.png" | relative_url }})

Built a centralized Wazuh SIEM environment to monitor Windows and Linux endpoints from a dedicated Ubuntu Server.

### Project Overview

I repurposed an older gaming laptop into dedicated SIEM hardware running Ubuntu Server. After deploying Wazuh, I configured both Windows and Linux endpoints and remotely administered the server over SSH from my primary workstation.

### What I Built

- Repurposed laptop as SIEM hardware
- Installed Ubuntu Server
- Deployed Wazuh Manager & Dashboard
- Configured Windows agent
- Configured Linux agent
- Validated endpoint enrollment and event collection

### Skills Demonstrated

`Wazuh` · `SIEM` · `Ubuntu Server` · `Linux` · `SSH` · `Endpoint Monitoring` · `Log Analysis`

[Read the full Wazuh SIEM Lab write-up](/projects/wazuh-siem-lab/)

---

## Python System Security Scan Report

![Python security scan report]({{ "/assets/images/VulnReport.png" | relative_url }})

![Python scan report]({{ "/assets/images/Vuln2.png" | relative_url }})

Built a Python-based security reporting tool that inventories a Windows system and generates an HTML report highlighting potential security concerns.

### Features

- System information collection
- Installed software inventory
- Available software updates
- Open port enumeration
- Running process analysis
- HTML report generation
- Basic CVE reporting

### Skills Demonstrated

`Python` · `Automation` · `Windows Security` · `System Enumeration` · `HTML Reporting`

### Source Code

https://github.com/afotouhi-cyber/Python-Vuln-scanner

---

## Current Learning

I am actively expanding this portfolio with projects focused on:

- Detection Engineering
- Threat Hunting
- Purple Teaming
- Malware Analysis
- Incident Response
- Security Automation
- SOAR Development
- Cloud Security
