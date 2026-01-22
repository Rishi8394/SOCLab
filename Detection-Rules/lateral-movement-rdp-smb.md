# Lateral Movement Detection via RDP and SMB

## Objective
Detect potential lateral movement by identifying abnormal RDP and SMB authentication patterns across multiple hosts.

---

## Threat Description
Attackers often move laterally using valid credentials via RDP or SMB to access additional systems after initial compromise.

---

## Data Sources
- Windows Security Logs (Event IDs 4624, 4625)
- Windows Logon Type 3 (SMB) and 10 (RDP)
- SIEM (Splunk)

---

## Detection Logic
- Identify a single user account authenticating to multiple hosts within a short time window
- Detect RDP or SMB logins from unusual source systems
- Flag authentication sequences inconsistent with baseline behavior

---

## MITRE ATT&CK
- T1021 – Remote Services
- T1078 – Valid Accounts

---

## SOC Investigation Steps
1. Identify source and destination hosts
2. Validate whether access was authorized
3. Review account privilege level
4. Check for associated process or PowerShell activity

---

## Response Actions
- Isolate affected systems if malicious
- Reset credentials for compromised accounts
- Increase monitoring on related hosts
