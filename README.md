# Incident Reporting & Communication Framework: "Who Did What, Why, How, So What, Now What"

This communication model is adapted from reflective and storytelling frameworks used in education, healthcare, and leadership. It helps responders structure clear, audience-tailored summaries during incident response reporting.

## Attribution
This framework is inspired by:
- **"Somebody Wanted But So" (SWBS) strategy** -  widwly used in education to help students summarize, originator is not well-documented
- **Borton's Developmental Model (1970)** – "What? So What? Now What?"
- **Driscoll's Model of Reflection**
- **Rolfe et al.'s Reflective Model (2001)**

These models were developed to promote reflection and critical thinking and have been adapted here for incident responders.

---

## Framework Overview

| **Component** | **Explanation** | **Tips for Use** |
|---------------|-----------------|------------------|
| **Who**       | Who was involved (attacker, insider, external actor) | Use generic terms for non-technical audiences |
| **Did What**  | What action they took (e.g., phishing, exfiltration) | Focus on the behavior, not just the alert |
| **Why**       | Likely motivation (e.g., access data, install malware) | Make intent relatable: theft, disruption, etc. |
| **How**       | TTPs, entry points, tools used | Include MITRE references for technical peers |
| **So What**   | Impact or risk posed | Emphasize business impact, compliance, downtime |
| **Now What**  | Actions taken or recommended | Show containment, response, and future steps |

---

## Audience-Specific Examples

### 1. Technical Peers

> **Who:** External actor with suspected FIN7 tactics  
> **Did What:** Sent credential phishing emails via spoofed domain  
> **Why:** To gain access and move laterally  
> **How:** HTML smuggling + fake O365 login page (MITRE T1566.002)  
> **So What:** Credential use detected in VPN logs; potential pivot point  
> **Now What:** Blocked domains, reset creds, added detections for lateral movement

---

### 2. Executive Leadership / Board

> **Who:** An external threat actor targeted our workforce  
> **Did What:** They launched a phishing campaign to steal credentials  
> **Why:** Likely to access sensitive internal systems and data  
> **How:** Used a professional-looking fake login page  
> **So What:** A successful compromise could've led to data exfiltration and financial loss  
> **Now What:** The threat was detected early; accounts were secured; ongoing monitoring in place

---

### 3. Legal/Compliance

> **Who:** Unknown external actor  
> **Did What:** Attempted unauthorized access via phishing  
> **Why:** Potential motive includes data theft or regulatory impact  
> **How:** Phishing email bypassed spam filter; linked to spoofed login  
> **So What:** No confirmed data breach, but access attempt to regulated data zone  
> **Now What:** Reviewed DLP logs, documented in case register, issued internal memo

---

### 4. Non-Technical Colleagues

> **Who:** A cybercriminal tried to target our company  
> **Did What:** They sent fake emails pretending to be company notices  
> **Why:** To trick someone into giving away their login  
> **How:** Linked to a site that looked like our login page  
> **So What:** No one fell for it, but it could have been serious  
> **Now What:** We blocked the site and are sending reminders to stay alert

---

### 5. Public Relations (PR)

> **Who:** An external attacker targeting enterprise users  
> **Did What:** Tried to collect login credentials through a phishing email  
> **Why:** Likely aimed to compromise systems and leak information  
> **How:** Professional spoofing of company branding and login pages  
> **So What:** No breach confirmed, and controls worked as intended  
> **Now What:** Incident contained; optional holding statement prepared if disclosure becomes necessary

---

### 6. Human Resources (Insider Threat)

> **Who:** A current employee with elevated access privileges  
> **Did What:** Attempted to download large quantities of internal documents to a personal device  
> **Why:** Under investigation for potential policy violation or preparing to exit the company  
> **How:** Used legitimate credentials and tools outside of normal business hours  
> **So What:** Potential violation of company policy and data protection rules; risk of intellectual property loss  
> **Now What:** Account access restricted, HR notified, internal investigation initiated, documentation prepared for possible disciplinary action

---

### 7. Mixed Audience (Technical + Non-Technical) with Clarifications

> **Who:** An external attacker leveraging credential stuffing techniques — (which means they tried lots of usernames and passwords from previous breaches to see if any still worked).
> **Did What:** They launched an automated login attack against our VPN portal — (a bot rapidly entered credentials into our remote access system).
> **Why:** The likely goal was to find a valid account with access to internal systems — (in other words, they wanted a backdoor into our network).
> **How:** They used a scripted tool to send login requests from multiple IPs — (this helps them avoid detection and try as many combos as possible).
> **So What:** Most attempts failed, but one account showed signs of partial access before it was locked — (this could have allowed them to move further into the network if we hadn’t caught it).
> **Now What:** Now What: We’ve blocked the source IPs, reset credentials, and are reviewing logs for any other unusual activity — (we’re locking down what they touched, checking for signs of deeper access, and improving detection going forward).

---
## Tips for Use

- Tailor the **depth of technical detail** based on the audience
- Use the **"So What"** section to connect the incident to real business consequences
- Keep **"Now What"** action-focused to reassure stakeholders
- Consider **visuals or diagrams** for executive, PR, and HR audiences

---

*Prepared by: Martha Sosa  
Inspired by foundational communication and reflection models.*
