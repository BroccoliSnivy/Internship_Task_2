# Internship - Day 2 : Phishing Email Dissection Report

Phishing is a type of social engineering attack where an attacker sends fraudulent messages designed to trick a human into revealing sensitive information or clicking on malicious links. These emails often impersonate legitimate institutions or people to gain the victim’s trust.

---

## Sample Phishing Email

```bash
From: PayPal Security <security@secure-paypall.com>  
To: you@example.com  
Subject: Urgent: Account Verification Required

Dear Customer,

We noticed unusual activity in your PayPal account. To protect your 
account, we’ve temporarily limited your access. To restore full access, 
please verify your identity by clicking the link below:

[Verify My Account Now](http://paypal-secure-update.com/verify)

Failure to act within 24 hours may result in permanent account suspension.

Thank you for choosing PayPal.  

Sincerely,  
PayPal Security Team
```



---

## Characteristics of the Phishing Email

The sender tries to appear legitimate using a professional-sounding email and message tone, but there are subtle cues of forgery. The domain used (`secure-paypall.com`) is not the real PayPal domain, even though it visually looks similar. The email uses urgency and fear to force action. The link provided does not point to a real PayPal website.

---

#### **Suspecious Elements**

**1. Suspicious Sender Email**

- The sender address looks like: `support@security.paypall.com`

- At a glance, it feels legit, but notice the domain — **“paypall”** with two Ls.

- This is a classic spoofing method to trick people who skim through emails.

**2. Threatening / Urgent Language**

- Phrases like: *“Failure to act within 24 hours will result in permanent suspension.”*

- This is psychological pressure to rush you into clicking without thinking.

**3. Misleading Links**

- The button says: **“Verify My Account Now”**

- But when you hover over it, the link is to `paypal-secure-update.com` — **not** a PayPal domain.

- Always hover over links before clicking — mismatched or unfamiliar domains are a huge warning sign.

**4. Lack of Personalization**

- Starts with “Dear Customer” — but real emails from services like PayPal usually use your real name.

- Phishing emails are sent to thousands at once, so they stay generic.

**5. Odd Formatting or Design Inconsistencies (optional)**

- Fonts, colors, or button design might look slightly off.

- It’s not always obvious, but something may “feel weird” about the layout.

---

## Tools to Analyze Email Headers

- **MXToolbox Email Header Analyzer** — https://mxtoolbox.com/EmailHeaders.aspx

- **Google Admin Toolbox Messageheader** — https://toolbox.googleapps.com/apps/messageheader/

- **IPVoid Email Analyzer** — https://www.ipvoid.com/email-source-analyzer/

These tools help uncover where the email actually came from by parsing the raw headers and highlighting mismatches in mail server paths, SPF failures, and forged sender info.

---

## Final Notes

Phishing emails are getting better at looking legitimate. They may use real logos, footers, and even valid-looking domains. But even the best fakes leave behind clues. Always look closely at the domain, the tone, and where the links are pointing. If it sounds too urgent to be real, it usually isn’t.
