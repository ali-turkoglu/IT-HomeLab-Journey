# Enterprise Windows Infrastructure Lab

> **Part 1 of the IT Infrastructure Lab Series**
>
> This repository shows how I built a complete Windows enterprise infrastructure in my HomeLab from scratch. Every phase is documented step by step, from the first hardware purchase to a fully working Windows Server environment.

> [!TIP]
> **New to this repository?**
>
> I recommend reading the documentation from beginning to end. Each phase builds on the previous one, making it easier to understand how the entire environment was designed and configured.

---

# Table of Contents

- [Project Overview](#project-overview)
- [Project Objectives](#project-objectives)
- [Technology Stack](#technology-stack)
- [Hardware](#hardware)
- [Architecture](#architecture)
- [Project Roadmap](#project-roadmap)
- [Project Timeline](#project-timeline)
- [Next Project](#next-project)
- [IT Infrastructure Lab Series](#it-infrastructure-lab-series)
- [License](#license)

---

# Project Overview

This repository documents the first part of my IT Infrastructure Lab Series.

The goal of this project was to build a realistic Windows enterprise environment in a HomeLab using modern Microsoft technologies. Instead of showing only the final result, I documented every important step along the way, including planning, installation, configuration, troubleshooting, and lessons learned.

The environment was built from scratch using Proxmox VE and Windows Server. During the project I configured Active Directory, DNS, DHCP, Group Policy, File Services, Print Services, Backup solutions, and WSUS, just like they are commonly used in many organizations.

This repository is both a learning project and a technical portfolio. I hope it can also help anyone who wants to build a similar HomeLab or learn Windows system administration.

---

# Project Objectives

The main goals of this project were to:

- Build a realistic Windows enterprise environment in a HomeLab.
- Learn and apply Microsoft infrastructure technologies.
- Follow common enterprise best practices whenever possible.
- Document every important step, decision, and problem during the project.
- Create a technical reference that others can learn from.
- Build a professional GitHub portfolio with real hands-on projects.

---

# Technology Stack

### Virtualization

- Proxmox VE

### Operating Systems

- Windows Server 2022
- Windows 11 Enterprise

### Microsoft Infrastructure

- Active Directory Domain Services (AD DS)
- DNS
- DHCP
- Group Policy
- File Server
- Print Server

### Backup & Recovery

- Windows Server Backup
- Veeam Backup & Replication

### Updates & Security

- Windows Server Update Services (WSUS)
- Windows Defender Firewall

### Version Control

- Git
- GitHub

---

# Hardware

The HomeLab is built on affordable and energy-efficient hardware that provides a good balance between performance, power consumption, and cost.

The complete hardware selection process, purchasing decision, and acceptance testing are documented in detail.

➡️ **[Phase 1 – Hardware Selection & Procurement](docs/1-Hardware/README.md)**

---

# Architecture

This repository focuses on the Windows infrastructure running inside my HomeLab.

The environment includes:

- Physical HomeLab hardware
- Proxmox VE virtualization
- Windows Server
- Active Directory
- DNS & DHCP
- Group Policy
- File Server
- Print Server
- Backup solutions
- WSUS

The architecture diagrams will continue to improve as the documentation grows.

---

# Project Roadmap

The project is divided into small phases. Each phase focuses on one technology and builds on the previous one.

## Foundation

- ✅ [Phase 1 – Hardware Selection & Procurement](docs/1-Hardware/README.md)
- ✅ [Phase 2 – Proxmox VE Installation](docs/2-Proxmox/README.md)
- ✅ [Phase 3 – Proxmox Post-Installation Configuration](docs/3-Proxmox-Configuration/README.md)

### Microsoft Infrastructure

- ✅ [Phase 4 – Windows Server Installation](docs/4-Windows-Server-Installation/README.md)
- ✅ [Phase 5 – Windows Server Initial Configuration](docs/5-Windows-Server-Initial-Configuration/README.md)
- ✅ [Phase 6 – Active Directory Domain Services](docs/6-Active-Directory-Domain-Services/README.md)
- ✅ [Phase 7 – DNS-DHCP](docs/7-DNS-DHCP/README.md) 
- ✅ [Phase 8 – Domain Client & Group Policy](docs/8-Domain-Client&Group-Policy/README.md)
- ✅ [Phase 9 – Active Directory Organization & File Sharing](docs/9-Active-Directory-Organization&Security-File-Sharing/README.md)
- ✅ [Phase 10 – Print Server Configuration](docs/10–Print-Server-Configuration/README.md)
- ✅ [Phase 11a – Windows Server Backup](docs/11-Windows-Backup-Server/README.md)
- ✅ [Phase 11b - Veeam Backup & Replication](docs/11b-Veeam-Backup&Replication/README.md)
- ✅ [Phase 12 – WSUS (Windows Server Update Services)](docs/12-WSUS/README.md)

> **Project Status:** ✅ Completed

---

# Project Timeline

This timeline shows the main milestones of the project.

| Date | Milestone |
|------|-----------|
| 04-07-2026 | GitHub repository created |
| 09-07-2026 | HomeLab hardware purchased |
| 12-07-2026 | Phase 1 completed |
| 13-07-2026 | Phase 2 completed |
| 14-07-2026 | Phase 3 completed |
| 15-07-2026 | Phase 4 completed |
| 17-07-2026 | Phase 5 completed |
| 19-07-2026 | Phase 6 completed |
| 19-07-2026 | Phase 7 completed |
| 20-07-2026 | Phase 8 completed |
| 23-07-2026 | Phase 9 completed |
| 24-07-2026 | Phase 10 completed |
| 25-07-2026 | Phase 11a completed |
| 26-07-2026 | Phase 11b completed |
| 27-07-2026 | Phase 12 completed |

---

# Next Project

## Enterprise Cloud & Identity Lab

This Windows infrastructure is the foundation for the next project.

The next repository will continue with modern Microsoft cloud technologies, including:

- Microsoft Entra ID
- Microsoft 365
- Microsoft Intune
- Exchange Online
- Microsoft Teams
- SharePoint Online
- Hybrid Identity
- Azure

➡️ **Repository:** *Coming Soon*

---

# IT Infrastructure Lab Series

This repository is the first project in my IT Infrastructure Lab Series.

Each repository focuses on a different area of enterprise IT while staying connected as part of the same HomeLab.

| Status | Repository |
|--------|------------|
| ✅ | **Enterprise Windows Infrastructure Lab** *(Current Repository)* |
| 🚧 | **Enterprise Cloud & Identity Lab** |
| ⏳ | **Enterprise Linux & Containers Lab** |
| ⏳ | **Enterprise Monitoring & Automation Lab** |
| ⏳ | **Enterprise Network Security Lab** |
| ⏳ | **Enterprise IT Service Management Lab** |

The series will continue as I build and document more enterprise technologies.

---

# License

This project is licensed under the MIT License.

See the **LICENSE** file for more information.
