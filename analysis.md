# Phishing Email Analysis Report
*File Analyzed:* phishing mail.txt   
*Date:* <09/12/2025>

---

## 1. Email Summary
The email claims there were unusual login attempts and asks the user to verify their identity using a link.

---

## 2. Extracted Link
From links.txt:

- https://security.example.com/verify/login

---

## 3. Domain Analysis
Domain extracted:

- security.example.com

### WHOIS:
The domain belongs to the reserved domain "example.com" under IANA.  
This indicates the domain is *not legitimate*.

### DNS Lookup:
- No A record (no IP address)
- No MX record
- No TXT/SPF/DMARC

This strongly indicates phishing.

---

## 4. Social Engineering Indicators
- *Urgency:* "within 24 hours"
- *Threat:* "account may be restricted"
- *Generic greeting:* "Dear User"
- *Suspicious sender domain:* account-security.com
- *Untrusted link:* security.example.com

---

## 5. Final Verdict
This is a *phishing email* designed to trick the user into clicking a malicious link and entering personal information.

---

## 6. Recommendation
- Do not click the link.
- Delete the email.
- Report to the security team.
