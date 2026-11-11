# SOC Analyst Tools & Technologies Reference

## Overview

This document provides a categorized reference of cybersecurity tools commonly used by Security Operations Center (SOC) analysts for security monitoring, threat detection, malware investigation, phishing analysis, network traffic inspection, endpoint monitoring, and incident response.

The purpose of this documentation is to understand the functionality of each tool, its role in SOC operations, and how it can be applied during security investigations.

---

# 1. File, Malware & Attachment Analysis

Tools used to inspect suspicious files, email attachments, executables, documents, and potential malware.

| Tool | Purpose | Website |
|---|---|---|
| VirusTotal | Scans files, hashes, URLs, and domains using multiple security engines. | https://www.virustotal.com/ |
| ANY.RUN | Interactive malware sandbox for observing suspicious file behavior. | https://any.run/ |
| Hybrid Analysis | Performs automated malware analysis and provides behavioral reports. | https://www.hybrid-analysis.com/ |
| Joe Sandbox | Advanced malware analysis and sandbox investigation. | https://www.joesandbox.com/ |
| MetaDefender Cloud | Multiengine file scanning, hash analysis, and file sanitization. | https://metadefender.opswat.com/ |
| CAPE Sandbox | Automated malware analysis and behavioral investigation. | https://github.com/kevoreilly/CAPEv2 |

### Common Investigation Tasks
- Calculate file hashes (MD5, SHA-1, SHA-256).
- Check file reputation.
- Identify potentially malicious files.
- Analyze executable behavior.
- Inspect file activities in sandbox environments.
- Identify Indicators of Compromise (IOCs).

---

# 2. URL & Phishing Analysis

Tools used to investigate suspicious URLs, phishing websites, malicious redirects, and fraudulent domains.

| Tool | Purpose | Website |
|---|---|---|
| URLScan.io | Analyzes URLs, website behavior, redirects, and network requests. | https://urlscan.io/ |
| VirusTotal | Checks URL and domain reputation. | https://www.virustotal.com/ |
| PhishTank | Provides a database of reported phishing URLs. | https://phishtank.org/ |
| Google Safe Browsing | Checks whether websites are known to be unsafe. | https://transparencyreport.google.com/safe-browsing/search |
| CheckPhish | Detects and investigates phishing websites. | https://checkphish.ai/ |
| ANY.RUN | Allows interactive investigation of suspicious websites. | https://any.run/ |

### Common Investigation Tasks
- Inspect suspicious URLs.
- Identify malicious redirects.
- Analyze website behavior.
- Investigate phishing domains.
- Check URL reputation.
- Identify suspicious external resources.

---

# 3. IP Address & Domain Investigation

Tools used to investigate suspicious IP addresses, domains, DNS records, network ownership, and threat intelligence indicators.

| Tool | Purpose | Website |
|---|---|---|
| AbuseIPDB | Checks IP addresses reported for abusive activities. | https://www.abuseipdb.com/ |
| Cisco Talos Intelligence | Provides IP, domain, and reputation intelligence. | https://talosintelligence.com/ |
| AlienVault OTX | Threat intelligence platform for sharing and investigating IOCs. | https://otx.alienvault.com/ |
| WHOIS Lookup | Retrieves domain registration information. | https://who.is/ |
| DNSDumpster | Provides DNS and domain infrastructure information. | https://dnsdumpster.com/ |
| GreyNoise | Helps identify common internet scanners and potentially targeted activity. | https://www.greynoise.io/ |
| Shodan | Searches for internet-exposed devices and services. | https://www.shodan.io/ |
| SecurityTrails | Provides domain, DNS, and infrastructure intelligence. | https://securitytrails.com/ |

### Common Investigation Tasks
- Investigate suspicious IP addresses.
- Check IP reputation and abuse reports.
- Identify domain ownership information.
- Analyze DNS records.
- Investigate suspicious network infrastructure.
- Identify related domains and IP addresses.
- Collect and document IOCs.

---

# 4. SIEM – Security Information and Event Management

SIEM platforms collect, centralize, correlate, and analyze security logs to identify suspicious activities and generate security alerts.

| Tool | Purpose | Website |
|---|---|---|
| Splunk Enterprise Security | Security monitoring, log analysis, alert investigation, and threat detection. | https://www.splunk.com/ |
| Wazuh | Open-source security monitoring, log analysis, endpoint security, and vulnerability detection. | https://wazuh.com/ |
| IBM QRadar | SIEM platform for event correlation, security monitoring, and threat investigation. | https://www.ibm.com/products/qradar-siem |
| Microsoft Sentinel | Cloud-native SIEM and security orchestration platform. | https://azure.microsoft.com/products/microsoft-sentinel |
| Elastic Security | Security analytics, SIEM capabilities, and threat detection. | https://www.elastic.co/security |
| Google Security Operations | Security analytics, SIEM, and threat investigation. | https://cloud.google.com/security/products/security-operations |

