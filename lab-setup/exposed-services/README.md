# Exposed Services

## Overview
This repository documents the network services that were intentionally exposed on a Windows target machine.  
The goal of this setup is to provide a realistic yet controlled attack surface for security testing and hands-on practice.

---

## Purpose
The exposed services are part of a lab environment created for:
- Service enumeration
- Reconnaissance practice
- Understanding common Windows attack surfaces

No real-world or production systems are involved in this environment.

---

## Exposed Services

### HTTP (Port 80)
- **Service:** Microsoft IIS  
- **Description:**  
  The Microsoft IIS web server was enabled to expose a reachable web endpoint.  
  This allows testers to perform basic enumeration, banner grabbing, and web-based reconnaissance during security testing.

---

## Verification
The exposed service was verified using the following methods:
- Local confirmation on the Windows target machine to ensure the service was running correctly.
- Remote discovery from the attacker machine using Nmap, confirming that the service was accessible externally.

---

## Notes
- All services listed in this repository were exposed intentionally for lab and training purposes.
- The environment is fully isolated and does not impact any production systems.
- The configuration may be modified or expanded during later testing stages.

---

## Disclaimer
This repository is intended for educational and security testing purposes only.  
Any techniques practiced using this setup should be performed responsibly and only on systems you own or have explicit permission to test.
