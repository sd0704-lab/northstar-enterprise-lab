# Virtual Machine Inventory

## Proxmox Host
- **Host Name:** NST-HV01
- **Role:** Hypervisor running lab VMs

## Core VMs (Proxmox)

### pfSense (NST-FW01)
- **Role:** Firewall/Router
- **Interfaces:** WAN (vtnet0), LAN (vtnet1)
- **LAN IP:** 192.168.10.1

### Windows Server 2025 Datacenter (NST-DC01)
- **Role:** Domain Controller
- **Services:** AD DS, DNS, File Services

### Windows 11 (NST-OFFICE01)
- **Role:** Domain-joined workstation

### Windows 10 (NST-OFFICE02)
- **Role:** Domain-joined workstation

### Wazuh (Ubuntu Server) (NST-SEIM01)
- **Role:** SIEM / Centralized logging

### Security Onion (NST-NDR01)
- **Role:** Network security monitoring

## External / Non-VM Systems

### Kali Linux / Kali Purple (Laptop)
- **Role:** Attack simulation and validation platform
