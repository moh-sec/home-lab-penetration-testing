## Summary of Findings

### Exposed Services
The following services were identified on the Windows 11 target system:

- **HTTP (80/tcp)**  
  Microsoft IIS 10.0 web server is exposed.  
  This service represents the primary attack surface and may be susceptible to
  web-based vulnerabilities or misconfigurations depending on the hosted content.

- **MSRPC (135/tcp)**  
  Standard Windows RPC service required for system operations.
  No immediate security issues identified.

- **NetBIOS (139/tcp)**  
  Legacy NetBIOS service detected, typically associated with SMB communication.
  May increase the attack surface for enumeration.

- **SMB (445/tcp)**  
  SMB service is accessible but requires authentication.
  No anonymous access or misconfigured shares were identified during testing.

### Security Observations
- The system exposes only standard Windows services.
- No critical vulnerabilities were discovered during initial assessment.
- Authentication mechanisms appear to be properly enforced.
- Windows 11 shows a hardened default configuration.

### Risk Assessment
Overall risk level: **Low**

### Notes
The lack of exploitable vulnerabilities emphasizes the importance of enumeration,
misconfiguration analysis, and credential-based attacks in modern Windows environments.
