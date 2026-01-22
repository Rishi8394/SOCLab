# SOC Runbook: Lateral Movement and Privilege Abuse Response

## Trigger
Alerts indicating abnormal RDP or SMB access combined with privileged account activity.

---

## Initial Triage
1. Identify affected hosts and accounts
2. Confirm use of RDP (Logon Type 10) or SMB (Logon Type 3)
3. Determine if privileged accounts are involved

---

## Investigation Steps
1. Review authentication sequence across hosts
2. Validate account authorization and role
3. Correlate with process or PowerShell activity
4. Assess potential impact scope

---

## Containment Actions
- Isolate affected systems
- Reset compromised credentials
- Temporarily restrict privileged access

---

## Escalation Criteria
- Domain or global admin accounts involved
- Multiple systems affected
- Evidence of persistence

---

## Post-Incident Actions
- Review lateral movement detections
- Improve authentication monitoring
- Document lessons learned
