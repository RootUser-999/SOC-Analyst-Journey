# SOC Analyst Fundamentals

## Introduction

This document contains my learning notes from the **SOC Analyst L1 Complete Series With Hands-On**, a structured cybersecurity training series covering Security Operations Center (SOC) operations, security monitoring, log analysis, threat detection, SIEM concepts, and incident investigation.

**Training Source:** ZeroDayVault – Cyber Panchayat  
**Instructor:** Sumit Jain  
**Platform:** YouTube  
**Training Status:** Completed

[Watch the Complete Training Playlist](https://www.youtube.com/playlist?list=PLl00VsGSqbtxjr2XGhEgrm_Fg_V3mTMkV)

---

# 1. Security Operations Center (SOC)

## What is a SOC?

A Security Operations Center (SOC) is a centralized team responsible for continuously monitoring, detecting, investigating, and responding to cybersecurity threats affecting an organization's IT infrastructure.

The primary objective of a SOC is to identify security incidents as early as possible and minimize their impact.

### Core Responsibilities of a SOC

- Continuous security monitoring.
- Detection of suspicious activities and potential threats.
- Security event analysis and investigation.
- Monitoring network and endpoint activities.
- Identifying Indicators of Compromise (IOCs).
- Investigating security alerts.
- Incident escalation and reporting.
- Supporting incident response activities.

## SOC Analyst Responsibilities

A SOC Analyst monitors security events, investigates alerts, identifies suspicious behavior, and determines whether an activity represents a potential security threat.

### Common Responsibilities

- Monitor security dashboards and SIEM alerts.
- Review Windows and Linux security logs.
- Investigate suspicious IP addresses and domains.
- Identify abnormal authentication activities.
- Analyze potential malware-related events.
- Correlate security events from different sources.
- Document investigation findings.
- Escalate confirmed or suspicious incidents.

## SOC Analyst Tiers

### L1 – Security Monitoring and Alert Triage

The first level of SOC operations focuses on monitoring and initial investigation.

Responsibilities:
- Monitor incoming security alerts.
- Perform initial alert analysis.
- Identify suspicious activities.
- Differentiate potential true positives from false positives.
- Collect relevant evidence.
- Escalate incidents requiring deeper investigation.

### L2 – Incident Investigation

L2 analysts perform deeper investigations into escalated security incidents.

Responsibilities:
- Conduct detailed incident investigations.
- Analyze attack behavior and indicators.
- Investigate compromised systems.
- Identify the scope and impact of incidents.
- Support containment and remediation.

### L3 – Advanced Threat Analysis

L3 analysts handle complex security incidents and advanced investigations.

Responsibilities:
- Advanced threat hunting.
- Malware and forensic investigations.
- Advanced detection engineering.
- Analysis of sophisticated attack techniques.
- Improving security detection capabilities.

---

# 2. SOC Operations and Workflow

SOC operations involve multiple stages of security monitoring and incident investigation.

### General SOC Workflow

1. **Monitoring:** Collect and monitor security events from different systems.
2. **Detection:** Identify potentially suspicious activities.
3. **Alert Generation:** Generate alerts based on detection rules and security events.
4. **Triage:** Review alerts and determine their priority.
5. **Investigation:** Analyze relevant logs, indicators, and supporting evidence.
6. **Escalation:** Forward incidents requiring further investigation.
7. **Response:** Support appropriate containment and remediation activities.
8. **Documentation:** Record findings and investigation results.

### Security Alert Triage

Alert triage is the process of reviewing, prioritizing, and initially investigating security alerts.

Important considerations:

- Alert severity.
- Source and destination information.
- Affected users and systems.
- Event timestamps.
- Related security events.
- Potential business impact.
- Available threat intelligence.

### True Positive vs. False Positive

| Classification | Description |
|---|---|
| True Positive | An alert correctly identifies malicious or suspicious activity. |
| False Positive | An alert is generated for activity that is actually legitimate. |
| True Negative | Legitimate activity is correctly identified as non-malicious. |
| False Negative | Malicious activity is missed by security detection. |

---

# 3. Security Logs and Log Analysis

## What are Security Logs?

Security logs are records of activities performed by users, applications, operating systems, and network devices.

SOC analysts use logs to understand system behavior, investigate suspicious activities, and identify potential security incidents.

### Common Log Sources

- Windows Event Logs.
- Linux system logs.
- Authentication logs.
- Firewall logs.
- Network device logs.
- Endpoint security logs.
- Application logs.
- Web server logs.

## Windows Event Logs

Windows Event Logs record operating system and application activities.

The Windows Event Viewer provides a centralized interface for viewing and analyzing these events.

### Main Windows Event Log Categories

| Log Category | Purpose |
|---|---|
| Application | Records application-related events. |
| Security | Records authentication, auditing, and security events. |
| System | Records operating system and service events. |
| Setup | Records installation and configuration events. |

### Important Windows Event IDs

| Event ID | Description |
|---|---|
| 4624 | Successful account logon. |
| 4625 | Failed account logon. |
| 4634 | Account logoff. |
| 4648 | Logon attempted using explicit credentials. |
| 4672 | Special privileges assigned to a new logon. |
| 4688 | A new process has been created. |
| 4720 | A user account was created. |
| 4722 | A user account was enabled. |
| 4726 | A user account was deleted. |
| 4732 | A member was added to a security-enabled local group. |
| 1102 | The audit log was cleared. |

**Why Event IDs Matter:** They help SOC analysts identify authentication anomalies, suspicious account changes, unusual process execution, and other security-relevant activities.

## Linux Log Analysis

Linux systems maintain logs that provide information about system activities, authentication attempts, services, and potential security events.

Common log locations:

| Log File | Purpose |
|---|---|
| `/var/log/auth.log` | Authentication and authorization events on Debian-based systems. |
| `/var/log/syslog` | General system activity on many Debian-based systems. |
| `/var/log/kern.log` | Kernel-related events. |
| `/var/log/secure` | Authentication and security messages on some distributions. |
| `/var/log/messages` | General system messages on some distributions. |

### Useful Linux Commands

```bash
# View recent system logs
journalctl -n 50

# View authentication logs
sudo cat /var/log/auth.log

# Monitor authentication logs in real time
sudo tail -f /var/log/auth.log

# Search for failed authentication attempts
sudo grep -i "failed" /var/log/auth.log

# View recent system activity
last

# View failed login attempts
sudo lastb
```

---

# 4. SIEM – Security Information and Event Management

## What is SIEM?

SIEM stands for Security Information and Event Management.

A SIEM platform collects, centralizes, analyzes, and correlates security events from different sources to help security teams detect and investigate potential threats.

### Main Functions of SIEM

- Centralized log collection.
- Log parsing and normalization.
- Security event correlation.
- Real-time security monitoring.
- Alert generation.
- Security dashboards and reporting.
- Incident investigation support.

### SIEM Workflow

1. Collect logs from endpoints, servers, and network devices.
2. Forward logs to the SIEM platform.
3. Parse and normalize collected events.
4. Analyze events using detection rules.
5. Correlate related security activities.
6. Generate alerts for suspicious behavior.
7. Investigate alerts and document findings.

### Common SIEM Platforms

- Splunk.
- IBM QRadar.
- Microsoft Sentinel.
- Wazuh.
- Elastic Security.

## Log Correlation

Log correlation involves connecting related events from multiple log sources to identify suspicious patterns that may not be obvious when analyzing individual events.

**Example:**

1. Multiple failed login attempts occur on a Windows machine.
2. A successful login follows those failures.
3. An unusual process starts running.
4. The account performs suspicious activities.

Analyzing these events together can provide a stronger indication of a potential security incident.

## SIEM Detection Rules and Use Cases

A SIEM use case defines a security scenario that an organization wants to detect and investigate.

Examples:

- Multiple failed login attempts.
- Suspicious account creation.
- Privilege escalation.
- Unusual process execution.
- Potential brute-force attacks.
- Suspicious network connections.

Correlation rules help identify relationships between events and generate alerts when defined conditions are met.

---

# 5. Threat Intelligence

## What is Threat Intelligence?

Threat intelligence is the collection and analysis of information about potential or existing cyber threats.

It helps security analysts understand attacker behavior, investigate suspicious indicators, and make informed security decisions.

## Indicators of Compromise (IOCs)

IOCs are observable indicators that may suggest a system or network has been compromised.

### Common IOC Types

- Suspicious IP addresses.
- Malicious domain names.
- File hashes.
- Suspicious URLs.
- Malware filenames.
- Unusual network connections.

## IP Address Investigation

SOC analysts investigate suspicious IP addresses to understand their reputation and potential involvement in malicious activities.

Important investigation details:

- IP address ownership.
- Geolocation information.
- ASN and network provider.
- Reputation and threat intelligence results.
- Associated malicious activity.
- Related domains and indicators.

## Domain Investigation

Domain investigation helps determine whether a domain is associated with phishing, malware distribution, command-and-control infrastructure, or other suspicious activities.

Important investigation details:

- Domain registration information.
- DNS records.
- Domain age.
- IP address resolution.
- Reputation information.
- Threat intelligence reports.

---

# 6. Malware and Suspicious Activity Investigation

Malware is malicious software designed to compromise systems, steal information, disrupt operations, or provide unauthorized access.

### Common Malware Categories

- Viruses.
- Worms.
- Trojans.
- Ransomware.
- Spyware.
- Rootkits.
- Remote Access Trojans (RATs).

### Suspicious Activities SOC Analysts Should Recognize

- Repeated failed authentication attempts.
- Unexpected account creation.
- Unusual privilege assignments.
- Suspicious process execution.
- Unexpected network connections.
- Unusual file modifications.
- Suspicious PowerShell activity.
- Unexpected changes to system configurations.

### Basic Investigation Approach

1. Identify the suspicious event or alert.
2. Determine the affected system and user.
3. Review relevant logs.
4. Identify associated IPs, domains, and file hashes.
5. Correlate related events.
6. Assess the potential impact.
7. Document the findings.
8. Escalate when necessary.

---

# 7. Security Tools and Resources

Security tools help SOC analysts collect evidence, investigate indicators, analyze logs, and monitor security activities.

### SIEM and Security Monitoring

- Splunk
- Wazuh
- IBM QRadar
- Elastic Security

### Threat Intelligence and IOC Investigation

- VirusTotal
- AbuseIPDB
- AlienVault OTX
- URLhaus
- Cisco Talos Intelligence

### Network and Traffic Analysis

- Wireshark
- tcpdump

### General Investigation Resources

- WHOIS lookup services.
- DNS lookup tools.
- IP reputation databases.
- Malware intelligence databases.

*These are relevant tools and resources for the covered learning areas, not a claim that every tool was independently used during the training.*

---

# 8. Phishing Email Analysis

Phishing is a social engineering attack in which attackers use deceptive emails or messages to trick users into revealing sensitive information, downloading malware, or visiting malicious websites.

### Common Phishing Indicators

- Suspicious sender addresses.
- Misleading display names.
- Unexpected attachments.
- Suspicious links.
- Urgent or threatening language.
- Requests for credentials or sensitive information.
- Mismatched sender and reply-to addresses.

### Email Investigation Areas

- Sender information.
- Recipient information.
- Email subject.
- Email headers.
- Sending IP address.
- URLs and attachments.
- SPF, DKIM, and DMARC authentication results.

### Phishing Investigation Process

1. Examine the sender and recipient information.
2. Review the email headers.
3. Identify suspicious URLs and attachments.
4. Check domain and IP reputation.
5. Investigate relevant indicators using threat intelligence.
6. Document the findings.

---

# 9. Practical SOC Learning Areas

The training series also introduces practical SOC learning through demonstrations, projects, security tools, log sources, and attack simulations.

Important practical areas include:

- Working with security log sources.
- Understanding security monitoring workflows.
- Investigating suspicious IP addresses.
- Learning how to use threat intelligence resources.
- Understanding SIEM-based log analysis.
- Exploring phishing email datasets.
- Learning about security tools used in SOC environments.
- Understanding attack simulations and their detection.

---

# 10. Key Skills and Learning Outcomes

After completing this training series, I developed foundational knowledge in the following areas:

### SOC Operations
- Understanding SOC structure and operations.
- Understanding L1, L2, and L3 analyst responsibilities.
- Security alert triage concepts.
- Incident investigation workflows.

### Log Analysis
- Understanding Windows Event Logs.
- Understanding Linux system and authentication logs.
- Identifying important Windows Event IDs.
- Recognizing suspicious authentication activities.

### SIEM
- Understanding SIEM architecture and functionality.
- Log collection and centralization concepts.
- Event correlation fundamentals.
- Detection rules and SIEM use cases.

### Threat Intelligence
- Understanding Indicators of Compromise.
- IP address and domain investigation.
- Threat intelligence resources.
- Malware-related indicators.

### Incident Investigation
- Recognizing suspicious system activities.
- Understanding phishing investigation.
- Basic malware investigation concepts.
- Incident documentation and escalation.

---

# 11. Training Reference

**Course:** SOC Analyst L1 Complete Series With Hands-On

**Instructor:** Sumit Jain

**YouTube Playlist:**  
https://www.youtube.com/playlist?list=PLl00VsGSqbtxjr2XGhEgrm_Fg_V3mTMkV

**Repository:** SOC Analyst Journey

**Status:** Completed

---

*This document represents my learning notes and foundational understanding developed through the training series. Additional practical exercises, lab configurations, investigation reports, screenshots, and technical demonstrations will be documented separately in this repository.*
