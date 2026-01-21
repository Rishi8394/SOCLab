# Incident Report: Brute Force Authentication Attempt

## Incident Summary
Multiple failed authentication attempts were detected against user accounts, indicating potential brute force or password spray activity.

---

## Incident Details
- **Incident Type:** Authentication Attack
- **Severity:** Medium
- **Status:** Contained
- **Detection Source:** SIEM (Splunk / Azure Sentinel)
- **Date Identified:** Simulated Lab Scenario

---

## Detection Overview
The incident was detected based on an abnormal number of failed login attempts within a short time window.  
The activity exceeded normal user behavior thresholds and triggered a SOC alert.

---

## Affected Assets
- User Accounts: Multiple
- Endpoint Systems: Windows 10 host(s)
- Cloud Identity: Azure AD (Entra ID)

---

## Investigation Timeline

1. Alert generated for repeated failed authentication attempts  
2. Analyst validated the alert and confirmed suspicious behavior  
3. Source IP and targeted accounts were identified  
4. Logs reviewed for any successful logins following failures  
5. No evidence of successful compromise identified  

---

## Indicators of Compromise (IOCs)
- Repeated failed login attempts
- Single source IP targeting multiple accounts
- Abnormal authentication frequency

---

## Root Cause Analysis
The activity was consistent with automated brute force or password spray techniques rather than normal user error.

---

## Containment Actions
- Source IP flagged for monitoring or blocking
- Affected user accounts monitored for further activity
- Authentication logs placed under increased observation

---

## Remediation & Recommendations
- Enforce Multi-Factor Authentication (MFA)
- Implement account lockout policies
- Tune SIEM detection thresholds
- Conduct user awareness reminders on password security

---

## Lessons Learned
- Early detection prevented account compromise
- Correlating authentication logs improves SOC visibility
- Continuous tuning is required to reduce false positives
