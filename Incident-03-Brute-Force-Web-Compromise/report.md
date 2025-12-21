# Incident Title: Brute Force Attack Leading to Website Compromise

## 1. Summary
Multiple users reported being redirected to a fake website and experiencing system slowdowns after downloading a file from the company’s website. An investigation revealed that the website had been compromised following a brute force attack on the admin account.

## 2. Detection
The incident was detected after customers contacted the helpdesk reporting suspicious download prompts, redirections, and degraded system performance.

## 3. Analysis
- Protocol: HTTP (Port 80)
- Attack Type: Brute Force → Malware Injection
- Affected System: Web server / Admin panel

The attacker repeatedly attempted to log in using common or default passwords. After successfully gaining access to the administrative account, the attacker modified the website’s source code.

A malicious JavaScript function was injected to prompt users to download a file. After executing the file, users were redirected to a spoofed website hosting malware.

## 4. Root Cause
- Weak password security for the admin account
- No brute-force protection mechanisms (account lockout, rate limiting)
- Lack of web application security controls

## 5. Impact
- Website integrity compromised
- Users exposed to malware
- Loss of user trust
- Potential data and reputation damage

## 6. Mitigation & Recovery
Immediate actions:
- Isolate or temporarily shut down the affected web server
- Reset all administrative credentials
- Remove injected malicious scripts
- Notify users and recommend malware scans

Preventive measures:
- Enforce strong password policies
- Enable Multi-Factor Authentication (MFA)
- Implement account lockout and rate limiting
- Deploy a Web Application Firewall (WAF)

## 7. Lessons Learned
- Brute-force attacks remain a common threat
- Strong authentication and monitoring are critical
- Early detection can prevent malware distribution

## 8. Confidence Level
High – User reports, log analysis, and code injection confirm the attack chain.
