# Network Topology

## Purpose
This section outlines the network layout used in the lab environment and explains how the attacker machine communicates with the target system.

---

## Lab Network Design
- A Linux virtual machine configured as the attacker
- A Windows 11 virtual machine configured as the target
- Both machines are connected to the same isolated virtual network

---

## Network Details
- Network type: Bridged
- Subnet: 192.168.1.0/24
- Gateway: Not required for this setup

---

## Communication Flow
- The Linux attacker initiates communication with the Windows target
- ICMP traffic is permitted for connectivity testing
- TCP traffic is allowed for service enumeration

---

## Notes
- The network is intentionally flat to keep testing simple
- No network segmentation is implemented at this stage
- The lab environment is isolated from production networks
