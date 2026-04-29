# 🖥️ Enterprise Infrastructure Simulation — TechMaroc SARL

A fully simulated enterprise IT environment designed to demonstrate real-world IT Support, System Administration, Networking, and ITSM capabilities aligned with Canadian job market requirements (Help Desk / NOC / IT Infrastructure roles).

---

# 🎯 Project Objective

This lab replicates a small-to-medium enterprise IT environment to demonstrate hands-on skills in:

- IT Support (Level 1 / Level 2)
- Active Directory administration
- Network troubleshooting & infrastructure support (pfSense)
- IT Service Management (ITSM)
- System monitoring & incident response (Zabbix, GLPI)
- Microsoft 365 / Azure AD (conceptual hybrid environment)

👉 The goal is to simulate real corporate IT operations, not just a technical lab.

---

# 🏢 Business Simulation Context

This environment simulates a real company IT infrastructure where employees depend on:

- Secure network access
- Centralized identity management
- Reliable IT services (DNS, DHCP, authentication)
- Ticket-based IT support system
- Continuous monitoring and incident response

---

# 🏗️ Architecture Overview

| Machine   | Role                                     | IP Address            |
|------------|----------------------------------------|----------------------|
| pfSense    | Firewall / Router / DHCP               | 192.168.10.1         |
| DC-01      | Active Directory / DNS / GPO           | 192.168.10.2         |
| SRV-LINUX  | GLPI (ITSM) + Zabbix Monitoring        | 192.168.10.20        |
| PC-01      | Windows 10/11 Workstation (Domain Join)| DHCP (192.168.10.100+) |
| PC-02      | Windows 10/11 Workstation (Domain Join)| DHCP (192.168.10.100+) |

---

# 🛠️ Technologies & Tools

## Core Infrastructure
- Windows Server (Active Directory Domain Services)
- DNS / DHCP / Group Policy (GPO)
- Windows 10/11 Enterprise Clients

## Networking
- pfSense Firewall (NAT, DHCP, Routing, Rules)
- VLAN concepts (via GNS3 simulation)
- TCP/IP troubleshooting

## IT Operations
- GLPI (ITSM Ticketing System)
- Zabbix (Monitoring & Alerting)

## Automation & Scripting
- PowerShell (Windows administration)
- Bash scripting (Linux automation)

## Conceptual / Enterprise Tools
- Microsoft 365 (Exchange, Teams, SharePoint)
- Azure AD (Hybrid Identity concept)

---

# 🔄 Operational Workflow (REAL IT SUPPORT SIMULATION)

This lab simulates real enterprise IT operations:

1. User reports an incident via GLPI
2. Ticket is categorized (Network / AD / System)
3. Investigation using logs (Zabbix / system tools)
4. Root cause analysis
5. Resolution applied (AD / network / system fix)
6. Ticket closure + documentation (KB update)

👉 This reflects real ITIL-based support workflow.

---

# 📊 Ticketing Summary

| Metric                   | Value       |
|-------------------------|-------------|
| Total tickets resolved  | 16+         |
| Average resolution time | ~40 minutes |
| Knowledge base articles | 16+         |
| Domains covered         | AD, M365, Network, Infrastructure |

---

# 🔥 Real-World IT Support Scenarios

## Scenario 1 — Domain Authentication Issue
- User unable to log into domain
- DNS resolution failure identified
- Root cause: DHCP misconfiguration
- Fix: Corrected DNS scope on pfSense
- Result: Access restored

---

## Scenario 2 — Network Connectivity Failure
- Multiple clients lost internet access
- pfSense logs analyzed
- Root cause: Incorrect NAT rule
- Fix: Updated firewall configuration
- Result: Network restored

---

## Scenario 3 — Active Directory Access Issue
- User cannot access shared resources
- Missing AD group membership
- Fix: Updated security group + GP refresh
- Result: Access restored

---

# 🧠 Key Skills Demonstrated

## IT Support
- Incident troubleshooting (L1 / L2)
- Ticket handling (ITSM workflow)
- User support & system access resolution

## System Administration
- Active Directory (Users, Groups, OUs)
- Group Policy configuration
- Windows Server administration

## Networking
- TCP/IP troubleshooting
- DNS / DHCP management
- Firewall configuration (pfSense)

## Monitoring
- Infrastructure monitoring (Zabbix)
- Alert handling and system diagnostics

---

# 🔐 Security Concepts

- Network segmentation (conceptual VLAN design)
- Firewall rules and NAT policies
- Active Directory security groups
- Access control enforcement

---

# 📸 Proof of Work

- Active Directory user & group management
- Group Policy (GPO) configuration
- GLPI ticket dashboard
- Zabbix monitoring alerts
- Network topology diagrams (pfSense LAN architecture)

---

# 🚀 Career Relevance (Canada Market)

This lab aligns with roles such as:

- IT Support Technician (L1 / L2)
- Help Desk Analyst
- NOC Technician
- IT Infrastructure Support Specialist
- Junior System Administrator

---

# 💡 Business Value

This project demonstrates the ability to:

- Support enterprise users in real IT environments
- Troubleshoot network and system issues under pressure
- Manage IT infrastructure using industry-standard tools
- Operate ITSM workflows similar to corporate environments
- Maintain system uptime and service reliability

---

# 🔗 Contact

- LinkedIn: Oussama Nebbak  
- Email: nebbakossama@gmail.com
