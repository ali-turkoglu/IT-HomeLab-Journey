# 10 – Print Server Configuration

> **Status:** ✅ Completed

---

## Overview

In this phase, I deployed a centralized Print Server in my HomeLab environment using Windows Server.

Instead of installing and configuring the network printer manually on each client computer, I shared the printer through the Print Server and deployed it automatically with Group Policy. This approach simplifies printer management, provides a consistent configuration across domain-joined computers, and reflects how printers are commonly managed in enterprise environments.

To ensure reliable communication, I assigned a static IP address to the printer and configured my home router to always reserve the same IP address based on the printer's MAC address.

---

## Objectives

- Install the Print and Document Services role.
- Configure a network printer on the Print Server.
- Share the printer with domain users.
- Deploy the shared printer using Group Policy.
- Verify automatic printer installation on a Windows 11 domain client.

---

## Installing the Print Server Role & Preparing the Printer

The first step was to install the **Print and Document Services** role on Windows Server. This role provides centralized printer management and allows printers to be shared across the Active Directory environment.

Before adding the printer to the server, I configured a static IP address directly from the printer's network settings. To prevent future IP conflicts, I also configured my home router to always reserve the same IP address for the printer based on its MAC address.

After completing the network configuration, I added the printer to the Print Server using its TCP/IP address. *(Note: IP addresses are redacted for security reasons).*

| Install Print Services Role | TCP/IP Printer Configuration |
|:---------------------------:|:----------------------------:|
| ![](images/01-print-role.png) | ![](images/02-tcp-ip-config.png) |

---

## Sharing the Printer

After Windows detected the network printer, I installed the **HP Universal Printing PCL 6** driver and configured the printer as a shared network resource.

The printer was published with the share name **HomeLab-Printer**, allowing domain clients to access it through the Print Server instead of connecting directly to the physical printer.

| Printer Name and Sharing | Print Management Console |
|:------------------------:|:------------------------:|
| ![](images/03-printer-sharing.png) | ![](images/04-print-management.png) |

---

## Deploying the Printer with Group Policy

Instead of installing the printer manually on each computer, I deployed the shared printer through **Group Policy**.

In the Print Management console, I used the "Deploy with Group Policy" feature. I created a dedicated GPO named **HomeLab Printer Deployment** and configured it to deploy the shared printer automatically to all computers in the domain (Per Machine connection).

| Deploy with Group Policy | GPO Applied Successfully |
|:------------------------:|:------------------------:|
| ![](images/05-deploy-gpo-setup.png) | ![](images/06-deploy-gpo-applied.png) |

---

## Verification

Finally, I checked the Group Policy Management Console to ensure the new GPO was linked and enabled in the `homelab.local` domain. 

Then, I switched to my Windows 11 domain client, restarted the computer, and verified that the shared printer appeared automatically under **Printers & Scanners**.

This confirmed that the Print Server deployment was working successfully and that the printer was automatically deployed through Group Policy.

| GPO Linked to Domain | Windows 11 Client Verification |
|:--------------------:|:------------------------------:|
| ![](images/07-gpo-console.png) | ![](images/08-client-verification.png) |

---

## Lessons Learned

- A Print Server makes it much easier to manage shared printers from a central location.
- Assigning a static IP address to the printer helps ensure reliable communication.
- Reserving the printer's IP address on the router helps avoid future IP conflicts.
- Deploying printers with Group Policy saves time by eliminating manual installation on each client computer.
- Using a separate GPO for printer deployment keeps Group Policy settings organized and easier to manage.

---

## Navigation

| Previous | Home | Next |
|:--------:|:----:|:----:|
| ⬅️ [Active Directory Organization](../9-Active-Directory-Organization&Security-File-Sharing/README.md) | 🏠 [Home](../../README.md) | ➡️ [Windows Backup Server](../11-Windows-Backup-Server/README.md) |
