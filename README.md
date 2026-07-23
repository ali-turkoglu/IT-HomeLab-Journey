# IT HomeLab Journey

Building a professional IT HomeLab from scratch while documenting every step.

> [!TIP]
> **New to this project?**
>
> This repository is designed to be read from beginning to end.
> Each phase builds on the previous one, so I recommend following the documentation in the order shown in the **Project Roadmap** below.
---

## Table of Contents

- [Project Overview](#project-overview)
- [Project Goals](#project-goals)
- [Technology Stack](#technology-stack)
- [Hardware](#hardware)
- [HomeLab Architecture](#homelab-architecture)
- [Project Roadmap](#project-roadmap)
- [Documentation](#documentation)
- [HomeLab Log](#homelab-log)
- [License](#license)
---


## Project Overview

This repository documents the complete process of building a professional IT HomeLab from scratch.

The project focuses on designing and implementing a realistic enterprise environment using virtualization, Microsoft infrastructure, Linux, networking, containers, automation, monitoring, security and cloud technologies.

Instead of publishing only the final results, every important decision, configuration, challenge and solution is documented step by step.

The project aims to become an open technical reference for students, IT enthusiasts and aspiring system administrators by documenting every stage of the journey. It also serves as a professional portfolio that demonstrates practical skills and real-world experience.



## Project Goals

Technical Goals

- Learn and experiment with modern system administration technologies in a realistic environment.
- Refresh existing IT knowledge and combine it with modern infrastructure technologies and best practices.
- Design, build and maintain a HomeLab that simulates a realistic enterprise IT infrastructure.
- Build an affordable and energy-efficient HomeLab that delivers a realistic enterprise learning experience.
- Simulate real-world enterprise IT scenarios commonly found in modern organizations.

### Documentation & Career Goals

- Document every stage of the project, from planning to deployment and maintenance.
- Explain the reasoning behind technical decisions and compare alternative approaches whenever appropriate.
- Record challenges encountered during the implementation process together with their solutions and lessons learned.
- Create an open technical reference that can help others build their own HomeLab.
- Build a professional portfolio that demonstrates practical experience, technical documentation skills and problem-solving abilities.

### Home Services Goals

The HomeLab is not only a learning platform but also a production environment that provides useful services for the household, including:

- Personal Cloud Storage
- Online Photo Archive
- Home File Server
- Automated Backup System
- Secure Remote Access via VPN
- Network-wide Ad Blocking
- Document Management
- Home Automation Platform
- Additional self-hosted services as the infrastructure evolves


## Technology Stack

### Virtualization

- Proxmox VE

### Microsoft Infrastructure

- Windows Server
- Active Directory
- DNS
- DHCP
- Group Policy
- File Server
- Print Server
- WSUS
- Windows Server Backup

### Cloud & Identity

- Microsoft Entra ID
- Microsoft 365

### Linux

- Ubuntu Server

### Containers

- Docker
- Docker Compose
- Portainer

### Automation

- PowerShell
- Bash

### Infrastructure

- Networking
- Monitoring
- Backup & Disaster Recovery
- Security

### Network Security

- pfSense

### Version Control

- Git & GitHub
  


## Hardware

The HomeLab is built using affordable and energy-efficient hardware that balances performance, power consumption and cost.

The complete hardware selection process, device comparisons, purchasing decisions, and acceptance testing are documented in detail.

➡️ **[Phase 1 – Hardware Selection & Procurement](docs/1-Hardware/README.md)**


## HomeLab Architecture

The HomeLab architecture will evolve as new technologies and services are introduced throughout the project.

The diagrams will be updated regularly to reflect the current infrastructure.

The final documentation will include:

- Physical network topology
- Virtual infrastructure
- Active Directory architecture
- Network segmentation
- Service dependencies
- Backup strategy
- Security architecture


## Project Roadmap

The project is organized into multiple phases that gradually build a complete enterprise-style HomeLab.

### Foundation

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
- 🚧 Phase 10 – Print Server
- ⏳ Phase 11 – Windows Server Backup
- ⏳ Phase 12 – WSUS (Windows Server Update Services)

### Cloud & Identity

- ⏳ Phase 13 – Microsoft Entra ID
- ⏳ Phase 14 – Microsoft 365 Integration

### Linux & Containers

- ⏳ Phase 15 – Ubuntu Server
- ⏳ Phase 16 – Docker & Portainer
  - Docker Compose
  - Container Management
  - Self-Hosted Services

### Monitoring & Automation

- ⏳ Phase 17 – Infrastructure Monitoring (Zabbix)
- ⏳ Phase 18 – PowerShell Automation
- ⏳ Phase 19 – Bash Scripting

### Security

- ⏳ Phase 20 – Windows Security Hardening
- ⏳ Phase 21 – pfSense Firewall

### Enterprise Scenarios

- ⏳ Phase 22 – User & Group Management
- ⏳ Phase 23 – File Sharing & Permissions
- ⏳ Phase 24 – Backup & Disaster Recovery
- ⏳ Phase 25 – Enterprise Troubleshooting Scenarios

> The roadmap will continue to evolve as new technologies and enterprise scenarios are added to the HomeLab.

## Documentation

The documentation is organized into individual phases. Each phase focuses on a specific technology or project milestone and follows the same documentation structure to ensure consistency throughout the repository.

Each phase includes:

- Overview
- Objectives
- Planning
- Architecture
- Implementation
- Configuration
- Screenshots
- Verification
- Lessons Learned
- Navigation to the previous and next project phases
  

## HomeLab Log

The HomeLab Log records important milestones throughout the project.

Instead of publishing only completed work, this project documents the entire journey, including planning, implementation, challenges, improvements and lessons learned.

## Timeline

- **04-07-2026** – GitHub repository created.
- **09-07-2026** – HomeLab hardware purchased.
- **12-07-2026** – Phase 1: Hardware Selection & Procurement completed.
- **13-07-2026** – Phase 2: Proxmox VE Installation completed.
- **14-07-2026** – Phase 3: Proxmox Post-Installation Configuration completed.
- **15-07-2026** – Phase 4: Windows Server 2022 Installation completed.
- **17-07-2026** – Phase 5: Windows Server Initial Configuration completed.
- **19-07-2026** – Phase 6: Active Directory Domain Services completed.
- **19-07-2026** – Phase 7: DNS & DHCP Configuration completed.
- **20-07-2026** – Phase 8: Domain Client & Group Policy completed.
- **23-07-2026** - Phase 9: Active Directory Organization & File Sharing.

## License

This project is licensed under the MIT License.
See the LICENSE file for more information.

