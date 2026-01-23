# 8814 – Inbound Email Containing Suspicious External Link
## Description
This alert was triggered by an inbound email contains one or more external links due to potentially suspicious characteristics. As part of the investigation, check firewall or proxy logs to determine whether any endpoints have attempted to access the URLs in the email and whether those connections were allowed or blocked.

**Alert Details**
* **Timestamp:** 01/22/2026 18:59:00.489
* **Datasource:** Email
* **Direction:** Inbound
* **Subject:** `Action Required: Finalize Your Onboarding Profile`
* **Sender:** `onboarding@hrconnex.thm`
* **Recipient:** `j.garcia@thetrydaily.thm`
* **Attachment:** None

### Content
Hi Ms. Garcia,\n\nWelcome to TheTryDaily!\n\nAs part of your onboarding, please complete your final profile setup so we can configure your access.\n\nKindly click the link below:\n\n<a href=”https://hrconnex.thm/onboarding/15400654060/j.garcia”>Set Up My Profile</a>.\n\nIf you have questions, please reach out to the HR Onboarding Team.

### Investigation & Verdict

**Related Entities:** `hrconnex.thm`

**Investigation Steps:**
Investigated `hrconnex.thm` in the SIEM. Identified past email communications between HR and the IT team referencing this domain, confirming it is a known and legitimate internal resource.

**Verdict:** False Positive

**Reason:** The domain `hrconnex.thm` is a legitimate and trusted website. This is not malicious traffic.
