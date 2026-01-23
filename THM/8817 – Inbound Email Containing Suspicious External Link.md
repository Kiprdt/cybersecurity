# 8817 – Inbound Email Containing Suspicious External Link
## Description
This alert was triggered by an inbound email contains one or more external links due to potentially suspicious characteristics. As part of the investigation, check firewall or proxy logs to determine whether any endpoints have attempted to access the URLs in the email and whether those connections were allowed or blocked.

**Alert Details**
* **Timestamp:** 01/22/2026 19:02:00.489
* **Datasource:** Email
* **Direction:** Inbound
* **Sender:** `no-reply@m1crosoftsupport.co`
* **Recipient:** `c.allen@thetrydaily.thm`
* **Subject:** `Unusual Sign-In Activity on Your Microsoft Account`
* **Attachment:** None

### Content
Hi C.Allen,\n\nWe detected an unusual sign-in attempt on your Microsoft account.\n\nLocation: Lagos, Nigeria\n\nIP Address: 102.89.222.143\n\nDate: 2025-01-24 06:42\n\nIf this was not you, please secure your account immediately to avoid unauthorized access.\n\n<a href=”https://m1crosoftsupport.co/login”>Review Activity</a>\n\nThank you,\n\nMicrosoft Account Security Team

## Investigation
My investigation confirms that this is a phishing attack using typosquatting because there is a clear spelling error in the domain name (using "1" instead of "i"). After I identified the link as malicious, I searched the SIEM logs and found a record showing that the firewall allowed the user's traffic to this domain. This means the user successfully reached the fake website, and their password was likely stolen and leaked to the attacker.

### Attack Indicators (IOCs)
* **Phishing URL:** `https://m1crosoftsupport.co/login`
* **Malicious Domain:** `m1crosoftsupport.co`
* **Attacker IP:** `45.148.10.131`

## Verdict & Disposition
* **Verdict:** True Positive (TP)
* **Status:** Escalated for Incident Response

## Remediation Plan
* **Isolate Host:** Remove `10.20.2.25` from the network to prevent lateral movement.
* **Account Remediation:** Immediate password reset and session revocation for `c.allen`.
* **Network Blocking:** Blacklist `m1crosoftsupport.co` and IP `45.148.10.13` on the corporate proxy/firewall.
* **Investigation:** Scan the endpoint for any subsequent downloads or secondary infections following the link click.
