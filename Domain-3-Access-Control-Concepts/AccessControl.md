# Access Control Concepts

## Introduction

This document covers the fundamental concepts of access control, detailing the various types of physical and logical controls and explaining how they are combined to strengthen the overall security of an organization. Effective access control is the cornerstone of information security, ensuring that the right people have the right access to the right resources at the right time.

---

## Module 1: Understand Access Control Concepts

*Domain D3.1, D3.1.3, D3.1.5, D3.2, D3.2.1, D3.2.2, D3.2.5*

### What is Security Control?

At its core, access control involves **limiting what objects can be available to what subjects according to what rules**. It's the selective restriction of access to a resource.

### Controls Overview

Security all comes down to a fundamental question: **“Who can get access to organizational assets, and what can they do when they get there?”**

Access controls are not just about restricting access but also about **enabling legitimate access**. The goal is to grant the appropriate level of access to authorized personnel and processes while denying access to all others.

Access is based on three core elements:

* **Subjects**: 👤 A subject is any entity that requests access to a resource. This is the **active** component in the access control model.
    * Examples include a **user**, a **process**, a program, a client, or a device like a smartphone.
    * Subjects initiate requests and should have a defined level of clearance or permissions.

* **Objects**: 📦 An object is the resource or asset that a subject is trying to access. This is the **passive** component.
    * Examples include data files, databases, systems, applications, or even physical assets like a server room.

* **Rules**: 📜 Rules define the conditions under which a subject can access an object. They are the foundation of the access control policy.
    * These rules can be based on user roles, time of day, location, or other attributes to ensure access is managed consistently and securely.

### Defense in Depth

Defense in Depth is an information security strategy that integrates people, technology, and operations to establish multiple, variable barriers against attacks. It applies countermeasures in a layered fashion to fulfill security objectives.

A technical example is **multi-factor authentication (MFA)**, where a password (something you know) is combined with a code from your phone (something you have). Another example is using multiple firewalls to segment and protect sensitive networks.

A non-technical example involves the layers required to access a physical data center: a perimeter fence, a locked building door, a keycard for the server room, and a final key for the server rack itself.



### Principle of Least Privilege (PoLP)

The **Principle of Least Privilege (`PoLP`)** is a standard of permitting only the **minimum access necessary** for users or programs to fulfill their function. Each user is granted access only to the items they absolutely need to perform their specific job or task, and nothing more. This is a foundational concept in **Privileged Access Management (`PAM`)**.

For example, a billing department employee can view financial data, but only a senior manager in that department can modify or delete it.

#### Need-to-Know

Closely related to `PoLP` is the **Need-to-Know** principle. While `PoLP` is about *permissions* (what a user is authorized to do), Need-to-Know is about *access to information*. A user might have the technical permissions to access all files on a server (`PoLP`), but they should only access the specific files they need to know about to do their job (Need-to-Know).

### Privileged Accounts

Privileged accounts are those with **elevated permissions** beyond those of normal users. These accounts pose a significant risk if compromised and require stricter controls.

* **Who uses them?** System administrators, help desk staff, security analysts, etc.
* **What measures are used?**
    * More extensive and detailed **logging**.
    * More stringent access control, such as **MFA** and **just-in-time access**.
    * Deeper trust verification, like enhanced **background checks**.
    * More frequent **auditing** of account activity.

### Segregation of Duties (SoD)

**Segregation of Duties (`SoD`)** is a security practice ensuring that **no one person should control an entire high-risk transaction from start to finish**. It breaks transactions into separate parts, requiring different people to execute each part. This helps prevent fraud and detect errors.

* **Collusion**: When two or more individuals conspire to bypass `SoD` controls.
* **Dual Control**: A specific type of `SoD` where two individuals must be present to perform a task, like two people using separate combinations to open a bank vault.
* **Two-Person Rule**: Requires a minimum of two people to be in a high-security area together, used for both security (preventing insider threats) and life safety.

### The User Access Lifecycle

Properly managing user access from hiring to departure is critical. This is often called the **Identity and Access Management (`IAM`) lifecycle**.

1.  **Provisioning (Onboarding)**: When a new employee is hired or changes position, an account is created or modified. Access rights should be based on pre-defined roles, not copied from another user's profile.
2.  **Access Review**: Permissions should be reviewed periodically (e.g., quarterly or annually) to ensure they are still appropriate and to correct for "privilege creep," where users accumulate unnecessary permissions over time.
3.  **De-provisioning (Offboarding)**: When an employee leaves, their account must be **immediately disabled**. It should be deleted after a set period to preserve audit trails, but access must be revoked instantly to prevent post-employment security incidents.

---

## Module 2: Understand Physical Access Controls

*Domain D3.1, D3.1.1, D3.1.2*

### What Are Physical Security Controls?

Physical access controls are items you can physically touch. They are mechanisms deployed to prevent, monitor, or detect direct contact with systems or areas within a facility. The security of **personnel always comes first**, followed by securing other physical assets.

### Types of Physical Access Controls

Physical controls can be categorized by their function:

* **Deterrent Controls**:  dissuade potential attackers.
    * Examples: Fences, warning signs, security guards, guard dogs.
