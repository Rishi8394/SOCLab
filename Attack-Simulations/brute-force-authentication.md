# Attack Simulation: Brute Force Authentication

## Objective
Simulate a brute force or password spray authentication attack to understand attacker behavior and validate SOC detection and response workflows.

---

## Attack Scenario Overview
An attacker attempts multiple authentication attempts against user accounts to gain unauthorized access.  
This simulation focuses on generating observable authentication failures rather than successful compromise.

---

## Attacker Perspective
- Target: User authentication mechanisms
- Technique: Repeated login attempts using common or guessed passwords
- Goal: Identify weak credentials or unprotected accounts

---

## Environment
- Attacker System: Parrot OS
- Target System: Windows 10 endpoint
- Cloud Identity: Azure AD (Entra ID)
- Monitoring: Splunk SIEM and Microsoft Sentinel

---

## Simulation Methodology

### On-Prem Authentication Attempts
- Multiple failed login attempts were generated against a Windows endpoint
- Authentication failures produced Windows Security Event logs
- No successful authentication was performed

### Cloud Authentication Attempts
- Simulated failed sign-in behavior aligned with Azure AD risky sign-in scenarios
- Focused on understanding log patterns rather than exploiting live cloud services

---

## Observed Artifacts
- Repeated failed authentication events
- Consistent source identifiers across attempts
- Increased authentication frequency within short time windows

---

## SOC Visibility
- Authentication failures ingested into SIEM platforms
- Detection rules triggered based on abnormal patterns
- Alerts escalated for analyst investigation

---

## Defensive Outcome
- Attack activity identified early
- No account compromise occurred
- Detection and response controls validated

---

## Notes
This simulation is designed for defensive validation purposes.  
The emphasis is on detection logic, investigation workflow, and response readiness rather than offensive exploitation.
