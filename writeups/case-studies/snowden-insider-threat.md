# Case Study: Edward Snowden Insider Threat (2013)

## Overview
In 2013, **Edward Snowden**, a contractor for Booz Allen Hamilton at the NSA, exfiltrated and leaked a massive cache of classified documents.  
The breach revealed U.S. surveillance programs and became one of the most high-profile insider threats in history.  

Snowden exploited **overprivileged access** and **weak oversight** of system administrators to collect data without triggering immediate alarms.  

---

## Attack Breakdown

### 1. Role & Access
- Snowden was a **systems administrator**, responsible for maintaining NSA networks.  
- This role gave him broad technical privileges across multiple classified systems.  
- He had the ability to both **administer and view data**, violating the principle of least privilege.  

### 2. Exploitation of Privileges
- Leveraged his access to move classified documents.  
- Used admin tools to copy and exfiltrate data over time.  
- No real-time monitoring flagged his unusual access patterns.  

### 3. Exfiltration & Disclosure
- Collected thousands of documents, including details on surveillance programs.  
- Disclosed materials to journalists, leading to global media coverage.  

### 4. Aftermath
- Immediate fallout: massive reputational damage to U.S. intelligence.  
- Political and legal consequences worldwide.  
- Prompted global debate on surveillance vs. privacy.  

---

## Prevention Measures

### Technical Controls
- **Least Privilege**: Restrict admin accounts to only system maintenance, not data access.  
- **Privileged Access Management (PAM)**: Require just-in-time elevation with session recording.  
- **User Behavior Analytics (UBA/UEBA)**: Monitor for abnormal activity like mass downloads or unusual system access.  
- **Two-Person Integrity Controls**: Require dual approval for accessing highly classified data.  

### Policy/Process Controls
- **Segregation of Duties**: Separate “system admin” roles from “data access” roles.  
- **Insider Threat Programs**: Continuous vetting of contractors and staff in sensitive roles.  
- **Regular Audits**: Independent review of privileged account activity.  

---

## Lessons Learned
- Insider threats are often more dangerous than outside attackers, because insiders already have trust and access.  
- **Contractors** can be just as high-risk as employees, and need equivalent oversight.  
- A single person with overprivileged, unmonitored access can cause **catastrophic damage**.  
- Detection must focus not only on external threats, but also on **abnormal behavior from trusted users**.  

---

## SOC / Blue Team Mapping
- **Monitoring**: Treat privileged account activity as high-severity events in SIEM.  
- **Data Loss Prevention (DLP)**: Detect mass transfers of sensitive data.  
- **Access Control**: Ensure admin roles cannot read or exfiltrate sensitive content.  
- **Threat Hunting**: Regularly search for “Snowden-like” anomalies (off-hours logins, large downloads, new system access).  
- **Incident Response Playbooks**: Have clear escalation paths for insider threat alerts.  

---

## Key Takeaway
The Snowden case shows that **insider threats are not hypothetical — they can cause historic breaches.**  
Organizations must enforce **least privilege, strong monitoring, and two-person controls** to prevent one individual from undermining entire systems.
