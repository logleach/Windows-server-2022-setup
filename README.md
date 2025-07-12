# Windows-server-2022-setup
Dcoumentation and hands-on setup of Windows Server 2022 in a Proxmox virtual environment for home lab testing. 

# 🖥️ Windows Server 2022 Setup in Proxmox

This repository documents the step-by-step process I followed to install and configure Windows Server 2022 in my home lab environment using Proxmox VE. It includes VM specs, installation steps, server role setup, remote access tools, and future update logs.

---

## 🔧 Project Overview

- 📍 **Host**: Proxmox VE on Dell PowerEdge R610
- 💽 **Guest OS**: Windows Server 2022 (Evaluation Edition)
- 🎯 **Purpose**: Build hands-on experience with Windows Server administration, Active Directory, DNS, and secure remote access

---

## 💻 VM Configuration

| Setting        | Value                     |
|----------------|---------------------------|
| OS             | Windows Server 2022       |
| CPU            | 2 Cores                   |
| RAM            | 4 GB                      |
| Disk           | 80 GB (SCSI)              |
| Network        | Bridged Adapter (Default) |
| Tools          | VirtIO drivers (if needed) |

---

## ⚙️ Installation Steps

1. Upload the Windows Server ISO to Proxmox
2. Create a new VM with the above specs
3. Boot into the ISO and install Windows Server 2022 (Desktop Experience)
4. Set a static IP and rename the server (e.g., `homelabserver`)
5. Enable Remote Desktop for access
6. Update Windows and configure basic security settings

---

## 🧱 Roles Installed

- ✅ Active Directory Domain Services (AD DS)
- ✅ DNS Server
- ✅ DHCP Server (optional)

### 🔹 Install Roles via PowerShell
```powershell
Install-WindowsFeature AD-Domain-Services, DNS -IncludeManagementTools
