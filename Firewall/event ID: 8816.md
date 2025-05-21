# Case report for event ID: 8816

| ID | Alert rule | Description | Incident type | Severity level | Date and time detected |
|----|------------|-------------|--------------|----------------|------------------------|
| 8816 | Access to Blacklisted External URL Blocked by Firewall | This alert was triggered when a user attempted to access an external URL that is listed in the organization's blacklist or threat intelligence feeds. The firewall or proxy successfully blocked the outbound request. Preventive control: Note: The blacklist only covers known threats. It does not guarantee protection against new or unknown malicious domains. | Firewall | High | May 17th 2025 at 18:25 |

## False Positive Report - Firewall Blocked URL

**Time of Activity:** 05/17/2025 18:25:54.928

**List of Related Entities:**  
- Datasource: Firewall
- Source IP: 10.20.2.17
- Source Port: 34257
- Destination IP: 67.199.248.11
- Destination Port: 80
- URL: http://bit.ly/3aHkX3a12340
- Protocol: TCP
- Rule: Blocked websites
- Application: Web browsing

**Reason for Classifying as False Positive:**  
This incident was flagged as a high severity alert when a user attempted to access a URL that is included in the organization's blacklist. Upon investigation, this has been determined to be a false positive for the following reasons:
- The firewall successfully performed its intended function by blocking access to a URL in the blacklist
- The blocked URL was part of normal preventive security controls functioning as designed
- No actual security breach occurred as the connection attempt was properly intercepted
- This represents expected behavior of the security controls rather than an active security incident
- The event requires no further remediation or investigation as the protection mechanism worked correctly

This type of event is considered routine operational security rather than an incident that requires investigation. The firewall's blacklist is designed to proactively block potentially malicious destinations, and this event confirms the control is working as intended.
