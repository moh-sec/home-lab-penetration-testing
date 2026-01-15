# Windows 11 – Initial Security Assessment

## Description
This repository contains the results of an initial security assessment performed against a Windows 11 system.  
The goal of this assessment was to identify externally exposed services, review their configurations, and highlight any obvious security concerns.

>  Note: This was a **non-intrusive, unauthenticated assessment**. No exploitation or credential-based attacks were performed.

---

## Scope
- Network service discovery
- Basic service enumeration
- High-level configuration review

Out of scope:
- Credential-based attacks
- Deep vulnerability exploitation
- Application logic testing

---

## Identified Exposed Services

### HTTP – Port 80
- **Service:** Microsoft IIS 10.0  
- **Findings:**  
  The web service is running on port 80 and responds as expected. No obvious misconfigurations or publicly exploitable issues were observed during the initial review.
- **Comments:**  
  Since this service represents the primary external attack surface, it should be considered a high-priority target for deeper application-level testing.

---

### MSRPC – Port 135
- **Service:** Microsoft RPC  
- **Findings:**  
  The service is accessible and behaves normally for a Windows-based system.
- **Comments:**  
  No immediate security risks were identified during this phase.

---

### NetBIOS – Port 139
- **Service:** NetBIOS over TCP/IP  
- **Findings:**  
  NetBIOS services were detected, which is common in Windows environments.
- **Comments:**  
  While no exploitation was attempted, exposure of this service could allow additional enumeration and should be reviewed to ensure it is necessary.

---

### SMB – Port 445
- **Service:** Server Message Block (SMB)  
- **Findings:**  
  The service responds to authentication requests. Anonymous access is disabled, and no publicly accessible shares were identified.
- **Comments:**  
  Authentication controls appear to be properly enforced.

---

## Security Observations
- Only default Windows services were externally exposed.
- No critical or high-severity vulnerabilities were identified during this assessment.
- SMB authentication controls are correctly configured.
- The system appears to be reasonably hardened for a default Windows 11 installation.

---

## Risk Assessment
**Overall Risk Level:** Low  

The limited attack surface reduces immediate risk. However, further progress would likely depend on:
- Deeper service and application enumeration
- Identification of subtle misconfigurations
- Access to valid user credentials

---

## Recommendations
1. Perform deeper application-level testing on the IIS-hosted web application.
2. Review the necessity of exposing NetBIOS and SMB services externally.
3. Ensure the system remains fully patched and actively monitor logs for suspicious activity.

---

## Disclaimer
This assessment represents a point-in-time snapshot based on limited testing.  
Security posture may change as new vulnerabilities are discovered or system configurations are modified.
