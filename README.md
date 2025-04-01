# CVE Request: Insufficient Session Expiration in Nagios Network Analyzer  

## Overview  
A **session management issue** in **Nagios Network Analyzer 2024R1.0.3** allows user sessions to remain valid after logout, enabling potential unauthorized access. This vulnerability falls under **Identification and Authentication Failures** and can lead to **account hijacking** and **unauthorized actions**.  

## Affected Product  
- **Product:** Nagios Network Analyzer  
- **Version:** 2024R1.0.3  
- **Vulnerability Type:** Insufficient Session Expiration  

## Impact  
- **Unauthorized Access:** Attackers can reuse session tokens after logout to access sensitive data.  
- **Account Hijacking:** Malicious users may perform actions on behalf of legitimate users.  
- **Reputation Damage:** Security breaches due to improper session handling can reduce user trust.  

## CVSS Score  
- **CVSS v3.0:** `CVSS:3.0/AV:A/AC:L/PR:L/UI:N/S:U/C:L/I:L/A:N`  
- **Severity:** Low  

## Root Cause  
The application fails to properly invalidate session tokens after logout, allowing session reuse beyond the expected expiration period.  

## Resolution Status  
- **Changelog Reference:** [Nagios Changelog](https://www.nagios.com/changelog/#network-analyzer)  

## Disclosure Timeline  
- **January 10, 2025:** Vulnerability acknowledged by Nagios.  
- **January 21, 2025:** Fix released.  
- **February 4, 2025:** Public disclosure permitted.  

## References  
- [MITRE CVE Entry] (https://www.cve.org/CVERecord?id=CVE-2025-28132) 
- [Nagios Changelog](https://www.nagios.com/changelog/#network-analyzer)  

## Suggested Remediation  
1. **Session Invalidation on Logout:** Ensure session tokens are invalidated upon user logout.  
2. **Short Session Timeout:** Implement automatic session expiration after a period of inactivity.  

## Credits  
- **Discovered by:** Harshal Tembhurne  

## Note  
This repository is created solely for providing the necessary details for vulnerability tracking while adhering to responsible disclosure practices.  
