# Incident Report: Azure AD Account Compromise

## Incident Summary
Suspicious sign-in activity was detected for a cloud user account, indicating a potential account compromise.

---

## Incident Details
- Incident Type: Cloud Identity Compromise
- Severity: Medium
- Detection Source: Microsoft Sentinel
- Affected Service: Azure AD (Entra ID)

---

## Detection Overview
The incident was triggered by a risky sign-in alert combined with anomalous login behavior.

---

## Investigation
- Reviewed sign-in logs and risk indicators
- Identified unfamiliar login location
- No evidence of successful privilege escalation found

---

## Containment
- User password reset
- Active sessions revoked
- MFA enforced

---

## Lessons Learned
- Identity monitoring is critical in cloud environments
- MFA significantly reduces account compromise risk
