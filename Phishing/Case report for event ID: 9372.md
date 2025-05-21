
# Case report for event ID: 8817

| ID | Alert rule | Description | Incident type | Severity level | Date and time detected |
|----|------------|-------------|--------------|----------------|------------------------|
| 8817 | Inbound Email Containing Suspicious External Link | This alert was triggered by an inbound email contains one or more external links due to potentially suspicious characteristics. As part of the investigation, check firewall or proxy logs to determine whether any endpoints have attempted to access the URLs in the email and whether those connections were allowed or blocked. | Phishing | Medium | May 17th 2025 at 18:26 |

## True Positive Report - Suspicious Phishing Email

**Time of Activity:** 05/17/2025 18:26:12.345

**List of Affected Entities:**  
- Datasource: Email System
- Recipient: c.allen@thetrydaily.thm
- Sender: no-reply@m1crosoftsupport.co
- Email Subject: Unusual Sign-In Activity on Your Microsoft Account
- External URL: https://m1crosoftsupport.co/login
- Affected System: Email Gateway

**Reason for Classifying as True Positive:**  
This incident was correctly identified as a true positive phishing attempt for the following reasons:
- The sender domain "m1crosoftsupport.co" uses typosquatting (number "1" instead of letter "i") to impersonate Microsoft
- The email creates a false sense of urgency with claims of unauthorized access from Nigeria
- The included link directs to a non-Microsoft domain likely hosting a credential harvesting page
- The message format and branding attempts to impersonate legitimate Microsoft security communications
- The geographical location mentioned (Lagos, Nigeria) is a common social engineering tactic

**Reason for Escalating the Alert:**  
This alert requires immediate escalation due to:
- Targeted attack against a specific employee (c.allen)
- Sophisticated impersonation of Microsoft security communications
- Potential credential theft that could lead to account compromise
- Risk of lateral movement if credentials were to be harvested
- Evidence of a targeted phishing campaign against our organization

**Recommended Remediation Actions:**  
1. Block the malicious domain "m1crosoftsupport.co" at the firewall and email gateway
2. Verify if the recipient attempted to access the link or entered credentials
3. If credentials were potentially compromised, force password reset for the affected user
4. Conduct enhanced monitoring of the affected user's account for 30 days
5. Send organization-wide notification about this specific phishing campaign
6. Update email security rules to better detect typosquatted Microsoft domains
7. Implement additional security awareness training focused on Microsoft impersonation attacks

**List of Attack Indicators:**  
- Domain: m1crosoftsupport.co (typosquatting)
- Email sender: no-reply@m1crosoftsupport.co
- Subject line: "Unusual Sign-In Activity on Your Microsoft Account"
- Phishing URL: https://m1crosoftsupport.co/login
- Reference to login from Nigeria with IP 102.89.222.143
- Email content creating urgency to "secure your account immediately"
- Impersonation of "Microsoft Account Security Team"

## Status: CONFIRMED INCIDENT - REMEDIATION IN PROGRESS