### Common Investigation Tasks
- Collect and analyze security logs.
- Monitor security dashboards.
- Investigate generated alerts.
- Perform event correlation.
- Identify suspicious authentication activities.
- Create and understand detection rules.
- Investigate security incidents using centralized logs.

---

# 5. Network Traffic Analysis

Tools used to capture, inspect, and analyze network traffic to identify suspicious communications and potential network attacks.

| Tool | Purpose | Website |
|---|---|---|
| Wireshark | Graphical packet capture and network protocol analysis. | https://www.wireshark.org/ |
| tcpdump | Command-line network packet capture and analysis. | https://www.tcpdump.org/ |
| Zeek | Network security monitoring and traffic analysis. | https://zeek.org/ |
| Suricata | Network IDS/IPS and threat detection. | https://suricata.io/ |
| Snort | Network intrusion detection and prevention. | https://www.snort.org/ |
| Nmap | Network discovery and service scanning. | https://nmap.org/ |

### Common Investigation Tasks
- Capture network packets.
- Analyze TCP, UDP, DNS, HTTP, and HTTPS traffic.
- Identify suspicious network connections.
- Investigate unusual communication patterns.
- Detect potential port scanning.
- Analyze network intrusion alerts.
- Identify communication with suspicious IP addresses.

---

# 6. Email Security & Phishing Investigation

Tools used to analyze suspicious emails, email headers, sender information, attachments, and phishing attempts.

| Tool | Purpose | Website |
|---|---|---|
| MXToolbox | Email header, DNS, and mail server diagnostics. | https://mxtoolbox.com/ |
| Google Admin Toolbox Messageheader | Analyzes email routing and message headers. | https://toolbox.googleapps.com/apps/messageheader/ |
| Microsoft Defender for Office 365 | Email threat protection and phishing investigation. | https://www.microsoft.com/security/business/siem-and-xdr/microsoft-defender-office-365 |
| PhishTool | Phishing email investigation and analysis. | https://phishtool.com/ |
| EML Analyzer | Examines email files and their contents. | https://eml-analyzer.herokuapp.com/ |

### Common Investigation Tasks
- Analyze email headers.
- Identify spoofed sender addresses.
- Inspect suspicious email attachments.
- Investigate phishing URLs.
- Check SPF, DKIM, and DMARC authentication.
- Identify suspicious sender IP addresses.
- Document phishing indicators.

---

# 7. Endpoint Detection & Response (EDR)

EDR solutions monitor endpoints such as computers and servers to detect malicious activities, investigate suspicious processes, and support incident response.

| Tool | Purpose | Website |
|---|---|---|
| Microsoft Defender for Endpoint | Endpoint threat detection, investigation, and response. | https://www.microsoft.com/security/business/endpoint-security/microsoft-defender-endpoint |
| CrowdStrike Falcon | Endpoint detection, threat hunting, and incident response. | https://www.crowdstrike.com/ |
| SentinelOne Singularity | Endpoint protection, threat detection, and automated response. | https://www.sentinelone.com/ |
| Elastic Defend | Endpoint protection and security monitoring. | https://www.elastic.co/security |
| Sysmon | Detailed Windows system activity logging. | https://learn.microsoft.com/sysinternals/downloads/sysmon |

### Common Investigation Tasks
- Monitor endpoint activities.
- Investigate suspicious processes.
- Detect unusual command execution.
- Identify suspicious file modifications.
- Investigate endpoint alerts.
- Monitor process creation and network connections.
- Support endpoint containment and response.

---

# 8. Digital Forensics & Incident Investigation

Tools used to collect, preserve, and analyze digital evidence during security incident investigations.

| Tool | Purpose | Website |
|---|---|---|
| Autopsy | Digital forensic investigation and disk analysis. | https://www.autopsy.com/ |
| Volatility 3 | Memory forensics and investigation. | https://github.com/volatilityfoundation/volatility3 |
| KAPE | Windows forensic artifact collection and processing. | https://www.kroll.com/en/insights/publications/cyber/kroll-artifact-parser-extractor-kape |
| Eric Zimmerman's Tools | Windows forensic artifact analysis. | https://ericzimmerman.github.io/ |
| FTK Imager | Forensic disk imaging and evidence acquisition. | https://www.exterro.com/digital-forensics-software/ftk-imager |
| Velociraptor | Endpoint visibility, digital forensics, and incident response. | https://docs.velociraptor.app/ |

### Common Investigation Tasks
- Collect digital evidence.
- Analyze disk images.
- Investigate memory dumps.
- Examine Windows forensic artifacts.
- Identify suspicious processes and activities.
- Investigate compromised systems.
- Preserve evidence for incident analysis.

---

# 9. Vulnerability Assessment & Security Scanning

Tools used to identify security weaknesses, exposed services, misconfigurations, and vulnerabilities.

