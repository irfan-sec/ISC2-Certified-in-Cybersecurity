# Domain 2: Incident Response, Business Continuity & Disaster Recovery - Practice Questions

---

## 🚨 Incident Response Questions

### Question 1: Incident vs Event
**Question:** What is the primary difference between a security event and a security incident?

* Events are more serious than incidents
* **Incidents actually or potentially jeopardize the CIA triad, while events are just observable occurrences**
* Events occur internally while incidents are external
* Incidents require legal action while events do not

**Answer:** **Incidents actually or potentially jeopardize the CIA triad, while events are just observable occurrences**.

**Explanation:** A security **event** is any observable occurrence in a network or system, and most events are benign (like a user logging in). A security **incident** is an event that actually or potentially compromises the confidentiality, integrity, or availability of information systems. Not all events are incidents, but all incidents start as events that are determined to pose a security risk.

---

### Question 2: Incident Response Phases
**Question:** According to the standard incident response lifecycle, what comes immediately after "Detection and Analysis"?

* Post-Incident Activity
* Preparation
* **Containment, Eradication, and Recovery**
* Evidence Collection

**Answer:** **Containment, Eradication, and Recovery** comes after Detection and Analysis.

**Explanation:** The incident response lifecycle follows this order: 1) Preparation, 2) Detection and Analysis, 3) Containment, Eradication, and Recovery, 4) Post-Incident Activity. Once an incident has been detected and analyzed to understand its scope and impact, the immediate priority is to contain the damage, remove the threat, and restore normal operations.

---

### Question 3: Incident Response Team Responsibilities
**Question:** What is the PRIMARY responsibility of an incident response team when an incident occurs?

* Identify the attacker's identity and motives
* **Determine the scope and damage of the incident**
* Notify law enforcement immediately
* Restore all systems to previous configurations

**Answer:** The primary responsibility is **to determine the scope and damage of the incident**.

**Explanation:** The incident response team's first priority is to understand what happened, how extensive the damage is, and what systems or data have been affected. This assessment drives all subsequent response actions. While identifying attackers and restoring systems may be important, understanding the scope and impact is the foundational step that enables effective response decisions.

---

### Question 4: Zero-Day Vulnerabilities
**Question:** What is the key characteristic that makes a zero-day vulnerability particularly dangerous?

* It affects multiple operating systems
* It can be exploited remotely
* **No patch or signature exists to detect or prevent exploitation**
* It requires administrative privileges to exploit

**Answer:** **No patch or signature exists to detect or prevent exploitation**.

**Explanation:** A zero-day vulnerability is a security flaw that is unknown to the software vendor and security community. Because it's unknown, there is no patch available to fix it, and security tools don't have signatures to detect its exploitation. This makes zero-day vulnerabilities particularly dangerous because traditional defenses are ineffective against them.

---

### Question 5: Incident Containment Strategy
**Question:** During the containment phase of incident response, what is the primary goal?

* Completely eliminate the threat
* Gather evidence for prosecution
* **Prevent the incident from spreading and causing additional damage**
* Restore all affected systems

**Answer:** The primary goal is **to prevent the incident from spreading and causing additional damage**.

**Explanation:** Containment focuses on limiting the scope and magnitude of the incident to prevent it from spreading to other systems or causing additional damage. This might involve isolating affected systems, blocking network access, or disabling certain functions. Eradication (elimination) and recovery come after containment, while evidence gathering occurs throughout the process.

---

## 🏢 Business Continuity Questions

### Question 6: Business Continuity vs Disaster Recovery
**Question:** What is the primary distinction between Business Continuity Planning (BCP) and Disaster Recovery Planning (DRP)?

* BCP is for natural disasters while DRP is for cyber attacks
* **BCP focuses on business operations while DRP focuses on IT systems recovery**
* BCP is long-term while DRP is short-term
* BCP and DRP are interchangeable terms

**Answer:** **BCP focuses on business operations while DRP focuses on IT systems recovery**.

**Explanation:** Business Continuity Planning (BCP) is the holistic strategy to keep the entire business functional during a disruption, covering people, processes, and facilities. Disaster Recovery Planning (DRP) is a subset of BCP that specifically focuses on restoring IT infrastructure and systems after a disaster. BCP ensures business operations continue; DRP ensures IT systems are restored.

---

### Question 7: Recovery Time Objective (RTO)
**Question:** What does Recovery Time Objective (RTO) represent?

