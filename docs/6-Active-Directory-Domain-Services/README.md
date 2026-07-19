# Phase 6 – Active Directory Domain Services

> **Status:** ✅ Completed

---

## Project Overview

In this phase, I installed and configured Active Directory Domain Services (AD DS).

This process promoted my standalone Windows Server to a Domain Controller (DC). This is an important step because Active Directory will manage all users, computers, and permissions in my HomeLab.

---

## Installing the Active Directory Domain Services Role

I opened **Server Manager** to start installing the Active Directory Domain Services (AD DS) role.

I selected the **Role-based or feature-based installation** option and chose the local server from the **Server Pool**.

Even though this HomeLab contains only one server, Server Manager can also install roles on remote Windows servers.

I selected **Active Directory Domain Services** from the available server roles. Windows Server automatically selected the required management tools for Active Directory administration.

| Select AD DS Role | Post-Installation Warning |
|:-----------------:|:-------------------------:|
| ![](images/01-add-roles.png) | ![](images/02-promote-warning.png) |

After the role installation completed, Windows Server required additional configuration before the server could become a Domain Controller.

I clicked the yellow warning icon and selected **Promote this server to a domain controller**.

---

## Creating a New Forest

Since this was the first Domain Controller in my HomeLab environment, I selected the option to create a new forest.

The root domain name I chose is:

**`homelab.local`**

| Deployment Configuration | Domain Controller Options |
|:------------------------:|:-------------------------:|
| ![](images/03-deployment-config.png) | ![](images/04-dc-options.png) |

---

## Domain Controller Options

I kept the default settings for the functional levels:

- **Forest functional level:** Windows Server 2016
- **Domain functional level:** Windows Server 2016

The **DNS Server** and **Global Catalog (GC)** options were selected automatically.

I also created a **Directory Services Restore Mode (DSRM)** password. I saved this password because it is required if I ever need to restore Active Directory.

---

## Prerequisites Check

Before starting the installation, Windows Server validated my configuration.

| Review Options | Prerequisites Check |
|:--------------:|:-------------------:|
| ![](images/05-review-options.png) | ![](images/06-prerequisites-check.png) |

During the check, I saw a warning about DNS delegation.

This warning is expected in a new HomeLab environment because there is no existing parent DNS infrastructure, so it can be safely ignored.

All prerequisite checks passed successfully, and I clicked **Install**.

---

## Validation

After the installation was finished, the server automatically restarted.

When it booted up, the login screen showed that I was now logging into the `HOMELAB` domain instead of the local computer.

To verify that the Domain Controller was working correctly, I opened **Active Directory Users and Computers**.

| Active Directory Users and Computers |
|:------------------------------------:|
| ![](images/07-aduc-verification.png) |

I saw that the new `homelab.local` domain was created successfully. The default containers, such as **Builtin**, **Computers**, **Domain Controllers**, and **Users**, were created automatically during the domain promotion process.

I also verified the domain configuration using PowerShell.

| PowerShell Validation |
|:---------------------:|
| ![](images/08-powershell-validation.png) |

The validation confirmed that the Domain Controller was configured successfully.

---

## Lessons Learned

- Installing the AD DS role does not immediately make the server a Domain Controller. The server must be promoted after the role installation.
- The DNS delegation warning is expected in an isolated HomeLab environment and can be safely ignored.
- Promoting a server to a Domain Controller automatically creates the basic Active Directory structure.

---

## Next Step

Now that Active Directory is running, the next step is to configure DNS and then deploy DHCP. This will allow other computers and virtual machines to join the domain automatically.

---

## Navigation

| Previous | Home | Next |
|----------|------|------|
| ⬅️ [Initial Configuration](../5-Windows-Server-Initial-Configuration/README.md) | 🏠 [Home](../../README.md) | ➡️ [DNS & DHCP Configuration](../7-DNS-DHCP-Configuration/README.md) |
