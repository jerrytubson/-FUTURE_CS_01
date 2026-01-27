# Vulnerability Assessment Report – Future Interns Task 1

## Overview
This repository contains a read-only vulnerability assessment conducted on a public-facing website as part of the Future Interns Cyber Security Internship.

The goal of the assessment was to identify common security weaknesses using passive techniques only, classify risks, and present findings in a clear, professional, and business-friendly report without performing any exploitation.

---

## Assessment Scope & Ethics

### Allowed
- Public pages only
- Passive scanning
- Header inspection
- Configuration analysis

### Not Allowed
- Exploitation
- Brute force attacks
- Login bypass
- Denial of Service (DoS)
- Any harmful activity

All testing was performed strictly within ethical and read-only boundaries.

---

## Tools Used
- **Nmap** – Port and service exposure discovery
- **OWASP ZAP** – Passive vulnerability scanning
- **Browser DevTools** – HTTP header inspection
- **Canva** – Professional report design

---

# Findings

## 1. Service Exposure (Nmap)

Open ports discovered:

- Port 80 (HTTP)
- Port 587 (SMTP Mail Submission)

### Risk
Publicly accessible services increase the attack surface and may allow attackers to probe for misconfigurations or vulnerabilities.

### Risk Level
Low

### Recommendation
Restrict unnecessary ports using firewall rules and expose only essential services.

---

## 2. Medium Risk Vulnerabilities (OWASP ZAP)

- Absence of Anti-CSRF tokens
- Content Security Policy (CSP) header not configured
- Missing Anti-clickjacking protection (X-Frame-Options)

### Impact
These issues may allow:
- Cross-site request forgery attacks
- Clickjacking
- Malicious script execution

### Risk Level
Medium

---

## 3. Low Risk Vulnerabilities (OWASP ZAP)

- X-Powered-By header reveals technology stack
- Server version information disclosure
- Missing X-Content-Type-Options header

### Impact
Information disclosure may assist attackers during reconnaissance.

### Risk Level
Low

---

## 4. Header Misconfiguration (Browser DevTools)

### Observed Headers
- Server: nginx/1.19.0
- X-Powered-By: PHP/5.6.40

### Missing Security Headers
- Content-Security-Policy
- X-Frame-Options
- X-Content-Type-Options

### Risk
Missing headers reduce protection against:
- Clickjacking
- MIME-sniffing
- Script injection attacks

### Risk Level
Medium–Low

---

# OWASP ZAP Scan Summary

Passive Scan Results:

- High: 0
- Medium: 3
- Low: 3
- Informational: 1

Full detailed report is provided in the repository as `zap_report.html`.

---

# Evidence Provided

The following supporting files are included:

- zap_report.html – Full OWASP ZAP report
- nmap_scan.txt – Raw Nmap scan output
- browser_headers.png – DevTools header inspection screenshot
- Nmap scan screenshot
- Vulnerability_Assessment_Report.pdf – Final professional report

---

# Repository Structure


---

# Conclusion

The assessment identified several missing security headers and exposed services that increase the website’s attack surface.

Although no critical vulnerabilities were discovered, implementing recommended fixes such as enabling security headers, hiding server information, and restricting unnecessary open ports will significantly improve the website’s security posture.

---

# Author
Jeremiah Olatubosun  
Cyber Security Intern – Future Interns







