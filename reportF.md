
# Case report for event ID: 1003

| ID | Alert rule | Description | Incident type | Severity level | Date and time detected |
|----|------------|-------------|--------------|----------------|------------------------|
| 1003 | Reply to suspicious email. | An employee replied to a suspicious sender with an unusual top level domain. Note from SOC Head: This detection rule still needs fine-tuning. | Phishing | Low | May 21st 2025 at 20:19 |

## Alert details

- **datasource**: emails
- **timestamp**: 05/21/2025 18:22:04.354
- **subject**: FWD: Convention Registration Now Open: Hat Trends and Insights
- **sender**: support@tryhatme.com
- **recipient**: warner@yahoo.com
- **attachment**: None
- **content**: The content of this email has been removed in accordance with privacy regulations and company security policies to protect sensitive information.
- **direction**: outbound

## False Positive Report

**Time of Activity:** 05/21/2025 18:19:05.354

**List of Related Entities:**  
- Sender: support@tryhatme.com
- Recipient: barker@headlinehats.com
- Direction: Outbound Email
- Datasource: emails
- Host: 10.10.183.246:8989
- Sourcetype: _json

**Reason for Classifying as False Positive:**  
This email was flagged due to its metadata being processed for potential sensitive content. However, after review, the message is determined to be a legitimate business communication. The subject line references an interview request for a company spotlight article, which aligns with normal outreach behavior. Additionally, the following indicators support the false positive classification:
- The email has no attachment, minimizing the likelihood of phishing/malware.
- The content was removed in accordance with privacy/security policies, but no known indicators of compromise (IoCs) are present in the metadata.
- The sender and recipient domains appear legitimate and business-related.
- The direction is outbound, and there is no evidence of data exfiltration or suspicious payloads.
