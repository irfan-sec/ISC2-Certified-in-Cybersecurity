# Incident Response, Business Continuity & Disaster Recovery

## Introduction

In cybersecurity, the principle of **Availability** ensures that systems and data are accessible when needed. **Incident Response (`IR`)**, **Business Continuity (`BC`)**, and **Disaster Recovery (`DR`)** are the core frameworks that uphold this principle. They work together as a tiered strategy to keep an organization resilient against disruptions.

`Incident Response (IR)` -> `Business Continuity (BC)` -> `Disaster Recovery (DR)`

* **Incident Response (`IR`)**: The immediate, tactical reaction to a security event to contain the issue and keep the business operating.
* **Business Continuity (`BC`)**: The strategic plan to sustain essential business functions during a crisis.
* **Disaster Recovery (`DR`)**: The process of restoring IT infrastructure and data after a catastrophic event, activated when IR and BC are insufficient.

---

## Module 1: Understand Incident Response

*Domain D2.3.1, D2.3.2, D2.3.3*

### Incident Terminology

* **Breach**: The confirmed loss of control or unauthorized access to **Personally Identifiable Information (`PII`)** or other sensitive data.
* **Event**: **Any observable occurrence** in a network or system. Most events are benign.
* **Exploit**: **A particular attack** that takes advantage of a system vulnerability.
* **Incident**: An **event that actually or potentially jeopardizes** the confidentiality, integrity, or availability (`CIA`) of an information system.
* **Intrusion**: A deliberate security incident where an attacker gains, or attempts to gain, unauthorized access to a system.
* **Threat**: **Any circumstance or event with the potential to cause harm** to organizational assets or operations.
* **Vulnerability**: A **weakness** in a system, process, or control that could be exploited by a threat.
* **Zero-Day**: A previously **unknown system vulnerability** for which no patch or fix exists.

### The Goal of Incident Response 🛡️

The priority of any incident response is to **protect life, health, and safety**. The primary goal of incident management is to **be prepared** with a plan that guides the organization through a crisis, reduces the impact of an incident, and allows for the rapid resumption of operations.

### The Incident Response Lifecycle

An Incident Response Plan (`IRP`) is a living document that outlines the technical processes, checklists, and tools to be used during an incident. The process typically follows a standard lifecycle.

1.  **Preparation**: This is the most critical phase. It involves developing a policy, **identifying critical assets**, training staff, and forming an Incident Response Team. It's crucial to plan for communication failures by establishing alternate methods.
2.  **Detection and Analysis**: Monitoring all possible attack vectors to identify an incident. Once detected, the incident is analyzed to determine its scope and priority, and all findings are documented.
3.  **Containment, Eradication, and Recovery**:
    * **Containment**: Taking immediate steps to stop the incident from causing further damage. This can involve isolating the affected systems from the network.
    * **Eradication**: Identifying and removing the root cause of the incident (e.g., eliminating the malware, patching the vulnerability).
    * **Recovery**: Restoring affected systems to normal operation and confirming they are secure.
4.  **Post-Incident Activity (Lessons Learned)**: After the incident is resolved, the team holds a retrospective meeting to analyze what happened, what worked, and what didn't. This phase focuses on documenting lessons learned to improve the preparation for future incidents.

### Incident Response Team

A cross-functional group is needed to manage an incident effectively. This team is often called a **Computer Incident Response Team (`CIRT`)** or a **Computer Security Incident Response Team (`CSIRT`)**.

**Potential Team Members**:
* Senior Management Representative
* Information Security Professionals
* Legal Representatives
* Public Affairs / Communications
* System and Network Engineers

**Primary Responsibilities**:
* Determine the scope and damage of the incident.
* Determine if any confidential information was compromised.
* Implement recovery procedures to restore security.
* Supervise the implementation of new security measures to prevent recurrence.

---

## Module 2: Understand Business Continuity (BC)

*Domain D2.1.1, D2.1.2, D2.1.3*

### The Importance of Business Continuity 📈

The goal of a **Business Continuity Plan (`BCP`)** is to **sustain essential business operations while recovering from a significant disruption**. This is a business-focused plan, not just an IT plan. **Communication** is a key part of the BCP, and it requires including management to authorize actions and make priority decisions during a crisis.

### Key Business Continuity Metrics

* **Recovery Time Objective (`RTO`)**: The **maximum acceptable amount of time** a system or function can be down after a disaster or failure. *Example: "The e-commerce website must be back online within 2 hours of an outage."*
* **Recovery Point Objective (`RPO`)**: The **maximum acceptable amount of data loss**, measured in time. It defines the point in time to which data must be restored. *Example: "We can tolerate losing no more than 15 minutes of transaction data."*



### Components of a Business Continuity Plan

A `BCP` is created by members from across the organization to ensure all critical processes are included.

* List of BCP team members with multiple contact methods.
* Immediate response procedures and checklists (safety, fire suppression, etc.).
* Notification systems and call trees.
* Guidance for management on decision-making authority.
* Clear criteria for when and how to enact the plan.
* Contact numbers for critical supply chain vendors, partners, and emergency services.

### Testing the Business Continuity Plan

A `BCP` should be tested routinely. Common testing methods include:

* **Walk-through/Tabletop Exercise**: Team members gather to discuss their roles and responses to a hypothetical scenario.
* **Simulation**: A more active test where the team responds to a simulated incident in a test environment.
* **Full Interruption**: A complete test that involves shutting down primary systems and failing over to the backup site. This is the most thorough but also the most disruptive and risky type of test.

---

## Module 3: Understand Disaster Recovery (DR)

*Domain D2.2, D2.2.1, D2.2.2, D2.2.3*

### The Goal of Disaster Recovery 🚒

Disaster Recovery (`DR`) begins where Business Continuity leaves off. While `BC` is about keeping the business running during a crisis, `DR` is about **restoring the IT and communications infrastructure** back to full operations after a disaster. A **Disaster Recovery Plan (`DRP`)** is a subset of the overall `BCP`.

### Components of a Disaster Recovery Plan

* An executive summary of the plan.
* Department-specific recovery plans.
* Technical guides for IT personnel to restore systems.
* Checklists for critical team members to guide their actions.
* A communication plan managed by Public Relations.
* Formal approval from executive management.

### Disaster Recovery Alternate Sites

A critical component of a `DRP` is having an alternate location to recover IT operations. There are three main types of recovery sites:

| Site Type | Description | Readiness | Cost |
| :-------- | :---------- | :-------- | :--- |
| **Hot Site** ♨️ | A fully configured and operational data center with all necessary hardware, software, and real-time data synchronization. | Immediate (Minutes to hours) | High |
| **Warm Site** 🌤️ | A data center with all the necessary hardware installed but not necessarily configured or running. Data may not be fully synchronized. | Moderate (Hours to days) | Medium |
| **Cold Site** 🧊 | An empty data center with only basic infrastructure like power, cooling, and networking. All hardware and software must be brought in and installed. | Slow (Days to weeks) | Low |

The choice of site depends on the organization's `RTO` and budget. A bank might require a hot site for its critical transaction systems, while a less time-sensitive business function might be adequately served by a cold site.