| Tool | Purpose | Website |
|---|---|---|
| Nessus | Vulnerability assessment and security scanning. | https://www.tenable.com/products/nessus |
| OpenVAS | Open-source vulnerability scanning. | https://www.greenbone.net/ |
| Nmap | Network discovery and service identification. | https://nmap.org/ |
| Nikto | Web server vulnerability and configuration scanning. | https://github.com/sullo/nikto |
| Qualys VMDR | Enterprise vulnerability management and detection. | https://www.qualys.com/apps/vulnerability-management-detection-response/ |

### Common Investigation Tasks
- Identify exposed network services.
- Detect known vulnerabilities.
- Identify outdated software.
- Investigate insecure configurations.
- Review vulnerability scan results.
- Prioritize security weaknesses.

---

# 10. Useful Command-Line Utilities

SOC analysts also use command-line utilities for log investigation, file analysis, network troubleshooting, and security monitoring.

| Utility | Purpose |
|---|---|
| PowerShell | Windows administration, event log analysis, and automation. |
| Windows Event Viewer | Examines Windows system and security logs. |
| grep | Searches text and log files for specific patterns. |
| awk | Processes and analyzes structured text data. |
| sed | Searches and modifies text streams. |
| journalctl | Examines Linux systemd journal logs. |
| netstat | Displays network connections and listening ports. |
| ss | Displays socket and network connection information. |
| nslookup | Performs DNS queries. |
| dig | Retrieves DNS information. |
| curl | Makes HTTP requests and tests web endpoints. |
| sha256sum | Calculates SHA-256 file hashes on Linux. |
| Get-FileHash | Calculates file hashes using PowerShell. |

---

# 11. Recommended Learning Priority

The following sequence is a suggested learning roadmap for someone preparing for a Junior SOC Analyst or SOC Analyst L1 role.

| Priority | Tool | Learning Objective |
|---|---|---|
| 1 | VirusTotal | File, hash, URL, and domain investigation. |
| 2 | AbuseIPDB | IP reputation analysis. |
| 3 | URLScan.io | Suspicious URL and phishing investigation. |
| 4 | Windows Event Viewer | Windows security log analysis. |
| 5 | Sysmon | Detailed Windows endpoint monitoring. |
| 6 | Wireshark | Network traffic analysis. |
| 7 | Splunk | SIEM queries and security alert investigation. |
| 8 | Wazuh | Endpoint monitoring and centralized security analysis. |
| 9 | ANY.RUN | Malware sandbox investigation. |
| 10 | Microsoft Defender | Endpoint detection and response. |
| 11 | Volatility 3 | Memory forensics fundamentals. |
| 12 | Autopsy | Digital forensic investigation. |

---

# 12. Practical SOC Investigation Workflow

### Example: Suspicious Email Attachment Investigation

A SOC analyst receives an alert or user report about a suspicious email attachment.

The following workflow demonstrates how different tools can be used during the investigation.

1. **Email Analysis:** Inspect the sender, recipient, subject, and email headers using email analysis tools.
2. **File Identification:** Identify the attachment type, filename, size, and SHA-256 hash.
3. **File Reputation:** Search the file hash using VirusTotal and other threat intelligence platforms.
4. **Sandbox Investigation:** If authorized, analyze the suspicious attachment in an isolated malware sandbox such as ANY.RUN or Hybrid Analysis.
5. **IOC Collection:** Extract suspicious IP addresses, domains, URLs, and file hashes.
6. **Threat Intelligence:** Investigate collected indicators using AbuseIPDB, VirusTotal, and AlienVault OTX.
7. **SIEM Investigation:** Search Splunk or Wazuh for related endpoint and network activities.
8. **Endpoint Investigation:** Review suspicious process execution and other endpoint events.
9. **Incident Documentation:** Record findings, evidence, severity, and recommended response actions.
10. **Escalation:** Escalate the incident according to organizational security procedures.

---

# 13. Security and Responsible Tool Usage

- Only investigate systems and networks for which you have authorization.
- Never upload confidential organizational files to public scanning services without approval.
- Use isolated environments for suspicious file analysis.
- Do not execute suspicious attachments on personal or production systems.
- Preserve investigation evidence and maintain accurate documentation.
- Follow organizational incident response procedures.
- Treat third-party reputation results as investigation leads, not definitive proof of malicious activity.

---

# 14. Personal Learning Progress

This section will be updated as I explore and practice different SOC tools.

| Tool | Learning Status | Practical Documentation |
|---|---|---|
| VirusTotal | Learning / Practicing | To be added |
| AbuseIPDB | Learning / Practicing | To be added |
| URLScan.io | Learning / Practicing | To be added |
| Wireshark | Learning / Practicing | To be added |
| Splunk | Learning / Practicing | To be added |
| Wazuh | Learning / Practicing | To be added |
| Sysmon | Learning / Practicing | To be added |
| ANY.RUN | Learning / Practicing | To be added |

---

**Purpose of this Document:** Maintain a technical reference of tools used in SOC operations and continuously document my progress through hands-on exercises, practical investigations, and security labs.

**Repository:** SOC Analyst Journey
