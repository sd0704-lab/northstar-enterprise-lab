# Northstar Precision Manufacturing
Enterprise Infrastructure Lab

## Phase 1 – Core Infrastructure

- Proxmox Hypervisor (NST-HV01)
- pfSense Firewall (FW-PFSENSE01)
- Domain Controller (NST-DC01)
- Windows 11 Client (NST-OFFICE01)
- Internal LAN: 192.168.10.0/24

## Active Directory Structure

OUs:
- NPM-Users
- NPM-Groups
- NPM-Servers
- NPM-Workstations

Departments:
- HR
- Engineering
- IT
- Management

## Security Model

Accounts → Security Groups → NTFS Permissions

Baseline GPO:
- Password complexity enabled
- Minimum 12 characters
- Account lockout at 5 attempts
- Guest account disabled

