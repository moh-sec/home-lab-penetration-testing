# 🌐 Network Topology

## Purpose
This section describes the network layout used in the home lab and how the attacker machine communicates with the target machine.

---

## 🧱 Lab Network Design
- Linux virtual machine configured as the attacker
- Windows 11 virtual machine configured as the target
- Both machines are connected to the same isolated virtual network

---

## 🌍 Network Details
- Network Type: Bridged 
- Subnet: 192.168.1.0/24
- Gateway: Not required

---

## 🔁 Communication Flow
- Linux attacker initiates communication with Windows target
- ICMP traffic is allowed for connectivity testing
- TCP traffic is allowed for service enumeration

---

## 📌 Notes
- The network is intentionally flat to simplify testing
- No network segmentation is implemented at this stage
- The environment is isolated 
