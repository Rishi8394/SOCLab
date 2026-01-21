# Brute Force Authentication Detection

## Objective
Detect repeated failed authentication attempts that may indicate brute force or password spray activity against user accounts.

---

## Threat Description
Attackers attempt multiple login attempts using different passwords or accounts to gain unauthorized access.  
This activity is commonly observed in both on-premise environments and cloud identity platforms.

---

## Data Sources
- Windows Security Event Logs (Event ID 4625)
- Azure AD (Entra ID) Sign-In Logs

---

## Detection Logic

### On-Prem (Windows)
Identify multiple failed login attempts from the same source within a short time window.

**Example Logic:**
- Count failed logins per source IP and user
- Trigger alert when threshold is exceeded

---

### Cloud (Azure AD)
Detect repeated failed sign-ins or password spray behavior across multiple accounts.

**Indicators:**
- Multiple failures from same IP
- Multiple users targeted in short duration
- Unfamiliar location or device

---

## MITRE ATT&CK Mapping
- **T1110** – Brute Force  
- **T1078** – Valid Accounts

---

## SOC Investigation Steps
1. Validate alert and confirm failure pattern
2. Identify affected accounts
3. Review source IP reputation
4. Check for successful logins following failures
5. Determine if activity is malicious or user error

---

## Response & Mitigation
- Temporarily block source IP (if applicable)
- Force password reset for affected accounts
- Enforce or validate MFA
- Monitor account activity post-incident

---

## Notes
Thresholds and logic should be tuned to reduce false positives based on environment behavior and business context.
