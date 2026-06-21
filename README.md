# IT Support Master Command Reference

Essential Windows commands every IT Support technician should know.

This repository is a growing command reference for IT Support, Help Desk, Desktop Support, and Windows troubleshooting tasks.

---

## System Performance & Maintenance

Use these commands when the PC is slow, freezing, acting up, or needs cleanup.

| Command | Action |
|---|---|
| %temp% | Opens the current user's temporary files folder for cleanup. |
| temp | Opens the Windows system temporary files folder. |
| prefetch | Opens the Prefetch folder. Cleaning this may help with some boot or application issues. |
| taskmgr | Opens Task Manager immediately. |
| resmon | Opens Resource Monitor for detailed CPU, memory, disk, and network usage tracking. |
| cleanmgr | Runs Disk Cleanup to remove system junk files and old Windows update files. |
| sfc /scannow | Runs System File Checker to scan and repair corrupted Windows system files. |
| DISM /Online /Cleanup-Image /RestoreHealth | Repairs the Windows system image. This is commonly used when SFC cannot fix the issue. |
| powercfg /h off | Disables Hibernation and can free up several gigabytes of disk space. |

---

## Network Troubleshooting

Use these commands when the internet is down, DNS is not working, or connectivity is unstable.

| Command | Action |
|---|---|
| ipconfig /all | Displays all network adapter details, including MAC address, DNS, DHCP, IP address, and gateway. |
| ipconfig /release | Releases the current IP address from the network adapter. |
| ipconfig /renew | Requests a new IP address from the DHCP server. |
| ipconfig /flushdns | Clears the DNS cache. This can help fix “site not found” or DNS resolution issues. |
| ping -t [IP/URL] | Runs a continuous ping to check for intermittent connection drops. |
| tracert [IP/URL] | Shows the path that network traffic takes to reach a destination. |
| netstat -an | Lists active network connections and listening ports. |
| nslookup [URL] | Checks whether DNS is correctly resolving a domain name. |
| netsh winsock reset | Resets the Windows network stack. Useful when network settings are corrupted or connectivity issues persist. |
| ncpa.cpl | Opens Network Connections, where you can enable/disable adapters, check adapter status, and configure IPv4/IPv6 settings. |

---

## System Administration & Diagnostics

Use these commands for Windows diagnostics, hardware checks, device management, logs, and system information.

| Command | Action |
|---|---|
| msinfo32 | Opens System Information and displays a full system summary, including hardware, components, and software environment. |
| eventvwr.msc | Opens Event Viewer to check system, application, security, and crash logs. |
| devmgmt.msc | Opens Device Manager to troubleshoot drivers, hardware devices, and unknown devices. |
| diskmgmt.msc | Opens Disk Management for formatting, partitioning, and checking drives. |
| chkdsk /f /r | Scans the hard drive for file system errors, physical errors, and bad sectors. |
| gpupdate /force | Forces an immediate Group Policy update. Useful after domain or policy changes. |
| wmic bios get serialnumber | Shows the PC serial number or service tag. Useful for inventory and warranty checks. |
| dxdiag | Opens DirectX Diagnostic Tool to check display, sound, and system information. |
| systeminfo \| findstr /B /C:"Domain" | Shows the domain or workgroup that the computer belongs to. Useful for checking if a PC is joined to a domain. |
| services.msc | Opens Windows Services to start, stop, restart, or check the status of system services. |
| firewall.cpl | Opens Windows Defender Firewall settings. Useful for checking firewall status and allowed apps. |

---

## Remote Desktop & Remote Access

Use these commands when troubleshooting RDP or remote access.

| Command | Action |
|---|---|
| mstsc | Opens Remote Desktop Connection. Used to connect to another Windows computer or server through RDP. |
| SystemPropertiesRemote | Opens Remote System Properties. Used to enable Remote Desktop and check remote access settings. |
| shutdown /r /o /f /t 0 | Restarts the computer immediately and opens Advanced Startup Options. Useful for recovery, Safe Mode, Startup Repair, and troubleshooting boot issues. |

---

## User Account Management

Use these commands when creating, deleting, or managing local Windows users.

| Command | Action |
|---|---|
| net user testuser password /add | Creates a new local user named testuser with the password “password”. Replace the username and password with your own values. |
| net user testuser /delete | Deletes the local user account named testuser. Use carefully because this removes the account from the computer. |

Example:

net user john P@ssword123 /add

This creates a local user named john with the password P@ssword123.

---

## Printers & Devices

Use these commands when troubleshooting printers or connected devices.

| Command | Action |
|---|---|
| control printers | Opens Devices and Printers. Useful for checking installed printers, setting the default printer, removing old printers, and troubleshooting print issues. |

---

## Professional Power User Shortcuts

Useful Windows keyboard shortcuts for faster IT support work.

| Shortcut | Action |
|---|---|
| Win + X | Opens the Power User Menu. Provides quick access to Admin Terminal, Device Manager, Disk Management, Network Connections, and more. |
| Ctrl + Shift + Esc | Opens Task Manager directly. |
| Win + L | Locks the workstation immediately. |
| Win + Shift + S | Opens the Windows snipping tool for screenshots. |
| Win + R | Opens the Run dialog box. You can type many commands from this reference here. |

---

## Common Run Commands

These commands are commonly opened by pressing Win + R first, then typing the command.

| Run Command | Action |
|---|---|
| control printers | Opens Devices and Printers. |
| ncpa.cpl | Opens Network Connections. |
| mstsc | Opens Remote Desktop Connection. |
| SystemPropertiesRemote | Opens Remote Desktop / Remote Access settings. |
| services.msc | Opens Windows Services. |
| firewall.cpl | Opens Windows Defender Firewall settings. |
| eventvwr.msc | Opens Event Viewer. |
| devmgmt.msc | Opens Device Manager. |
| diskmgmt.msc | Opens Disk Management. |
| msinfo32 | Opens System Information. |
| dxdiag | Opens DirectX Diagnostic Tool. |
| taskmgr | Opens Task Manager. |
| resmon | Opens Resource Monitor. |
| cleanmgr | Opens Disk Cleanup. |

---

## Notes

Some commands must be run as Administrator.

For example:

sfc /scannow
DISM /Online /Cleanup-Image /RestoreHealth
chkdsk /f /r
gpupdate /force
netsh winsock reset
net user username password /add
net user username /delete
shutdown /r /o /f /t 0

Always make sure you understand the command before running it on a production computer.
