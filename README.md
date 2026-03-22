# 🛡️ Network Security Homelab

> A growing collection of hands-on guides, lab walkthroughs, and concept breakdowns covering network security tools, technologies, and best practices built and tested in real homelab and cloud environments.

---

## 📋 Table of Contents

- [About This Repo](#about-this-repo)
- [Repo Structure](#repo-structure)
- [Guides Index](#guides-index)
- [Prerequisites](#prerequisites)
- [Homelab Overview](#homelab-overview)
- [Contributing](#contributing)

---

## About This Repo

This repository is a personal homelab knowledge base. Every guide here has been built hands-on — not copied from documentation. The goal is to document real deployments, real mistakes, and real fixes so that others (and future-me) can follow along without guessing.

Topics covered include firewalls, VPNs, intrusion detection, network monitoring, security concepts, and more. Guides cover both **on-premises** and **cloud (Azure)** environments.

---

## Repo Structure

```
network-security/
│
├── README.md                          ← You are here
│
├── firewalls/                         ← Firewall setup and configuration guides
│   └── azure-pfsense-nva.md
│
├── vpn/                               ← VPN technologies and tunnelling
│
├── ids-ips/                           ← Intrusion Detection and Prevention Systems
│
├── network-monitoring/                ← Traffic analysis, logging, and dashboards
│
├── labs/                              ← Full end-to-end lab scenarios
│
├── concepts/                          ← Theory and concept breakdowns
│
└── tools/                             ← Tool-specific references and cheat sheets
```

---

## Guides Index

### 🔥 Firewalls

| Guide | Platform | Description | Status |
|---|---|---|---|
| [pfSense as a Network Virtual Appliance (NVA)](firewalls/azure-pfsense-nva.md) | Azure | Deploy pfSense as a firewall using PowerShell — Marketplace and custom Hyper-V VHD methods | ✅ Complete |

---

### 🔐 VPN

| Guide | Platform | Description | Status |
|---|---|---|---|
| *Site-to-Site IPsec VPN (pfSense ↔ Azure)* | Azure | Coming soon | 🔜 Planned |
| *OpenVPN Remote Access on pfSense* | On-Prem / Azure | Coming soon | 🔜 Planned |

---

### 🚨 IDS / IPS

| Guide | Platform | Description | Status |
|---|---|---|---|
| *Suricata on pfSense* | On-Prem / Azure | Coming soon | 🔜 Planned |
| *Snort Setup and Rule Tuning* | On-Prem | Coming soon | 🔜 Planned |

---

### 📡 Network Monitoring

| Guide | Platform | Description | Status |
|---|---|---|---|
| *Wireshark Capture Analysis* | Any | Coming soon | 🔜 Planned |
| *Ntopng Traffic Dashboard* | On-Prem | Coming soon | 🔜 Planned |
| *Azure Network Watcher* | Azure | Coming soon | 🔜 Planned |

---

### 🧪 Labs

| Lab | Description | Status |
|---|---|---|
| *Lab 01 — Azure Perimeter Firewall* | Coming soon | 🔜 Planned |
| *Lab 02 — Site-to-Site VPN between Two Azure VNets* | Coming soon | 🔜 Planned |

---

### 📖 Concepts

| Concept | Description | Status |
|---|---|---|
| *Defence in Depth* | Coming soon | 🔜 Planned |
| *Zero Trust Networking* | Coming soon | 🔜 Planned |
| *Firewall Rule Design Principles* | Coming soon | 🔜 Planned |

---

### 🧰 Tools

| Tool | Description | Status |
|---|---|---|
| *nmap Cheat Sheet* | Coming soon | 🔜 Planned |
| *tcpdump Quick Reference* | Coming soon | 🔜 Planned |

---

## Prerequisites

All guides in this repo assume you have:

- An active **Azure Subscription** with Contributor or Owner rights (for cloud guides)
- **PowerShell 7+** installed locally
- The **Az PowerShell Module** installed (`Install-Module -Name Az`)
- **Hyper-V** available (for local VM guides)
- Basic familiarity with networking concepts — IP addressing, subnets, routing

---

## Homelab Overview

```
┌─────────────────────────────────────────────────────────┐
│                    Microsoft Azure                       │
│                                                         │
│  ┌──────────┐    ┌─────────────┐    ┌────────────────┐  │
│  │ Internet │───▶│  pfSense FW │───▶│  Internal VMs  │  │
│  │          │    │  (NVA)      │    │  10.0.2.x      │  │
│  └──────────┘    └─────────────┘    └────────────────┘  │
│                        │                                 │
│               ┌─────────────────┐                       │
│               │  Monitoring /   │                       │
│               │  IDS / Logging  │                       │
│               └─────────────────┘                       │
└─────────────────────────────────────────────────────────┘
          │
          │  Site-to-Site VPN (planned)
          │
┌─────────────────────────────────────────────────────────┐
│                  On-Premises Homelab                     │
│                                                         │
│  ┌──────────┐    ┌─────────────┐    ┌────────────────┐  │
│  │  Router  │───▶│  pfSense FW │───▶│  Lab VMs       │  │
│  │          │    │  (Hyper-V)  │    │  Kali, Ubuntu  │  │
│  └──────────┘    └─────────────┘    └────────────────┘  │
└─────────────────────────────────────────────────────────┘
```

---

## Contributing

This is a personal homelab repo but contributions are welcome. If you spot an error, have a better approach, or want to add a guide:

1. Fork the repo
2. Create a branch: `git checkout -b add/your-guide-name`
3. Add your guide following the existing folder structure and naming conventions
4. Open a Pull Request with a short description of what you added

**Naming conventions:**
- Files: `lowercase-with-hyphens.md`
- Folders: `lowercase-with-hyphens/`
- All guides should include a Prerequisites section and a Table of Contents

---

*Built with hands-on testing. No theory without practice.*
