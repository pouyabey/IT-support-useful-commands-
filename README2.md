# 🛠️ IT Support Master Command Reference

![Windows](https://img.shields.io/badge/Windows-Command%20Reference-0078D4?style=for-the-badge&logo=windows&logoColor=white)
![IT Support](https://img.shields.io/badge/IT%20Support-Help%20Desk-0EA5E9?style=for-the-badge)
![Troubleshooting](https://img.shields.io/badge/Windows-Troubleshooting-22C55E?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Growing%20Reference-F97316?style=for-the-badge)

Essential Windows commands every IT Support technician should know.

This repository is a growing command reference for **IT Support**, **Help Desk**, **Desktop Support**, and **Windows troubleshooting** tasks.

---

## 📌 Table of Contents

- [⚡ System Performance & Maintenance](#-system-performance--maintenance)
- [🌐 Network Troubleshooting](#-network-troubleshooting)
- [🖥️ System Administration & Diagnostics](#️-system-administration--diagnostics)
- [🖧 Remote Desktop & Remote Access](#-remote-desktop--remote-access)
- [👤 User Account Management](#-user-account-management)
- [🖨️ Printers & Devices](#️-printers--devices)
- [🚀 Professional Power User Shortcuts](#-professional-power-user-shortcuts)
- [🧰 Common Run Commands](#-common-run-commands)
- [⚠️ Notes](#️-notes)

---

![System Performance](https://img.shields.io/badge/System%20Performance%20%26%20Maintenance-0EA5E9?style=for-the-badge&logo=windows&logoColor=white)

## ⚡ System Performance & Maintenance

Use these commands when the PC is **slow**, **freezing**, **acting up**, or needs cleanup.

| Command | Action |
|---|---|
| `%temp%` | Opens the current user's temporary files folder for cleanup. |
| `temp` | Opens the Windows system temporary files folder. |
| `prefetch` | Opens the Prefetch folder. Cleaning this may help with some boot or application issues. |
| `taskmgr` | Opens **Task Manager** immediately. |
| `resmon` | Opens **Resource Monitor** for detailed CPU, memory, disk, and network usage tracking. |
| `cleanmgr` | Runs **Disk Cleanup** to remove system junk files and old Windows update files. |
| `sfc /scannow` | Runs **System File Checker** to scan and repair corrupted Windows system files. |
| `DISM /Online /Cleanup-Image /RestoreHealth` | Repairs the Windows system image. This is commonly used when SFC cannot fix the issue. |
| `powercfg /h off` | Disables **Hibernation** and can free up several gigabytes of disk space. |

---

![Network Troubleshooting](https://img.shields.io/badge/Network%20Troubleshooting-22C55E?style=for-the-badge&logo=internetexplorer&logoColor=white)

## 🌐 Network Troubleshooting

Use these commands when the internet is down, DNS is not working, or connectivity is unstable.

| Command | Action |
|---|---|
| `ipconfig /all` | Displays all network adapter details, including **MAC address**, **DNS**, **DHCP**, IP address, and gateway. |
| `ipconfig /release` | Releases the current IP address from the network adapter. |
| `ipconfig /renew` | Requests a new IP address from the DHCP server. |
| `ipconfig /flushdns` | Clears the DNS cache. This can help fix **site not found** or DNS resolution issues. |
| `ping -t [IP/URL]` | Runs a continuous ping to check for intermittent connection drops. |
| `tracert [IP/URL]` | Shows the path that network traffic takes to reach a destination. |
| `netstat -an` | Lists active network connections and listening ports. |
| `nslookup [URL]` | Checks whether DNS is correctly resolving a domain name. |
| `netsh winsock reset` | Resets the Windows network stack. Useful when network settings are corrupted or connectivity issues persist. |
| `ncpa.cpl` | Opens **Network Connections**, where you can enable/disable adapters, check adapter status, and configure IPv4/IPv6 settings. |

---

![System Administration](https://img.shields.io/badge/System%20Administration%20%26%20Diagnostics-A855F7?style=for-the-badge&logo=powershell&logoColor=white)

## 🖥️ System Administration & Diagnostics

Use these commands for Windows diagnostics, hardware checks, device management, logs, services, and system information.

| Command | Action |
|---|---|
| `msinfo32` | Opens **System Information** and displays a full system summary, including hardware, components, and software environment. |
| `eventvwr.msc` | Opens **Event Viewer** to check system, application, security, and crash logs. |
| `devmgmt.msc` | Opens **Device Manager** to troubleshoot drivers, hardware devices, and unknown devices. |
| `diskmgmt.msc` | Opens **Disk Management** for formatting, partitioning, and checking drives. |
| `chkdsk /f /r` | Scans the hard drive for file system errors, physical errors, and bad sectors. |
| `gpupdate /force` | Forces an immediate **Group Policy** update. Useful after domain or policy changes. |
| `wmic bios get serialnumber` | Shows the PC serial number or service tag. Useful for inventory and warranty checks. |
| `dxdiag` | Opens **DirectX Diagnostic Tool** to check display, sound, and system information. |
| `systeminfo \| findstr /B /C:"Domain"` | Shows the domain or workgroup that the computer belongs to. Useful for checking if a PC is joined to a domain. |
| `services.msc` | Opens **Windows Services** to start, stop, restart, or check the status of system services. |
| `firewall.cpl` | Opens **Windows Defender Firewall** settings. Useful for checking firewall status and allowed apps. |

---

![Remote Desktop](https://img.shields.io/badge/Remote%20Desktop%20%26%20Remote%20Access-F97316?style=for-the-badge&logo=microsoft&logoColor=white)

## 🖧 Remote Desktop & Remote Access

Use these commands when troubleshooting **RDP**, remote access, or advanced startup options.

| Command | Action |
|---|---|
| `mstsc` | Opens **Remote Desktop Connection**. Used to connect to another Windows computer or server through RDP. |
| `SystemPropertiesRemote` | Opens **Remote System Properties**. Used to enable Remote Desktop and check remote access settings. |
| `shutdown /r /o /f /t 0` | Restarts the computer immediately and opens **Advanced Startup Options**. Useful for recovery, Safe Mode, Startup Repair, and troubleshooting boot issues. |

---

![User Account Management](https://img.shields.io/badge/User%20Account%20Management-EF4444?style=for-the-badge&logo=windows11&logoColor=white)

## 👤 User Account Management

Use these commands when creating, deleting, or managing local Windows users.

| Command | Action |
|---|---|
| `net user testuser password /add` | Creates a new local user named `testuser` with the password `password`. Replace the username and password with your own values. |
| `net user testuser /delete` | Deletes the local user account named `testuser`. Use carefully because this removes the account from the computer. |

### Example

```cmd
net user john P@ssword123 /add