* The amount of data that can be lost during an incident
* The cost of recovering from a disaster
* **The maximum acceptable time a system can be unavailable**
* The time needed to create a backup

**Answer:** RTO represents **the maximum acceptable time a system can be unavailable**.

**Explanation:** Recovery Time Objective (RTO) defines the maximum amount of downtime that an organization can tolerate for a particular system or business function. It helps prioritize recovery efforts and determine appropriate business continuity strategies. For example, if a critical system has an RTO of 2 hours, the organization must be able to restore that system within 2 hours of an outage.

---

### Question 8: Recovery Point Objective (RPO)
**Question:** Recovery Point Objective (RPO) is primarily concerned with:

* System uptime requirements
* **Maximum acceptable data loss measured in time**
* Recovery cost limitations
* Number of backup copies needed

**Answer:** RPO is concerned with **maximum acceptable data loss measured in time**.

**Explanation:** Recovery Point Objective (RPO) defines the maximum amount of data loss an organization can tolerate, measured in time. For example, an RPO of 15 minutes means the organization can tolerate losing up to 15 minutes worth of data. This drives backup frequency and replication strategies - if you can only lose 15 minutes of data, you need backups or replication at least every 15 minutes.

---

### Question 9: Business Impact Analysis (BIA)
**Question:** What is a key outcome of conducting a Business Impact Analysis (BIA)?

* Determining insurance requirements
* **Identifying critical business functions and their dependencies**
* Calculating disaster recovery costs
* Selecting backup technologies

**Answer:** A key outcome is **identifying critical business functions and their dependencies**.

**Explanation:** A Business Impact Analysis (BIA) identifies an organization's most critical business functions and processes, analyzes how they depend on each other and on IT systems, and determines the impact of disruptions over time. This analysis is fundamental to business continuity planning because it helps prioritize recovery efforts and determine RTO/RPO requirements for different systems and processes.

---

### Question 10: BCP Testing Methods
**Question:** Which type of business continuity plan testing is the most comprehensive but also carries the highest risk?

* Walk-through/Tabletop exercise
* Simulation testing
* **Full interruption testing**
* Documentation review

**Answer:** **Full interruption testing** is the most comprehensive and highest risk.

**Explanation:** Full interruption testing involves actually shutting down primary systems and failing over to backup sites or alternate procedures. While this provides the most realistic test of the business continuity plan, it also carries the highest risk because it could cause actual business disruption if the test fails or if problems occur during the failback process.

---

## 🔥 Disaster Recovery Questions

### Question 11: Disaster Recovery Site Types
**Question:** Which type of disaster recovery site can be operational within minutes to hours after a disaster?

* Cold site
* Warm site
* **Hot site**
* Mobile site

**Answer:** A **hot site** can be operational within minutes to hours.

**Explanation:** A hot site is a fully configured and operational data center with real-time data synchronization. Since it's already running and has current data, it can take over operations very quickly. A warm site has hardware but may not be fully configured or have current data, while a cold site is just empty space that requires hardware installation and configuration.

---

### Question 12: Hot Site Characteristics
**Question:** What is the primary characteristic of a hot site in disaster recovery planning?

* Lowest cost option for disaster recovery
* **Fully operational with real-time data synchronization**
* Requires manual data restoration from backups
* Takes days to weeks to become operational

**Answer:** The primary characteristic is **fully operational with real-time data synchronization**.

**Explanation:** A hot site is a complete duplicate of the primary data center that is fully configured, operational, and continuously synchronized with the primary site. This allows for immediate or near-immediate failover in case of a disaster. While hot sites provide the fastest recovery times, they are also the most expensive disaster recovery option.

---

### Question 13: Data Backup Importance
**Question:** Why are data backups considered the most critical component of any disaster recovery plan?

* They are required by regulations
* They are the least expensive recovery option
* **They provide the source material for restoring lost data and systems**
* They eliminate the need for redundant systems

**Answer:** Backups are critical because **they provide the source material for restoring lost data and systems**.

**Explanation:** Data backups are the foundation of disaster recovery because they contain the information needed to rebuild systems and restore business operations after a catastrophic failure. Without reliable, current backups, data lost in a disaster may be gone forever, making true recovery impossible. Hardware can be replaced, but unique business data cannot be recreated.

---

### Question 14: DRP Executive Summary Purpose
**Question:** What is the primary purpose of the Executive Summary in a Disaster Recovery Plan?

* To provide detailed technical procedures
* **To offer a high-level overview for senior management**
* To list emergency contact information
* To serve as a checklist for IT staff

