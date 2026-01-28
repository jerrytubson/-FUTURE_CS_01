Cyber Security Assessment Projects – Future Interns (Tasks 1 & 2)
Overview


This repository contains two cybersecurity assessments completed as part of the Future Interns Cyber Security Internship Program.

The projects focus on:
Web security vulnerability assessment
Phishing email detection and awareness

Both tasks were performed using ethical, read-only, and defensive security practices.
No exploitation or harmful activity was conducted.

The objective was to identify risks, classify them clearly, and present findings in a professional, business-friendly format similar to real-world security consulting engagements.

Assessment Scope & Ethics

Allowed

Passive analysis only
Public information gathering
Header inspection
Configuration review
Email and domain investigation
Risk documentation

Not Allowed

Exploitation
Brute force attacks
Login bypass
Denial of Service (DoS)
Malware execution
Any harmful or intrusive activity

All work strictly followed ethical cybersecurity standards.

Task 1 – Vulnerability Assessment (Web Security Audit)
Objective

Perform a passive vulnerability assessment on a public-facing website to identify common security misconfigurations and exposed services without exploiting the target.

Tools Used

Nmap – Port and service exposure discovery

OWASP ZAP – Passive vulnerability scanning

Browser DevTools – HTTP header inspection

Canva – Professional report design

Findings
1. Service Exposure (Nmap)

Open ports discovered:

Port 80 (HTTP)

Port 587 (SMTP Mail Submission)

Risk

Publicly accessible services increase the attack surface and may allow attackers to probe for vulnerabilities.

Risk Level

Low

Recommendation

Restrict unnecessary services using firewall rules and expose only essential ports.

2. Medium Risk Vulnerabilities (OWASP ZAP)

Absence of Anti-CSRF tokens

Content Security Policy (CSP) not configured

Missing Anti-clickjacking protection

Impact

May allow:

Cross-site request forgery

Clickjacking

Malicious script execution

Risk Level

Medium

3. Low Risk Vulnerabilities (OWASP ZAP)

X-Powered-By header disclosure
Server version leakage
Missing X-Content-Type-Options

Impact

Information disclosure assists attackers during reconnaissance.

Risk Level

Low

4. Header Misconfiguration (Browser DevTools)
Missing Headers
Content-Security-Policy
X-Frame-Options
X-Content-Type-Options

Risk Level

Medium–Low

OWASP ZAP Scan Summary

High: 0
Medium: 3
Low: 3
Informational: 1

Evidence Provided (Task 1)
Task-1-Vulnerability-Assessment/
 ├── report/
 └── evidence/

Includes:
zap_report.html
nmap_scan.txt
header screenshots
Final PDF report

Task 2 – Phishing Detection & Awareness System
Objective

Analyze phishing email samples to identify malicious indicators, classify risks, and develop an awareness guide that helps users recognize and prevent phishing attacks.

This task simulates real-world Security Operations Center (SOC) and Security Awareness responsibilities.

Tools Used
Google Message Header Analyzer – Email authentication checks
MXToolbox – Header & domain analysis
Browser tools – Safe domain investigation
Microsoft Word / PDF – Professional reporting

Findings
1. Suspicious Sender Domains

Examples:
microsoft-security-check.com
payroll-secure-login.net

Risk

Look-alike domains impersonate trusted brands to deceive users.

Risk Level

High

Recommendation

Verify domain spelling and legitimacy before interacting.

2. Email Authentication Failures

Header analysis revealed:

SPF: fail
DKIM: none
DMARC: fail

Impact

Indicates spoofed or unauthorized sender.

Risk Level

High

3. Malicious / Suspicious Links

Links redirect users to fake credential harvesting pages.

Impact

May result in:

Credential theft

Account compromise

Financial loss

Risk Level

High

4. Social Engineering Indicators

Observed tactics:

Urgent language

Fear-based messages

Generic greetings ("Dear User", "Dear Employee")

Immediate action requests

Risk

Manipulates users into unsafe actions.

Risk Level

Medium–High

Risk Classification Summary (Task 2)

All analyzed emails were classified as:

Phishing (High Risk)

Evidence Provided (Task 2)
Task-2-Phishing-Detection/
 ├── report/
 └── evidence/


Includes:

Sample email texts
Email headers
Google Header Analyzer results
MXToolbox results
Domain lookup screenshots
Final report (PDF & DOCX)

Repository Structure
FUTURE_CS_01/
│
├── Task-1-Vulnerability-Assessment/
│   ├── report/
│   └── evidence/
│
├── Task-2-Phishing-Detection/
│   ├── report/
│   └── evidence/
│
└── README.md

Conclusion

The assessments identified multiple security weaknesses across:
 Website configuration
 Service exposure
 Missing security protections
 Phishing and social engineering threats

Although no critical exploitation was performed, implementing the recommended fixes and awareness controls will significantly improve the organization’s overall security posture.

These projects demonstrate practical skills in:

Vulnerability Assessment
Email Forensics
Phishing Detection
Risk Analysis
Security Reporting
Defensive Security Practices

Author

Jeremiah Olatubosun
Cyber Security Intern – Future Interns