* **Preventive Controls**: physically block unauthorized access.
    * Examples: Locks, fences, mantraps, turnstiles, cable locks.
* **Detective Controls**: identify and report an access attempt in progress.
    * Examples: Motion detectors, cameras (`CCTV`), alarm systems, logs.
* **Corrective Controls**: implemented after an incident to mitigate damage.
    * Example: Fire suppression systems.
* **Compensating Controls**: provide an alternative to a primary control.
    * Example: A security guard acts as a compensating control if a door lock is broken.

#### Badge Systems and Gate Entry

Access control systems use badges or tokens to identify authorized employees. Card types include bar codes, magnetic stripes, proximity cards, and smart cards. High-security environments may also integrate **biometrics** during enrollment. The system logs all access attempts—both authorized and unauthorized.

#### Environmental Design (CPTED)

**Crime Prevention through Environmental Design (`CPTED`)** uses architectural and environmental design to create safer workspaces. Key principles include:

* **Natural Surveillance**: Designing spaces to be open and visible (e.g., good lighting, low hedges) to discourage criminal activity.
* **Natural Access Control**: Using walkways, fences, and landscaping to guide people to proper entrances and away from restricted areas.
* **Territorial Reinforcement**: Using signs, landscaping, and fences to clearly define property lines and establish a sense of ownership.

#### Biometrics

Biometrics use unique human characteristics for authentication.

* **Physiological**: Fingerprints, iris scans, retinal scans, palm scans.
* **Behavioral**: Voiceprints, signature dynamics, keystroke dynamics.

While accurate, biometrics can be expensive and raise privacy concerns.

### Monitoring

* **Cameras (`CCTV`)**: A flexible method for surveillance. They can deter crime, detect incidents, and provide forensic evidence if recorded.
* **Logs**: Physical logs (e.g., a sign-in sheet) or electronic logs from badge systems record access events. They are essential for audits and forensic investigations and must be protected from tampering.
* **Security Guards**: An effective and flexible control that can deter, prevent, and respond to incidents in real-time.
* **Alarm Systems**: Alert personnel to unauthorized access (e.g., a forced door), environmental hazards (e.g., a fire alarm), or emergencies (e.g., a panic button).

---

## Module 3: Understand Logical Access Controls

*Domain D3.2, D3.2.3, D3.2.4, D3.2.5*

### What are Logical Access Controls?

Logical access controls are electronic methods that limit access to systems, data, and applications. They are the rules and configurations that enforce access policies within the digital environment.

### Access Control Models

There are several models for implementing logical access control.

#### Discretionary Access Control (DAC)

In a **`DAC`** model, the **owner of an object controls who can access it**. If you create a file, you can decide who else gets to read or edit it. This is the most common and flexible model, used by most operating systems like Windows and Linux.

* **Control**: Managed by the data owner.
* **Major Weakness**: Relies on the user's discretion, which can lead to inconsistent security and accidental data exposure.

#### Mandatory Access Control (MAC)

In a **`MAC`** model, access is controlled by a **central authority based on security classifications (or labels)**. A user is given a clearance level (e.g., "Secret"), and they can only access objects with a matching or lower classification level (e.g., "Secret" or "Unclassified"). Users cannot change access permissions, even for objects they create.

* **Control**: Managed by a central administrator based on security labels.
* **Use Case**: Common in military and high-security government environments where confidentiality is paramount.

#### Role-Based Access Control (RBAC)

In an **`RBAC`** model, access is assigned to **roles** rather than directly to individual users. Users are then assigned to roles. For example, instead of giving 50 individual employees access to the accounting system, you create an "Accountant" role with the necessary permissions and assign all 50 employees to that role.

* **Control**: Managed by an administrator who defines roles and assigns users to them.
* **Benefit**: Highly scalable and simplifies administration, especially in large organizations. It is the most common model used in corporate environments.
* **Risk**: **Privilege Creep**, where users accumulate roles and permissions over time and retain them even after changing jobs.

#### Attribute-Based Access Control (ABAC)

**`ABAC`** is a more modern and dynamic model. Access is granted based on a combination of **attributes** about the **subject, object, and environment**. A policy engine evaluates these attributes against established rules in real time.

* **Example Rule**: "Allow *Doctors* (subject attribute) to access *Medical Records* (object attribute) for *their own patients* (relationship attribute) during *business hours* (environment attribute) from a *hospital-managed device* (environment attribute)."
* **Benefit**: Extremely flexible and granular, ideal for complex and dynamic environments like cloud computing and IoT.

### Comparison of Logical Access Control Models

| Model | Who Controls Access? | Granularity | Common Use Case |
| :---- | :-------------------- | :---------- | :------------------ |
| **DAC** | Data Owner | Low (User/Group) | Standard Operating Systems |
| **MAC** | System Administrator | Low (Security Labels) | Military, High-Security Government |
| **RBAC**| System Administrator | Medium (Roles) | Most Corporate Enterprises |
| **ABAC**| Policy Administrator | High (Attributes) | Cloud, IoT, Dynamic Systems |
