# 🖥️ IT Support Home Lab — TechMaroc SARL

> Infrastructure IT complète simulant une PME marocaine réelle.  
> Projet conçu pour démontrer des compétences en **support IT, administration système, réseau et ITSM**.

---

## 🎯 Objectif du projet

Ce laboratoire simule une infrastructure d’entreprise incluant :

- Active Directory (gestion des utilisateurs, groupes et GPO)
- Réseau sécurisé avec pfSense
- Supervision infrastructure avec Zabbix
- Gestion des incidents IT avec GLPI
- Environnement hybride Microsoft 365 / Azure AD (concept)

👉 Objectif : reproduire un environnement réel de **support IT niveau entreprise (L1/L2)**.

---

## 🏗️ Architecture du lab

| Machine   | Rôle                                    | IP Address            |
|------------|----------------------------------------|----------------------|
| pfSense    | Firewall / Router / DHCP               | 192.168.10.1         |
| DC-01      | Active Directory / DNS / GPO           | 192.168.10.2         |
| SRV-LINUX  | GLPI + Zabbix Monitoring               | 192.168.10.20        |
| PC-01      | Windows 10/11 Workstation (Domain Join)| DHCP (192.168.10.100+) |
| PC-02      | Windows 10/11 Workstation (Domain Join)| DHCP (192.168.10.100+) |

---

## 🛠️ Technologies utilisées

- Active Directory (Users, Groups, OUs, GPO, DNS)
- Microsoft 365 (Exchange, Teams, SharePoint, OneDrive)
- Azure AD Connect (Hybrid Identity concept)
- GLPI (ITSM Ticketing system)
- Zabbix (Monitoring & alerting)
- pfSense (Firewall, NAT, VPN, DHCP)
- GNS3 (Network simulation: VLANs, routing, ACLs)
- PowerShell / Bash (Automation & scripting)

---

## 📂 Structure du projet
IT-Support-Homelab/
├── Architecture/ # Network diagrams + VM specs
├── Lab-Setup/ # Step-by-step installation guides
├── Network-Labs/ # GNS3 labs (routing, VLAN, DHCP)
├── Tickets/ # Incident management (ITIL style)
├── Runbooks/ # Operational procedures
├── Security/ # Firewall rules, GPO, policies
├── Screenshots/ # Proof of work (AD, GLPI, Zabbix)
├── Scripts/ # PowerShell & automation scripts
├── Templates/ # Ticket & KB templates
└── Reports/ # Weekly reports 

---

## 📊 Ticketing Summary

| Metric                   | Value       |
|-------------------------|-------------|
| Total tickets resolved  | 16+         |
| Average resolution time  | ~40 minutes |
| Knowledge base articles | 16+         |
| Domains covered         | AD, M365, Network, Infra |

---

## 📸 Evidence & Screenshots

This section includes real proof of implementation:

- Active Directory user management
- Group Policy (GPO) configuration
- GLPI dashboard (ticketing system)
- Zabbix monitoring alerts
- Network topology diagram (draw.io)

---

## 🔐 Key Skills Demonstrated

- IT Support (Level 1 / Level 2)
- Windows Server Administration
- Active Directory Management
- Network troubleshooting
- ITSM (Incident & Request management)
- System monitoring (Zabbix)
- Basic cybersecurity hardening
- Automation with PowerShell / Bash

---

## 🚀 Project Value

This project simulates a real enterprise IT environment and demonstrates:

- Real-world troubleshooting scenarios
- IT infrastructure deployment
- Network and security configuration
- Helpdesk and ITSM workflows

---

## 🔗 Contact

- 💼 LinkedIn: Oussama Nebbak
- 📧 Email: nebbakossama@gmail.com