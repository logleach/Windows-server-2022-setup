# 📋 Changelog – Windows Server 2022 Setup

This changelog tracks all major updates, configuration changes, and improvements made to the Windows Server 2022 VM in my home lab.

---

## [2025-07-12] – Initial Deployment
- Created new Windows Server 2022 VM in Proxmox
- Installed OS using Microsoft evaluation ISO
- Set static IP and renamed the server to `homelabserver`
- Enabled Remote Desktop for remote access
- Installed Active Directory Domain Services and DNS roles
- Promoted the server to a Domain Controller
- Configured basic domain and user accounts
- Installed Windows Updates

---

## [Upcoming]
- Configure DHCP Server role
- Create baseline Group Policy Objects (GPOs)
- Backup and export AD config
- Test joining a client machine to the domain
