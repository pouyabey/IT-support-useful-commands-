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

```

![Printers](https://img.shields.io/badge/Printers%20%26%20Devices-EAB308?style=for-the-badge&logo=printables&logoColor=black)
![Printer Support](https://img.shields.io/badge/Printer-Support-FDE047?style=flat-square)
![Devices](https://img.shields.io/badge/Devices-Troubleshooting-FACC15?style=flat-square)

## 🖨️ Printers & Devices

Use these commands when troubleshooting **printers**, **default printer settings**, or connected devices.

| Command | Action |
|---|---|
| `control printers` | Opens **Devices and Printers**. Useful for checking installed printers, setting the default printer, removing old printers, and troubleshooting print issues. |

---

![Shortcuts](https://img.shields.io/badge/Professional%20Power%20User%20Shortcuts-64748B?style=for-the-badge&logo=windows&logoColor=white)
![Keyboard](https://img.shields.io/badge/Keyboard-Shortcuts-94A3B8?style=flat-square)
![Fast Access](https://img.shields.io/badge/Fast-Access-475569?style=flat-square)

## 🚀 Professional Power User Shortcuts

Useful Windows keyboard shortcuts for faster **IT support**, **navigation**, and **troubleshooting** work.

| Shortcut | Action |
|---|---|
| `Win + X` | Opens the **Power User Menu**. Provides quick access to Admin Terminal, Device Manager, Disk Management, Network Connections, and more. |
| `Ctrl + Shift + Esc` | Opens **Task Manager** directly. |
| `Win + L` | Locks the workstation immediately. |
| `Win + Shift + S` | Opens the Windows snipping tool for screenshots. |
| `Win + R` | Opens the **Run** dialog box. You can type many commands from this reference here. |

---

![Common Run Commands](https://img.shields.io/badge/Common%20Run%20Commands-06B6D4?style=for-the-badge&logo=gnometerminal&logoColor=white)
![Run Dialog](https://img.shields.io/badge/Win%20%2B%20R-Run%20Dialog-0891B2?style=flat-square)
![Quick Access](https://img.shields.io/badge/Quick-Access-67E8F9?style=flat-square&logoColor=black)

## 🧰 Common Run Commands

These commands are commonly opened by pressing `Win + R`, then typing the command.

| Run Command | Action |
|---|---|
| `control printers` | Opens **Devices and Printers**. |
| `ncpa.cpl` | Opens **Network Connections**. |
| `mstsc` | Opens **Remote Desktop Connection**. |
| `SystemPropertiesRemote` | Opens **Remote Desktop / Remote Access** settings. |
| `services.msc` | Opens **Windows Services**. |
| `firewall.cpl` | Opens **Windows Defender Firewall** settings. |
| `eventvwr.msc` | Opens **Event Viewer**. |
| `devmgmt.msc` | Opens **Device Manager**. |
| `diskmgmt.msc` | Opens **Disk Management**. |
| `msinfo32` | Opens **System Information**. |
| `dxdiag` | Opens **DirectX Diagnostic Tool**. |
| `taskmgr` | Opens **Task Manager**. |
| `resmon` | Opens **Resource Monitor**. |
| `cleanmgr` | Opens **Disk Cleanup**. |

---

![Notes](https://img.shields.io/badge/Important%20Notes-FACC15?style=for-the-badge&logo=readme&logoColor=black)
![Admin Required](https://img.shields.io/badge/Admin-Required-EF4444?style=flat-square)
![Use Carefully](https://img.shields.io/badge/Use-Carefully-F97316?style=flat-square)
![Production Warning](https://img.shields.io/badge/Production-PC%20Warning-DC2626?style=flat-square)

## ⚠️ Notes

Some commands must be run as **Administrator**.

For example:

```cmd
sfc /scannow
DISM /Online /Cleanup-Image /RestoreHealth
chkdsk /f /r
gpupdate /force
netsh winsock reset
net user username password /add
net user username /delete
shutdown /r /o /f /t 0
```

Always make sure you understand the command before running it on a production computer.

---

![Repository Goal](https://img.shields.io/badge/Repository-Goal-22C55E?style=for-the-badge&logo=github&logoColor=white)
![Learning Project](https://img.shields.io/badge/Learning-Project-16A34A?style=flat-square)
![IT Portfolio](https://img.shields.io/badge/IT-Portfolio-15803D?style=flat-square)

## ✅ Repository Goal

The goal of this repository is to build a practical and easy-to-use command reference for:

- **IT Support Technicians**
- **Help Desk Analysts**
- **Desktop Support Technicians**
- **Entry-Level System Administrators**
- **Students preparing for IT support roles**

More commands and troubleshooting notes will be added over time.

---

![Future Additions](https://img.shields.io/badge/Future-Additions-A855F7?style=for-the-badge&logo=readme&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-Basics-7C3AED?style=flat-square)
![Active Directory](https://img.shields.io/badge/Active%20Directory-Commands-9333EA?style=flat-square)
![Microsoft 365](https://img.shields.io/badge/Microsoft%20365-Admin-6D28D9?style=flat-square)

## 📚 Future Additions

Planned future sections:

- **Active Directory commands**
- **PowerShell basics**
- **Microsoft 365 admin commands**
- **Windows security commands**
- **Printer troubleshooting commands**
- **Disk and storage commands**
- **Remote support commands**
- **Useful Linux commands for IT support**
- **Useful macOS commands for IT support**

---

![Updates](https://img.shields.io/badge/Contribution%20%2F%20Updates-0EA5E9?style=for-the-badge&logo=github&logoColor=white)
![Growing Reference](https://img.shields.io/badge/Growing-Reference-0284C7?style=flat-square)
![Documentation](https://img.shields.io/badge/Documentation-Practice-0369A1?style=flat-square)

## ⭐ Contribution / Updates

This is a personal learning and documentation project.

I will continue updating this reference as I practice more **IT Support**, **Windows troubleshooting**, and **system administration** tasks.
