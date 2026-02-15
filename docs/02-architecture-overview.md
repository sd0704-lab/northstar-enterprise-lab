# Architecture Overview

## Summary
This repository documents the Northstar Precision Manufacturing (NPM) Enterprise Cyber Defense Lab. The lab is a simulated enterprise environment designed to support blue team operations, incident response exercises, and purple team testing.

## High-Level Components
- **Proxmox VE (NST-HV01):** Virtualization host running core lab VMs
- **pfSense (NST-FW01):** Firewall/router providing WAN/LAN separation and lab routing
- **Windows Server 2025 Datacenter (NST-DC01):** Active Directory Domain Services (AD DS) and DNS
- **Windows 10/11 Clients (NST-OFFICE01/NST-OFFICE02):** Domain-joined endpoints for policy/testing
- **Wazuh (Ubuntu Server) (NST-SIEM01):** Centralized security logging/SIEM
- **Security Onion (NST-NDR01):** Network security monitoring platform
- **Kali Linux / Kali Purple:** Attack simulation and validation platform (laptop)

## Design Principles
- **Isolation:** Lab traffic separated from home network where possible
- **Least complexity:** Only build what supports coursework and capstone requirements
- **Documentation-first:** Each change is captured in /docs and tracked in the change log
