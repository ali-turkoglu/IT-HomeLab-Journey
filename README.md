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

### Technical Goals

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

### Linux

- Ubuntu Server
- Bash

### Containers

- Docker
- Portainer

### Automation

- PowerShell
- Bash

### Infrastructure

- Networking
- Virtualization
- Backup
- Monitoring
- Security
- pfSense

### Cloud & Identity

- Microsoft Entra ID
- Microsoft 365

### Version Control

- Git & GitHub
  


## Hardware

The HomeLab is built using affordable and energy-efficient hardware that balances performance, power consumption and cost.

The complete hardware selection process, device comparisons, purchasing decisions, and acceptance testing are documented in detail.

➡️ **[Phase 1 – Hardware Selection & Procurement](docs/1-Hardware/README.md)**


## HomeLab Architecture

The architecture will evolve together with the HomeLab.

As new services are deployed, the architecture diagrams will be updated to reflect the current infrastructure.

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

- 🚧 Phase 4 – Windows Server Installation
- ⏳ Phase 5 – Active Directory Domain Services
- ⏳ Phase 6 – DNS
- ⏳ Phase 7 – DHCP
- ⏳ Phase 8 – Group Policy
- ⏳ Phase 9 – File Server & NTFS Permissions
- ⏳ Phase 10 – Print Server
- ⏳ Phase 11 – Windows Server Backup
- ⏳ Phase 12 – WSUS (Windows Server Update Services)

### Linux & Containers

- ⏳ Phase 13 – Ubuntu Server
- ⏳ Phase 14 – Docker & Portainer

### Monitoring & Automation

- ⏳ Phase 15 – Zabbix Monitoring
- ⏳ Phase 16 – PowerShell Automation
- ⏳ Phase 17 – Bash Scripting

### Security

- ⏳ Phase 18 – Windows Security Hardening
- ⏳ Phase 19 – pfSense Firewall

### Cloud & Identity

- ⏳ Phase 20 – Microsoft Entra ID
- ⏳ Phase 21 – Microsoft 365 Integration

### Enterprise Scenarios

- ⏳ Phase 22 – User & Group Management
- ⏳ Phase 23 – File Sharing & Permissions
- ⏳ Phase 24 – Backup & Disaster Recovery
- ⏳ Phase 25 – Enterprise Troubleshooting Scenarios


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

04-07-2026 – GitHub repository created.
09-07-2026 – HomeLab hardware purchased.
12-07-2026 – Phase 1: Hardware Selection & Procurement completed.
13-07-2026 – Phase 2: Proxmox VE Installation completed.
14-07-2026 – Phase 3: Proxmox Post-Installation Configuration completed.


## License

This project is licensed under the MIT License.
See the LICENSE file for more information.

