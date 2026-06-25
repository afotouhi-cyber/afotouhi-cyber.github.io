---
layout: page
title: Projects
permalink: /projects/
---

# Projects

Hands-on cybersecurity projects focused on security monitoring, endpoint visibility, Linux administration, vulnerability awareness, and practical automation.

---

## Wazuh SIEM Homelab

![Wazuh SIEM dashboard]({{ "/assets/images/SIEM.png" | relative_url }})

Built a centralized Wazuh SIEM environment to monitor Windows and Linux endpoints from a dedicated Ubuntu Server.

### Project Overview

I repurposed an older gaming laptop as dedicated SIEM hardware by wiping it and installing Ubuntu Server. After installing Wazuh, I used SSH from my primary Windows PC to administer and troubleshoot the server remotely.

The lab includes both Windows and Linux endpoints. The Windows agent was deployed using the downloadable Wazuh installer and configuration interface, while the Linux agent was installed and configured through the command line.

### What I Built

- Repurposed and configured a gaming laptop as dedicated Wazuh server hardware.
- Installed Ubuntu Server and deployed the Wazuh manager and dashboard.
- Used SSH for remote Linux administration from a primary Windows workstation.
- Installed and configured a Windows Wazuh agent using the downloadable installer.
- Installed and configured a Linux Wazuh agent through the Linux CLI.
- Validated agent enrollment, endpoint visibility, dashboard connectivity, and security-event data.

### Skills Demonstrated

`Wazuh` · `SIEM` · `Ubuntu Server` · `Linux CLI` · `SSH` · `Windows Administration` · `Endpoint Monitoring` · `Log Analysis` · `Troubleshooting`

[Read the full Wazuh SIEM Lab write-up](/projects/wazuh-siem-lab/)

---

## Python System Security Scan Report

![Python system security scan report]({{ "/assets/images/VulnReport.png" | relative_url }})

![Python scan report: exposed ports and running processes]({{ "/assets/images/Vuln2.png" | relative_url }})

Built a Python-based system security reporting tool that gathers local Windows system information and produces an HTML report to help identify areas that may need review.

### Project Overview

The script collects basic host information, reviews installed applications for available updates, identifies listening ports, samples running processes, and formats the results into a readable HTML report. The report is intended as a local security-awareness and triage aid, not a replacement for enterprise vulnerability management or a full vulnerability scanner.

### What It Reviews

- Operating system, architecture, hostname, CPU, memory, and disk information
- Installed application versions and available updates when detected
- Listening ports and services that may warrant review
- Running process samples
- Basic CVE-summary output when available

### Skills Demonstrated

`Python` · `Security Automation` · `Windows Security` · `System Enumeration` · `Port Review` · `Process Analysis` · `HTML Reporting` · `Vulnerability Awareness`

### Security Considerations

Sensitive information, including IP addresses, has been redacted from the published screenshots. The tool is designed for systems I own or am authorized to assess.

### Source Code

[View the Python System Security Scan Report source code on GitHub](https://github.com/afotouhi-cyber/Python-Vuln-scanner)

---

## Current Learning Focus

I am continuing to expand this portfolio with projects involving vulnerability management, detection engineering, alert triage, threat hunting, and Python automation.
