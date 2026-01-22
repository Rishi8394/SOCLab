# Azure Resource Abuse Detection

## Objective
Detect anomalous Azure resource activity that may indicate cloud account abuse or compromise.

---

## Threat Description
Compromised cloud accounts may be used to create unauthorized resources, perform crypto-mining, or abuse subscriptions.

---

## Data Sources
- Azure Activity Logs
- Defender for Cloud alerts
- Microsoft Sentinel

---

## Detection Logic
- Monitor unexpected VM creation
- Detect abnormal resource provisioning frequency
- Identify resource creation outside business hours

---

## MITRE ATT&CK
- T1078 – Valid Accounts
- T1496 – Resource Hijacking

---

## SOC Investigation Steps
1. Identify newly created resources
2. Validate owner and purpose
3. Review authentication and role assignments
4. Assess cost and security impact

---

## Response Actions
- Disable affected accounts
- Remove unauthorized resources
- Apply stricter RBAC controls
