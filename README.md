🚨 Phishing Email Analysis — Cybersecurity Task

A practical cybersecurity project where a phishing email sample is analyzed using Kali Linux techniques. This repository demonstrates real-world SOC workflow: extracting indicators, performing domain investigation, verifying authenticity .

---

📁 Project Structure

phishing-task2/
│

├── phishing mail.txt      # Original phishing email provided

├── links.txt              # Extracted URLs from the email

├── domains.txt            # Extracted domains from the URLs

├── analysis.md            # Full phishing analysis report


---

🎯 Objective

Analyze a suspicious email to identify phishing indicators using Kali Linux tools.
The workflow includes:

Extracting URLs and domains

Investigating WHOIS records

Checking DNS: A, TXT, SPF, DMARC

Identifying social engineering patterns

---

🛠 Tools & Commands Used (Kali Linux)

1. Extracting URLs

grep -oE 'https?://[^ )]+' "phishing mail.txt" > links.txt

2. Extracting Domains

cut -d/ -f3 links.txt > domains.txt

3. WHOIS Lookup

whois <domain>

4. DNS Queries

dig <domain>
dig +short TXT <domain>

5. Creating Report

nano analysis.md
---

🔍 Summary of Email Behavior

The phishing email used:

Urgency (“verify within 24 hours”)

Fear tactics (“account may be restricted”)

Generic greeting (“Dear User”)

Suspicious link pointing to a non-legitimate domain

Non-standard sender domain mimicking a security service


These patterns match known phishing techniques.

---

📊 Indicators of Compromise (IOCs)

Type	Value

URL	https://security.example.com/verify/login
Domain	security.example.com
Sender Domain	account-security.com

---

📝 Analysis Output

The analysis.md report includes:

Raw link extraction

WHOIS & DNS findings

SPF/DMARC validation

Social engineering indicators

Final phishing verdict

Recommended mitigation steps

---

🧠 Key Learning Outcomes

Working with Kali Linux for email forensics

Extracting and analyzing phishing indicators

Understanding domain reputation checks

Recognizing social engineering tactics
