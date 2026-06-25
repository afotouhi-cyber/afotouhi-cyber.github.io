---
layout: page
title: Wazuh SIEM Lab
permalink: /projects/wazuh-siem-lab/
---

# Wazuh SIEM Lab

## Project Overview

I built a Wazuh SIEM homelab to centralize security monitoring for Windows and Linux endpoints. The project gave me hands on experience deploying a SIEM, configuring endpoint agents, working from the Linux command line, troubleshooting connectivity, and reviewing security telemetry from a centralized dashboard.

![Wazuh SIEM dashboard](/assets/images/SIEM.png)

![Wazuh agent overview](/assets/images/SIEM2.png)

## Lab Architecture

The Wazuh server runs on a repurposed gaming laptop. I wiped the laptop, installed Ubuntu Server, and used it as dedicated hardware for the Wazuh manager and dashboard.

After completing the initial server installation, I moved back to my primary PC and managed the Ubuntu Server remotely over SSH. This allowed me to complete configuration and troubleshooting from my main workstation while keeping the SIEM platform isolated on dedicated hardware.

### Components

* **Wazuh Server:** Ubuntu Server installed on a repurposed gaming laptop
* **Administration Workstation:** Primary Windows PC used for remote administration through SSH
* **Windows Endpoint:** Configured using the downloadable Wazuh agent installer and agent configuration settings
* **Linux Endpoint:** Configured through the command line using Wazuh installation and enrollment commands
* **Network:** Private homelab network used for agent-to-manager communication

## Deployment Process

### 1. Server Preparation

* Wiped and repurposed an older gaming laptop for dedicated SIEM use.
* Installed Ubuntu Server and completed initial network configuration.
* Installed Wazuh on Ubuntu Server.
* Verified access to the Wazuh dashboard from my primary PC.
* Enabled and used SSH for remote administration of the Ubuntu Server.

### 2. Windows Agent Deployment

For the Windows endpoint, I used the Wazuh agent installer and configured the agent to communicate with the Wazuh server. I verified that the agent appeared in the Wazuh dashboard and that the endpoint was sending telemetry.

### 3. Linux Agent Deployment

For the Linux endpoint, I installed and configured the Wazuh agent through the command line. This required using Linux terminal commands to install the agent, configure the manager address, start the service, and verify connectivity.

### 4. Validation and Monitoring

* Confirmed Windows and Linux agent enrollment in the Wazuh dashboard.
* Verified agent status and communication with the manager.
* Reviewed endpoint inventory, operating-system details, and agent health.
* Reviewed alert severity and event activity through the dashboard.
* Troubleshot agent connectivity and configuration issues during deployment.

## Skills Demonstrated

`Wazuh` · `SIEM` · `Ubuntu Server` · `Linux CLI` · `SSH` · `Windows Endpoint Administration` · `Endpoint Monitoring` · `Log Analysis` · `Virtualization` · `Troubleshooting`

## Key Takeaways

This project improved my understanding of how a SIEM is deployed and maintained outside of a managed enterprise environment. It also gave me practical experience using Ubuntu Server, SSH, Linux command-line administration, Windows agent deployment, endpoint enrollment, and centralized monitoring of multiple operating systems.

[Back to Projects](/projects/)
