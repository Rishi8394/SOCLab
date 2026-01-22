# Suspicious Service or Scheduled Task Creation

## Objective
Detect persistence mechanisms through unauthorized service or scheduled task creation.

---

## Threat Description
Attackers establish persistence by creating services or scheduled tasks that execute malicious binaries or scripts.

---

## Data Sources
- Windows Security Logs
- Sysmon (Service and Task creation events)
- SIEM (Splunk)

---

## Detection Logic
- Monitor new service creation events
- Detect scheduled tasks created outside standard administrative workflows
- Flag services executing from non-standard directories

---

## MITRE ATT&CK
- T1543 – Create or Modify System Process
- T1053 – Scheduled Task

---

## SOC Investigation Steps
1. Identify created service or task
2. Review execution path and command
3. Validate business justification
4. Check for related malware or PowerShell activity

---

## Response Actions
- Disable malicious service or task
- Remove persistence mechanism
- Scan affected system for compromise
