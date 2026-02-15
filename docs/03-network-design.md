# Network Design

## Overview
The lab network is implemented behind a home router. pfSense provides firewalling and routing for the internal lab subnet.

## Home Network (Upstream)
- **Home Router:** Netgear Nighthawk
- **Upstream Subnet:** 192.168.1.0/24 (typical)
- **pfSense WAN:** Receives an address from the home router (DHCP or static)

## Lab Network (Internal)
- **pfSense LAN:** 192.168.10.1
- **Lab Subnet:** 192.168.10.0/24

## Notes
- Remote access VPN was evaluated and deferred to reduce scope and attack surface.
- Future segmentation (VLANs) may be implemented during networking coursework if required.

## Planned Future VLANs (Roadmap)
- VLAN10 - Servers
- VLAN20 - Workstations
- VLAN30 - Security Tools
