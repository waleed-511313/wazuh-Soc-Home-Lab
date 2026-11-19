# wazuh-Soc-Home-Lab
# Wazuh SOC Home Lab Project

## 📌 Overview
This project demonstrates the setup of a Security Operations Center (SOC) home lab using **Wazuh** to monitor endpoints, detect threats, and analyze security events in real-time.

## 🛠️ Lab Environment
- **SIEM/Server:** Ubuntu Server 24.04 (Wazuh Manager & Dashboard) - IP: 192.168.100.90
- **Monitored Endpoint:** Windows (Wazuh Agent)
- **Network:** VirtualBox Bridged Adapter

## 🎯 Implemented Scenarios

### 1. SSH Brute Force Attack
- **Description:** Simulated multiple failed SSH login attempts from the Windows machine to the Ubuntu server.
- **Tool Used:** PowerShell (SSH client).
- **Detection:** Wazuh successfully detected the `Authentication failures` and flagged it under the MITRE ATT&CK framework as Brute Force.

### 2. File Integrity Monitoring (FIM)
- **Description:** Modified a sensitive system file (`/etc/passwd`) on the Ubuntu server to simulate unauthorized changes.
- **Tool Used:** Nano text editor.
- **Detection:** Wazuh detected the checksum change and generated an alert for `Integrity checksum changed`.

### 3. Port Scanning (Reconnaissance)
- **Description:** Scanned the Ubuntu server to discover open ports and running services.
- **Tool Used:** `nmap -sV`
- **Detection:** Wazuh captured the scan activity and logged events related to `nmap` and network reconnaissance.

## 📊 Results & Analysis
The Wazuh dashboard successfully visualized security alerts, correlating them with the MITRE ATT&CK framework. The total events reached **1,717**, with **19** authentication failures detected, proving the lab's effectiveness in capturing both network and host-based attacks.

## 📷 Visual Evidence
*(Screenshots will be uploaded here)*
