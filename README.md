# 🧠 Active Directory Home Lab – Windows Server, Sysmon, Splunk & Red Team Simulation

This is a **self-hosted lab project** where I built a Windows-based domain environment with **Active Directory**, **Splunk**, and **attack simulation tools** to better understand enterprise network security. The lab simulates a real-world IT infrastructure with domain services, endpoint telemetry, and SIEM analysis.

It culminates with a **brute-force attack from Kali Linux** and telemetry inspection via Splunk, offering both red team and blue team perspectives.

---

## 📌 Table of Contents

- [Goals](#goals)
- [Architecture Overview](#architecture-overview)
- [Core Technologies](#core-technologies)
- [Key Features](#key-features)
- [Lab Breakdown](#lab-breakdown)
- [Security & Monitoring](#security--monitoring)
- [Future Enhancements](#future-enhancements)
- [Screenshots](#screenshots)

---

## 🎯 Goals

- Build a virtualized Active Directory domain environment.
- Simulate enterprise infrastructure for security learning.
- Collect and analyze endpoint logs using Splunk.
- Practice red team techniques with Kali Linux and Atomic Red Team.
- Strengthen detection and monitoring skills for SOC workflows.

---

## 🌐 Architecture Overview

![active-directory-schema](https://github.com/user-attachments/assets/e6462b6d-8240-43b5-9f1e-0429f76162e3)

---

## 🧰 Core Technologies

| Category             | Tools / Services                        |
|----------------------|-----------------------------------------|
| Virtualization       | VirtualBox                              |
| Domain Services      | Windows Server 2022 + Active Directory  |
| Endpoint             | Windows 10                              |
| Logging & SIEM       | Sysmon, Splunk, Splunk Universal Forwarder |
| Red Team             | Kali Linux, Crowbar, Atomic Red Team    |
| Attack Simulation    | MITRE ATT&CK techniques                 |

---

## 🚀 Key Features

- **Windows Server AD domain setup** with DNS & DHCP.
- **Sysmon and Splunk Forwarder** deployed for endpoint logging.
- **Log collection & analysis** via Splunk Web interface.
- **Brute-force RDP attack** executed from Kali Linux.
- **Simulated adversary behavior** using Atomic Red Team.
- **Detection validation** with MITRE ATT&CK mapping.
- **Real-time telemetry** from security, system, and application logs.

---

## 🛠️ Lab Breakdown

### 🖥️ VM Setup
- **AD-Win-Serv-2022** – Domain Controller, DNS, and ADDS.
- **AD-Win-10** – Windows 10 client, domain-joined.
- **AD-Splunk** – Ubuntu-based Splunk server.
- **AD-Kali-Linux** – Kali Linux attacker VM.

### 🧾 Domain Configuration
- Promoted Windows Server to a domain controller.
- Created two users: `JSmith` (IT) and `TSmith` (HR).
- Configured Organizational Units for user management.
- Joined the Windows 10 client to the domain using `JSmith`.

### 📡 Networking
- NAT network created in VirtualBox for inter-VM connectivity.
- Static IPs assigned based on a pre-built topology diagram.

---

## 🛡️ Security & Monitoring

- **Sysmon**: Installed with Olaf’s advanced configuration for granular telemetry.
- **Splunk Forwarder**: Deployed on endpoints, logs forwarded to central server.
- **Log Sources**: Security, Application, System, Sysmon events.
- **Custom Index (`endpoint`)**: Centralized log collection and queries.
- **Detection**: Verified Event IDs for failed/successful logins, new account creation, PowerShell execution.
- **Atomic Red Team**: Simulated MITRE T1136 (Create Account), T1059 (PowerShell), and verified detection in Splunk.

---

## 🔐 Red Team Simulation

### 💥 Brute Force Attack
- **Tool**: Crowbar on Kali Linux
- **Target**: RDP login for `TSmith`
- **Method**: RockYou wordlist with modified password injection
- **Detection**: Event ID 4625 (failed logins), followed by 4624 (successful login)

### 🎯 Atomic Red Team
- Tested techniques like:
  - **T1136.001** – Local account creation
  - **T1059.001** – PowerShell scripting
- Verified gaps in detection and updated telemetry pipeline accordingly.

---

## 🔄 Future Enhancements

- Integrate Sigma rules for alerting.
- Configure Splunk dashboards for real-time analysis.
- Add endpoint detection tools (e.g., Velociraptor, Wazuh).
- Enable PowerShell logging and WinRM for remote management.
- Explore Windows Event Forwarding for log centralization.

---

## 🖼️ Screenshots

> _Coming soon: Splunk dashboards, event log views, attack telemetry samples._
