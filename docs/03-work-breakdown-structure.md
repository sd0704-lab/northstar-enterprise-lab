## 03 – Work Breakdown Structure (WBS)
Northstar Precision Manufacturing (NPM) – Enterprise Cyber Defense Lab

## 1. Purpose
This Work Breakdown Structure (WBS) defines the hierarchical decomposition of all project work required to complete the Northstar Precision Manufacturing (NPM) Enterprise Cyber Defense Lab.
The WBS establishes a controlled execution baseline aligned with the Project Charter and Scope documents.

## 2. WBS Overview
### 1.0 Project Governance
1.1 Project Charter Development
1.2 Scope and Objectives Definition
1.3 Stakeholder Register Creation
1.4 Work Breakdown Structure Development
1.5 Risk Register Development
1.6 Schedule and Milestone Planning
1.7 Communication Plan Development
1.8 Change Management Log Maintenance
### 2.0 Core Infrastructure Deployment (Phase 1)
2.1 Hypervisor Deployment
* 2.1.1 Install Proxmox VE
* 2.1.2 Configure host networking
* 2.1.3 Configure storage
2.2 Firewall Implementation
* 2.2.1 Deploy pfSense VM
* 2.2.2 Configure WAN/LAN interfaces
* 2.2.3 Configure DHCP services
* 2.2.4 Establish baseline firewall rules
2.3 Active Directory Deployment
* 2.3.1 Install Windows Server
* 2.3.2 Promote to Domain Controller (AD DS + DNS)
* 2.3.3 Configure DNS
* 2.3.4 Create OU structure
* 2.3.5 Implement RBAC model
2.4 Endpoint Deployment
* 2.4.1 Install Windows 10 client
* 2.4.2 Install Windows 11 client
* 2.4.3 Join systems to domain
* 2.4.4 Validate Group Policy application
### 3.0 Security Hardening
3.1 Baseline GPO Configuration
* 3.1.1 Enforce password complexity
* 3.1.2 Configure account lockout policy
* 3.1.3 Disable guest account
* 3.1.4 Apply workstation baseline policies
3.2 Access Control Implementation
* 3.2.1 Create security groups
* 3.2.2 Assign NTFS permissions
* 3.2.3 Validate least privilege enforcement
### 4.0 Monitoring & Detection Engineering (Phase 3)
4.1 SIEM Deployment
* 4.1.1 Deploy Ubuntu Server VM
* 4.1.2 Install and configure Wazuh
* 4.1.3 Configure agent deployment
* 4.1.4 Validate log ingestion
4.2 Network Monitoring Deployment
* 4.2.1 Deploy Security Onion VM
* 4.2.2 Configure network monitoring interfaces
* 4.2.3 Validate traffic capture
4.3 Detection Engineering
* 4.3.1 Identify priority MITRE ATT&CK techniques
* 4.3.2 Develop detection use cases
* 4.3.3 Execute controlled attack simulations
* 4.3.4 Validate detection accuracy
### 5.0 Adversary Simulation
5.1 Deploy Kali Linux / Kali Purple (External Platform)
5.2 Conduct authentication attack simulations
5.3 Conduct privilege escalation simulations
5.4 Conduct lateral movement simulations
5.5 Document findings and response validation
### 6.0 Architecture Enhancement (Future Phase Consideration)
6.1 VLAN Segmentation Design
6.2 VLAN Implementation and Firewall Policy Enforcement
6.3 DHCP Migration to Windows Server (Optional Enhancement)
6.4 Network Boundary Refinement
### 7.0 Final Documentation & Capstone Delivery
7.1 Update Architecture Design Documentation
7.2 Finalize Risk Register
7.3 Update Change Log
7.4 Prepare Capstone Report
7.5 Prepare Presentation Materials

## 3. WBS Dictionary (High-Level)
Each WBS element represents a defined deliverable or work package.
Work packages at the lowest level are considered measurable completion points and may be tracked for milestone validation.

## 4. WBS Control Baseline
Completion of Section 1.0 (Project Governance) establishes the formal execution baseline for the NPM project.
All future scope adjustments must be documented in the Change Management Log (Document 11).
