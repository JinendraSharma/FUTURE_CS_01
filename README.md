OWASP Juice Shop Security Assessment

This repository contains a full security analysis of the OWASP Juice Shop application performed using industry-standard scanning methodology and aligned with OWASP Top 10 2021 security categories. The assessment includes vulnerability discovery, risk classification, proof-of-concept examples, and prioritized remediation recommendations based on real-world exploitation risk.

📌 Assessment Overview

Target: Local instance of OWASP Juice Shop

Scan Date: Nov 30, 2025

Tools used: OWASP ZAP, Node.js environment

Total vulnerabilities identified: 16, categorized by severity

Includes SQL Injection, CORS misconfigurations, missing headers, outdated libraries, session flaws, and general information disclosures



🧪 Methodology

The assessment followed these steps:

Full application spidering & endpoint discovery

Passive analysis (header inspection, disclosure detection)

Active probing (SQLi, XSS, authentication flaws, etc.)

Dependency and JavaScript library vulnerability auditing

Mapping of findings against OWASP Top 10


🔥 Key Findings

1 Critical vulnerability: SQL Injection enabling full DB compromise

6 Medium-risk misconfigurations affecting access control & security policies

5 Low-risk issues involving informational system leakage

4 Informational findings assisting reconnaissance



🛠 Remediation Focus

Immediate (0–7 days):

Patch SQL Injection using prepared statements

Reduce permissive CORS

Implement CSP & X-Frame-Options

Migrate session IDs from URLs to HTTP-only cookies



Short-term (1–2 weeks):

Enforce Strict-Transport-Security

Implement complete CSP directives

Remove sensitive comments & timestamp disclosures


Long-term:

Ongoing scanning

Penetration tests

Dependency & patch management



