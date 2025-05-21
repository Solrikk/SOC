# Case report for event ID: 9372

| ID | Alert rule | Description | Incident type | Severity level | Date and time detected |
|----|------------|-------------|--------------|----------------|------------------------|
| 9372 | Suspicious Email with External Links | This alert was triggered by an inbound email containing one or more external links due to potentially suspicious characteristics. As part of the investigation, check firewall or proxy logs to determine whether any endpoints have attempted to access the URLs in the email and whether those connections were allowed or blocked. | Phishing | High | May 17th 2025 at 16:29 |

## Incident Details

**Datasource:** email

**Timestamp:** 05/17/2025 16:29:58.928

**Subject:** Unusual Sign-In Activity on Your Microsoft Account

**Sender:** no-reply@m1crosoftsupport.co

**Recipient:** c.allen@thetrydaily.thm

**Attachment:** None

**Content:**
```
Hi C.Allen,

We detected an unusual sign-in attempt on your Microsoft account.

Location: Lagos, Nigeria

IP Address: 102.89.222.143

Date: 2025-01-24 06:42

If this was not you, please secure your account immediately to avoid unauthorized access.

<a href="https://m1crosoftsupport.co/login">Review Activity</a>

Thank you,

Microsoft Account Security Team
```

**Direction:** inbound

## Analysis and Findings

This email exhibits multiple indicators of a phishing attempt:

1. **Deceptive Sender Domain:** The sender address uses "m1crosoftsupport.co" (with the number "1" instead of "i") instead of a legitimate Microsoft domain like microsoft.com
2. **Urgency Creation:** The email creates a sense of urgency regarding account security
3. **Suspicious Link:** The email contains a link to a non-Microsoft domain that likely hosts a credential harvesting page
4. **Geographic Mismatch:** References to login from Nigeria may be used to trigger emotional response and reduce critical thinking
5. **Brand Impersonation:** The email is designed to appear as if it's from Microsoft's security team

## Recommended Actions

1. **Block Domain:** Add "m1crosoftsupport.co" to email blocklist and web filtering solutions
2. **User Education:** Send an advisory to all users about this specific phishing attempt
3. **Check Access Logs:** Review web proxy/firewall logs to determine if any users attempted to access the link
4. **Password Reset:** If any users accessed the link, initiate password resets and additional security checks
5. **Enhanced Monitoring:** Monitor for additional emails from this sender or similar patterns

## Status: ACTIVE INVESTIGATION
