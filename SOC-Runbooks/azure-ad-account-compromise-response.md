# SOC Runbook: Azure AD Account Compromise Response

## Trigger
Risky sign-in or anomalous authentication alert in Microsoft Sentinel.

---

## Investigation Steps
1. Review sign-in risk and location
2. Confirm user activity legitimacy
3. Check recent account changes

---

## Containment Actions
- Reset user credentials
- Revoke sessions
- Enforce MFA

---

## Escalation Criteria
- Privileged accounts involved
- Repeated compromise attempts
- Multiple users affected

---

## Post-Incident Actions
- Update detection rules
- Review identity security policies
- Document incident findings
