# Windows Server Update Services (WSUS)

> **Status:** ✅ Completed

---

## Overview

Windows Server Update Services (WSUS) is a Microsoft server role that allows administrators to manage Windows updates from a central server.

Instead of downloading updates directly from Microsoft, client computers receive approved updates from the WSUS server. This gives administrators more control over the update process, reduces internet bandwidth usage, and allows updates to be tested before deployment.

Although this HomeLab contains only a few virtual machines, implementing WSUS demonstrates how update management is commonly handled in enterprise environments.

---

## Objectives

- Install the WSUS server role.
- Configure the WSUS server and dedicated storage.
- Synchronize updates from Microsoft Update.
- Configure Products and Classifications.
- Create Computer Groups.
- Configure Group Policy (Client-Side Targeting).
- Verify client communication with WSUS.

---

## Environment

| Component | Value |
|-----------|-------|
| Server | Windows Server 2022 Standard Evaluation |
| Role | Windows Server Update Services |
| Domain | homelab.local |
| Client | Windows 11 Enterprise |
| Virtualization | Proxmox VE |

---

## Real-World Scenario

In most organizations, computers do not download updates directly from Microsoft. Instead, administrators synchronize updates with WSUS, review them, approve the required updates, and deploy them to client computers in a controlled way. 

This helps reduce the risk of problematic updates crashing business-critical systems and saves huge amounts of internet bandwidth.

*(Note: To keep this documentation simple and easy to read, only configuration steps that required a decision or a change are shown. Default and informational wizard pages are intentionally omitted).*

---

## 1. Installation & Storage Preparation

### Add a Dedicated Virtual Disk
Before installing WSUS, I added a dedicated **20 GB virtual disk** in Proxmox. WSUS content can grow quickly over time. Keeping update files on a separate disk helps prevent the operating system drive from running out of free space.

After adding the new virtual disk, I initialized it in Windows Disk Management, formatted it with NTFS, and assigned the drive letter **E:**. I created a dedicated folder named **WSUS** to store update files.

| Add WSUS Disk in Proxmox | WSUS Dedicated Storage (E:) |
|:------------------------:|:---------------------------:|
| ![](images/04-add-wsus-disk-proxmox.png) | ![](images/05-wsus-dedicated-storage.png) |

---

### Install the WSUS Role
I installed the **Windows Server Update Services** role using Server Manager. Windows automatically selected the required features. For this HomeLab, I selected the default WSUS services and used the Windows Internal Database (WID) instead of a SQL Server database. 

I selected the `E:\WSUS` folder as the content location.

| Select WSUS Role & Features | WSUS Content Location |
|:---------------------------:|:---------------------:|
| ![](images/01-add-roles-and-features.png)<br>![](images/02-add-required-features.png) | ![](images/03-select-role-services.png) <br> ![](images/07-wsus-content-location.png) |

After the installation finished, Windows required a short post-installation configuration. The post-installation tasks completed successfully.

| Confirm Installation | Post-Installation Tasks |
|:--------------------:|:-----------------------:|
| ![](images/09-confirm-installation.png) | ![](images/10-wsus-installation-completed.png)<br>![](images/11-post-installation-tasks.png) |

---

## 2. Initial Configuration Wizard

After the installation, I launched the **WSUS Configuration Wizard**.

- **Upstream Server:** I configured WSUS to synchronize updates directly from **Microsoft Update** (No upstream WSUS server is used in this lab).
- **Proxy:** A proxy server is not used in this HomeLab.

| Configuration Wizard | Upstream Server |
|:--------------------:|:---------------:|
| ![](images/12-wsus-configuration-wizard.png) | ![](images/14-choose-upstream-server.png) |

- **Products:** I selected only the Microsoft products used in this HomeLab to save disk space: *Windows 11*, *Microsoft Server Operating System 22H2*, and *Microsoft Defender Antivirus*.
- **Classifications:** I selected the update categories that are most important for a small lab environment: *Critical Updates*, *Definition Updates*, and *Security Updates*.
- **Synchronization:** I chose to start the first synchronization manually.

| Classifications Selection |
|:-------------------------:|
| ![](images/17-classifications-selection.png) |

---

## 3. Initial Synchronization

After completing the initial configuration, I manually started the first synchronization.

The synchronization completed successfully and WSUS downloaded the update metadata from Microsoft Update.

In this HomeLab, the first synchronization found:

- **485** new updates
- **275** expired updates
- **0** synchronization errors

This confirms that the WSUS server is communicating correctly with Microsoft Update and is ready to manage updates for client computers.

| Initial Synchronization |
|:-----------------------:|
| ![](images/23-Synchronizations-Succeeded.png) |

---

## 4. WSUS Console & Computer Groups

After the configuration wizard finished, the WSUS console was available.

To organize update management, I created two computer groups: **Servers** and **Workstations**. This allows me to apply different update policies for servers and client computers.

| WSUS Console Overview | Computer Groups |
|:---------------------:|:---------------:|
| ![](images/18-wsus-console-overview.png) | ![](images/19-computer-groups.png) |

---

## 5. Configure Group Policy

To simulate a real enterprise environment, I created separate Group Policies for workstations and servers. This allows each device type to receive updates using its own schedule.

### Workstations Policy

I created a GPO named **HomeLab - WSUS Workstations** and linked it to the Workstations organizational unit.
- WSUS Server: `http://WIN-SRV01:8530`
- Client-Side Targeting: `Workstations`
- Automatic Updates: Download and install updates every day at 03:00.

| WSUS Server Location | Client-Side Targeting |
|:--------------------:|:---------------------:|
| ![](images/20-gpo-wsus-server-location.png) | ![](images/21-gpo-client-side-targeting.png) |

| Automatic Updates Configuration |
|:-------------------------------:|
| ![](images/22-gpo-configure-automatic-updates.png) |

### Servers Policy

I also created a second Group Policy named **HomeLab - WSUS Servers** and linked it to the Servers organizational unit. The configuration is the same, but the Client-Side Targeting setting uses the **Servers** computer group instead.

> **Design Decision Note:**
> The Domain Controller was intentionally excluded from the WSUS server policy. In many enterprise environments, Domain Controllers are managed using dedicated update policies and scheduled maintenance windows.

---

## Common Issues

During real-world WSUS deployments, administrators often face issues. Some of the most common problems include:

- Clients do not appear in WSUS.
- Group Policy is not applied.
- Synchronization fails.
- Incorrect client-side targeting.
- Clients continue using Microsoft Update instead of the internal server.
- Firewall blocks WSUS communication.

---

## Lessons Learned

- WSUS provides incredible centralized control over Windows updates.
- Using separate Computer Groups makes update management more flexible.
- Keeping update files on a dedicated disk (E:) helps prevent the operating system drive from running out of free space.
- Excluding Domain

  ---

## Navigation

| Previous | Home | Next |
|----------|------|------|
| ⬅️  [Veeam Backup & Replication](../11b-Veeam-Backup&Replication/README.md) | 🏠 [Home](../../README.md) | ➡️ **Coming Soon** |
