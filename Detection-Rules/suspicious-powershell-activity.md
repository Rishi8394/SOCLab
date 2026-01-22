# Suspicious PowerShell Activity Detection

## Objective
Detect potentially malicious PowerShell execution commonly associated with post-exploitation and lateral movement.

---

## Threat Description
PowerShell is frequently abused by attackers to execute encoded commands, download payloads, or perform system discovery while bypassing traditional security controls.

---

## Data Sources
- Windows Security Logs
- Sysmon Event Logs
- SIEM (Splunk)

---

## Detection Logic
- Monitor PowerShell process execution
- Identify encoded or obfuscated command usage
- Flag execution from non-standard parent processes

---

## MITRE ATT&CK
- T1059.001 – PowerShell
- T1027 – Obfuscated Files or Information

---

## SOC Investigation Steps
1. Validate PowerShell execution context
2. Review command-line arguments
3. Identify parent and child processes
4. Check for network connections or file creation
5. Assess whether activity aligns with normal administration

---

## Response Actions
- Isolate affected endpoint if malicious
- Block suspicious scripts or command patterns
- Reset credentials if compromise is suspected
- Update detection logic as needed
