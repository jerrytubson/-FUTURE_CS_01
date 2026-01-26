# Vulnerability Assessment Report – Future Interns Task 1

## Overview
This project contains a professional read-only vulnerability assessment conducted as part of the Future Interns Cyber Security Internship.

The goal was to evaluate a live public website for common security weaknesses using passive and ethical testing techniques, then document findings in a business-friendly security audit report.

---

## Target Website
testphp.vulnweb.com

---

## Scope
Only non-intrusive testing methods were used.

Allowed:
- Public pages only
- Passive scanning
- Header analysis
- Configuration review

Not performed:
- Exploitation
- Brute force attacks
- Denial-of-Service
- Authentication bypass

---

## Tools Used
- Nmap – Service and port discovery
- OWASP ZAP – Passive vulnerability scanning
- Browser Developer Tools – Manual header inspection
- Canva – Professional report design

---

## Findings Summary

### Medium Risk
- Absence of Anti-CSRF protection
- Missing Content Security Policy (CSP)
- Missing Anti-clickjacking header

### Low Risk
- Server version information disclosure
- X-Powered-By technology disclosure
- Missing X-Content-Type-Options header

### Exposure
- HTTP service accessible on port 80

---

## Repository Structure

