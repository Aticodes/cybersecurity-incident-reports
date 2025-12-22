# Incident Title: Phishing Attack Leading to Credential Compromise and Data Breach

## 1. Summary
An intern reported being unable to access her internal network account. Access logs revealed that the account was actively accessing customer database records despite the intern being locked out. Further investigation showed that the intern had entered her credentials on a malicious external website, leading to unauthorized access and a data breach.

## 2. Detection
The incident was detected after the intern reported login issues and multiple employees noticed missing or altered customer records. Access logs confirmed suspicious activity originating from the compromised account.

## 3. Analysis
- Attack Type: Credential Phishing
- Affected Account: Intern user account
- Impacted Asset: Customer database

A malicious actor obtained the intern’s login credentials through a phishing email directing her to a fake login page. The attacker used these credentials to access the internal network and customer database, resulting in data exposure and manipulation.

## 4. Impact
- Unauthorized access to customer data
- Deletion and modification of customer records
- Potential regulatory and reputational damage

## 5. Response Actions
- Disabled the compromised user account
- Audited access logs and affected systems
- Informed management and initiated incident communication procedures
- Notified customers and relevant authorities as required by policy

## 6. Recovery
- Restored the customer database from the previous night’s full backup
- Informed staff to re-enter data created after the backup
- Verified system integrity after restoration

## 7. Preventive Measures
- Enforced Multi-Factor Authentication (MFA)
- Limited login attempts
- Conducted security awareness training for employees and interns
- Implemented improved firewall configurations
- Deployed intrusion detection and prevention systems (IDS/IPS)

## 8. Lessons Learned
- Phishing remains a high-risk attack vector
- User awareness is critical to security
- Backups and recovery plans are essential for minimizing damage

## 9. Confidence Level
High – Logs, user reports, and data integrity issues confirm the attack.
