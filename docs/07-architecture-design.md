## 07 – Architecture Design
Northstar Precision Manufacturing (NPM) – Enterprise Cyber Defense Lab

## 7.1 Architecture Overview
### Summary
The Northstar Precision Manufacturing (NPM) Enterprise Cyber Defense Lab is a simulated mid-sized enterprise environment designed to model real-world corporate infrastructure supporting:
* Identity and access management
* Network segmentation and firewall policy enforcement
* Centralized logging and monitoring
* Incident response exercises
* Purple team adversary simulation
The environment is fully virtualized and governed under structured project management documentation.
### High-Level Components
* **Proxmox VE (NST-HV01)**
  Virtualization platform hosting all core lab virtual machines.
* **pfSense (NST-FW01)**
  Firewall and routing platform providing WAN/LAN segmentation, DHCP services, and internal lab traffic control.
* **Windows Server 2025 Datacenter (NST-DC01)**
  Active Directory Domain Services (AD DS) with integrated DNS.
* **Windows 10/11 Clients (NST-OFFICE01 / NST-OFFICE02)**
  Domain-joined workstations used for policy enforcement and endpoint testing.
* **Wazuh (NST-SIEM01)**
  Centralized security logging and host-based monitoring platform.
* **Security Onion (NST-NDR01)**
  Network detection and response (NDR) platform for packet analysis and intrusion monitoring.
* **Kali Linux / Kali Purple (Attack Platform)**
  External adversary simulation environment hosted on a separate VMware platform. Used for controlled attack execution, validation of detections, and purple team testing against the lab infrastructure.

## 7.2 Network Design
### Logical Network Segmentation
The lab environment is logically segmented to simulate enterprise security boundaries.
**Primary LAN Segment**
* Internal lab subnet: 192.168.10.0/24
* Routed through pfSense firewall
### Traffic Flow Model
* Workstations authenticate to Domain Controller
* DC provides DNS and directory services
* Endpoints and servers forward logs to Wazuh
* Network traffic monitored by Security Onion
* Controlled attack simulations originate from Kali platform
### Security Boundary Principles
* Firewall controls inter-network routing
* No exposure to production/home systems
* Segmentation maintained at the virtual switch and firewall level

## 7.3 Virtual Machine Inventory
| Hostname     | Role              | Operating System      | Function                  |
| ------------ | ----------------- | --------------------- | ------------------------- |
| NST-HV01     | Hypervisor        | Proxmox VE            | VM hosting platform       |
| NST-FW01     | Firewall          | pfSense               | Routing & firewall policy |
| NST-DC01     | Domain Controller | Windows Server 2025   | AD DS + DNS               |
| NST-OFFICE01 | Workstation       | Windows 11            | Domain client             |
| NST-OFFICE02 | Workstation       | Windows 10            | Domain client             |
| NST-SIEM01   | SIEM              | Ubuntu Server + Wazuh | Log aggregation           |
| NST-NDR01    | Monitoring        | Security Onion        | Network monitoring        |

## 7.4 Identity & Access Architecture
### Directory Services
Active Directory Domain Services provides:
* Centralized authentication
* Organizational Unit (OU) structure
* Role-Based Access Control (RBAC)
* Group Policy enforcement
### DNS Integration
DNS is integrated with Active Directory to support:
* Domain controller location (SRV records)
* Kerberos authentication
* Domain join operations
### Access Model
Access control follows:
**Accounts → Security Groups → Resource Permissions**
This model enforces least privilege and supports role-based delegation.

## 7.5 Logging & Monitoring Architecture
### Log Collection
* Windows endpoints forward logs to Wazuh
* Server logs centrally aggregated
* Security Onion monitors network traffic
### Monitoring Objectives
* Detect authentication anomalies
* Monitor privilege escalation attempts
* Capture lateral movement behavior
* Map detections to MITRE ATT&CK techniques

## 7.6 Design Principles
### Isolation
Lab traffic is logically separated from the residential network environment.
### Minimal Complexity
Only components necessary to support coursework and capstone objectives are deployed.
### Documentation-First Approach
All infrastructure modifications are documented within `/docs` and tracked in the Change Log (Document 11).
### Enterprise Simulation
Design decisions reflect a mid-sized enterprise security model rather than a basic home lab configuration.

## 7.7 Planned Network Segmentation (Target State)
## Objective
To enhance internal network security through logical segmentation using VLANs and firewall policy enforcement.
## Proposed VLAN Structure
* 10	SERVERS	Domain Controller, SIEM, Monitoring systems
* 20	USERS	Windows client endpoints
* 30	SECURITY	Monitoring and detection platforms
* 40	MANAGEMENT	Hypervisor and firewall management interfaces
## Security Benefits
* Reduces lateral movement capability
* Enforces least-privilege network access
* Enables firewall rule granularity
* Improves detection engineering realism
## Current Status
VLAN implementation is planned for Phase 2 of the project and is not currently active in the production lab environment.
