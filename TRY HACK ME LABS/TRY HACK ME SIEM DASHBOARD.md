# TryHackMe SIEM Dashboard — Suspicious IP & Brute-Force Investigation

## 1. Lab Overview

| Field | Details |
|---|---|
| **Platform** | TryHackMe |
| **Lab Type** | SIEM Monitoring and Incident Investigation |
| **Focus Area** | Suspicious IP and Brute-Force Detection |
| **Difficulty** | Beginner / Intermediate |
| **Status** | Completed |
| **Primary Tasks** | Log analysis, IP investigation, threat detection, IP blocking, and incident reporting |

## 2. Objective

The objective of this practical exercise was to use a SIEM dashboard to monitor security events, identify suspicious IP addresses, investigate abnormal login attempts, and detect potential brute-force activity.

The investigation involved analyzing authentication logs, identifying suspicious source IPs, examining repeated failed login attempts, blocking the malicious IP address, and preparing an incident report.

## 3. Tools and Technologies

- **TryHackMe:** Hands-on cybersecurity training environment.
- **SIEM Dashboard:** Centralized monitoring and analysis of security events.
- **Authentication Logs:** Records of successful and failed login attempts.
- **IP Investigation:** Analysis of suspicious source IP addresses.
- **Security Monitoring:** Detection and investigation of suspicious activity.

## 4. Investigation Workflow

### Step 1: SIEM Dashboard Monitoring

Accessed the SIEM dashboard to review incoming security events and monitor authentication activity.

Focused on:

- Failed login attempts
- Successful login events
- Suspicious source IP addresses
- Repeated authentication failures
- Unusual login patterns
- Security alerts and event timestamps

### Step 2: Suspicious IP Identification

Reviewed authentication logs to identify source IP addresses associated with unusual login activity.

Investigated IP addresses based on:

- Frequency of failed login attempts
- Repeated authentication requests
- Multiple login attempts against an account
- Unusual login patterns
- Related security alerts

### Step 3: Login Attempt Analysis

Analyzed authentication events to distinguish between successful and failed login attempts.

The investigation focused on:

- Identifying targeted user accounts
- Reviewing timestamps of login attempts
- Comparing failed and successful authentication events
- Identifying repeated attempts from the same source IP
- Checking for suspicious login patterns

### Step 4: Brute-Force Attack Detection

Investigated repeated failed authentication attempts to identify potential brute-force activity.

Indicators considered:

- Multiple failed login attempts within a short period
- Repeated attempts against the same account
- Login attempts targeting multiple accounts
- Authentication failures originating from the same IP address
- Potential successful login following repeated failures

**Detection logic:** A high volume of failed authentication events from a single source IP can indicate a brute-force attempt. However, the activity must be investigated before classifying it as malicious.

### Step 5: IP Blocking

After identifying and investigating the suspicious source IP, performed the IP-blocking action available in the lab environment.

The purpose was to prevent further suspicious connection attempts from the identified source.

Actions included:

- Identifying the suspicious source IP.
- Reviewing its associated authentication activity.
- Confirming the suspicious behavior.
- Applying the IP-blocking action.
- Reviewing subsequent activity to check whether the suspicious attempts continued.

### Step 6: Incident Reporting

Documented the investigation findings and reported the suspicious activity.

The report included:

- Suspicious source IP address
- Related login attempts
- Observed brute-force indicators
- Affected user accounts, if identified
- Investigation timeline
- IP-blocking action
- Final investigation outcome

## 5. Key Findings

The exercise provided practical experience in identifying and investigating suspicious authentication activity.

| Investigation Area | Finding / Action |
|---|---|
| SIEM Monitoring | Reviewed security events through the SIEM dashboard. |
| IP Analysis | Identified suspicious source IP activity. |
| Login Monitoring | Analyzed successful and failed authentication attempts. |
| Brute-Force Detection | Investigated repeated failed login attempts. |
| Threat Response | Blocked the identified suspicious IP in the lab. |
| Incident Reporting | Documented and reported the investigated activity. |

## 6. Investigation Evidence

Add screenshots from your TryHackMe lab to demonstrate the investigation.

| Screenshot | Evidence to Include |
|---|---|
| `01-siem-dashboard.png` | SIEM dashboard showing security events. |
| `02-suspicious-ips.png` | Suspicious IP addresses identified during analysis. |
| `03-login-attempts.png` | Failed and successful login attempts. |
| `04-brute-force-detection.png` | Repeated authentication failures or related alert. |
| `05-ip-blocking.png` | Evidence of the IP-blocking action. |
| `06-incident-report.png` | Final incident report or investigation summary. |

## 7. Skills Practiced

- SIEM dashboard monitoring
- Security event analysis
- Authentication log investigation
- Suspicious IP identification
- Brute-force attack detection
- Security alert investigation
- Basic incident response
- IP blocking and threat containment
- Incident documentation and reporting

## 8. Lessons Learned

- SIEM dashboards help centralize security events and identify suspicious activity.
- Repeated failed login attempts can indicate brute-force activity.
- Source IP addresses provide useful context during authentication investigations.
- Successful logins following repeated failures should be investigated carefully.
- Blocking suspicious IP addresses can help contain malicious activity.
- Proper incident documentation helps communicate findings and response actions.

## 9. Investigation Summary

Completed a hands-on SIEM investigation in TryHackMe involving suspicious IP addresses and authentication activity. Analyzed login attempts, investigated repeated failures indicating potential brute-force behavior, identified the suspicious source IP, applied an IP-blocking action within the lab environment, and documented the incident findings.

---

**Note:** This documentation describes activity performed in a controlled TryHackMe lab environment. Replace or supplement the evidence section with your actual screenshots and investigation details.