**Answer:** The purpose is **to offer a high-level overview for senior management**.

**Explanation:** The Executive Summary is designed for senior leadership and provides a concise overview of the entire Disaster Recovery Plan, including its purpose, scope, key objectives, and strategic importance. It allows executives to understand the plan's value and approve its implementation without needing to read technical details.

---

### Question 15: Business Continuity Support
**Question:** Who must provide support for business continuity planning efforts to ensure success?

* External consultants
* IT department managers
* **Executive management or senior leadership**
* Frontline employees

**Answer:** Support must come from **executive management or senior leadership**.

**Explanation:** Business continuity planning requires significant resources, budget, and cross-departmental cooperation. Without visible support and sponsorship from executive management, the effort will likely fail to get the necessary authority, funding, and cooperation from different departments. Senior leadership support is crucial for overcoming organizational resistance and ensuring adequate resource allocation.

---

## 📋 Communication and Notification Questions

### Question 16: Notification Systems Purpose
**Question:** Why are notification systems and call trees important in a business continuity plan?

* To contact customers about service disruptions
* To coordinate with emergency responders
* **To rapidly alert personnel when the BCP is being activated**
* To document the incident for legal purposes

**Answer:** They are important **to rapidly alert personnel when the BCP is being activated**.

**Explanation:** When a disaster strikes, rapid and clear communication is critical. Notification systems and call trees ensure that all relevant personnel - from the response team to general staff and key stakeholders - are informed quickly about the activation of the Business Continuity Plan. This enables a coordinated and effective response where everyone knows their roles and responsibilities.

---

### Question 17: Red Book Purpose
**Question:** In business continuity planning, what is the purpose of maintaining a "red book"?

* To document lessons learned from past incidents
* **To serve as a hard copy backup accessible outside the facility**
* To track employee emergency contact information
* To record real-time incident updates

**Answer:** The purpose is **to serve as a hard copy backup accessible outside the facility**.

**Explanation:** The "red book" is a physical, printed copy of the business continuity plan kept at a secure, offsite location. In a disaster where primary facilities and electronic systems are inaccessible, the red book ensures that key personnel can still access critical plans, contact lists, and procedures needed to manage the response and recovery efforts.

---

### Question 18: Communication Network Resilience
**Question:** In the United States, what type of networks are designed to maintain essential communications during severe cyberattacks?

* Commercial cellular networks
* Internet-based networks
* **Military-grade networks**
* Hospital-specific networks

**Answer:** **Military-grade networks** are designed for this purpose.

**Explanation:** Military-grade networks are specifically designed with high levels of resilience, redundancy, and security to ensure they can operate under extreme conditions, including widespread cyberattacks. These networks serve as a fallback for maintaining essential national security and government functions when commercial communication infrastructures may be compromised or unreliable.

---

## 🔍 Incident Analysis Questions

### Question 19: Intrusion Definition
**Question:** An external entity attempting to gain unauthorized access to your organization's IT environment is an example of:

* An event
* **An intrusion**
* A vulnerability
* Malware

**Answer:** This is an example of **an intrusion**.

**Explanation:** An intrusion is any attempt to compromise the confidentiality, integrity, or availability of a system, or to bypass its security mechanisms. An unauthorized attempt to access an IT environment, whether successful or not, fits the definition of an intrusion attempt. This is more specific than just an "event" and represents a deliberate security incident.

---

### Question 20: Incident Detection Example
**Question:** A user reports that they cannot log in despite using correct credentials, and investigation reveals their account has been compromised. This scenario represents:

* Risk management
* **Incident detection**
* Vulnerability assessment
* Preventive control failure

**Answer:** This represents **incident detection**.

**Explanation:** This scenario demonstrates the incident detection process: receiving an alert (user's call), investigating the issue, and confirming that a security incident (compromised account) has occurred. Detection is the phase where potential problems are identified and confirmed as actual security incidents requiring response.

---

## Summary

These practice questions cover the essential concepts from Domain 2: Incident Response, Business Continuity & Disaster Recovery, including:

- **Incident Response**: Phases, team responsibilities, and containment strategies
- **Business Continuity**: BCP vs DRP, RTO/RPO concepts, and testing methods
- **Disaster Recovery**: Site types, backup importance, and executive support
- **Communication**: Notification systems and resilient networks
- **Incident Analysis**: Detection and classification of security events

Understanding these concepts is crucial for the 10% of the CC exam that focuses on this domain. Focus on the practical application of these concepts in real-world incident response and business continuity scenarios.