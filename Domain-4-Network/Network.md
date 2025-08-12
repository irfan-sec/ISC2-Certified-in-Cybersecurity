#Network Security

---

## Module 1: Understand Computer Networking

*Domain D4.1.1, D4.1.2*

### What is Networking

A network is simply two or more computers linked together to share data, information or resources.

To properly establish secure data communications, it is important to explore all of the technologies involved in computer communications. From hardware and software to protocols and encryption and beyond, there are many details, standards and procedures to be familiar with.

#### Types of Networks

There are two basic types of networks:

* **Local area network (LAN)** - A local area network (LAN) is a network typically spanning a single floor or building. This is commonly a limited geographical area.
* **Wide area network (WAN)** - Wide area network (WAN) is the term usually assigned to the long-distance connections between geographically remote networks.

#### Network Devices

* **Hubs** are used to connect multiple devices in a network. They’re less likely to be seen in business or corporate networks than in home networks. Hubs are wired devices and are not as smart as switches or routers.
* You might consider using a **switch**, or what is also known as an intelligent hub. Switches are wired devices that know the addresses of the devices connected to them and route traffic to that port/device rather than retransmitting to all devices. Offering greater efficiency for traffic delivery and improving the overall throughput of data, switches are smarter than hubs, but not as smart as routers. Switches can also create separate broadcast domains when used to create VLANs, which will be discussed later.
* **Routers** are used to control traffic flow on networks and are often used to connect similar networks and control traffic flow between them. Routers can be wired or wireless and can connect multiple switches. Smarter than hubs and switches, routers determine the most efficient “route” for the traffic to flow across the network.
* **Firewalls** are essential tools in managing and controlling network traffic and protecting the network. A firewall is a network device used to filter traffic. It is typically deployed between a private network and the internet, but it can also be deployed between departments (segmented networks) within an organization (overall network). Firewalls filter traffic based on a defined set of rules, also called filters or access control lists.
* A **server** is a computer that provides information to other computers on a network. Some common servers are web servers, email servers, print servers, database servers and file servers. All of these are, by design, networked and accessed in some way by a client computer. Servers are usually secured differently than workstations to protect the information they contain.
* **Endpoints** are the ends of a network communication link. One end is often at a server where a resource resides, and the other end is often a client making a request to use a network resource. An endpoint can be another server, desktop workstation, laptop, tablet, mobile phone or any other end user device.

#### Other Networking Terms

* **Ethernet (IEEE 802.3)** is a standard that defines wired connections of networked devices. This standard defines the way data is formatted over the wire to ensure disparate devices can communicate over the same cables.
* **Media Access Control (MAC) Address** - Every network device is assigned a Media Access Control (MAC) address. An example is `00-13-02-1F-58-F5`. The first 3 bytes (24 bits) of the address denote the vendor or manufacturer of the physical network interface. No two devices can have the same MAC address in the same local network; otherwise an address conflict occurs.
* **Internet Protocol (IP) Address** - While MAC addresses are generally assigned in the firmware of the interface, IP hosts associate that address with a unique logical address. This logical IP address represents the network interface within the network and can be useful to maintain communications when a physical device is swapped with new hardware. Examples are `192.168.1.1` and `2001:db8::ffff:0:1`.

### Networking Models

Many different models, architectures and standards exist that provide ways to interconnect different hardware and software systems with each other for the purposes of sharing information, coordinating their activities and accomplishing joint or shared tasks.

Computers and networks emerge from the integration of communication devices, storage devices, processing devices, security devices, input devices, output devices, operating systems, software, services, data and people.

Translating the organization’s security needs into safe, reliable and effective network systems needs to start with a simple premise. The purpose of all communications is to exchange information and ideas between people and organizations so that they can get work done.

Those simple goals can be re-expressed in network (and security) terms such as:

* Provide reliable, managed communications between hosts (and users)
* Isolate functions in layers
* Use packets (representation of data at `L3` of OSI model ) as the basis of communication
* Standardize routing, addressing and control
* Allow layers beyond internetworking to add functionality
* Be vendor-agnostic, scalable and resilient

In the most basic form, a network model has at least two layers:

* **UPPER LAYER APPLICATION**: also known as the host or application layer, is responsible for managing the integrity of a connection and controlling the session as well as establishing, maintaining and terminating communication sessions between two computers. It is also responsible for transforming data received from the Application Layer into a format that any system can understand. And finally, it allows applications to communicate and determines whether a remote communication partner is available and accessible.
    * APPLICATION
        * APPLICATION 7
        * PRESENTATION 6
        * SESSION 5
* **LOWER LAYER**: it is often referred to as the media or transport layer and is responsible for receiving bits from the physical connection medium and converting them into a frame. Frames are grouped into standardized sizes. Think of frames as a bucket and the bits as water. If the buckets are sized similarly and the water is contained within the buckets, the data can be transported in a controlled manner. Route data is added to the frames of data to create packets. In other words, a destination address is added to the bucket. Once we have the buckets sorted and ready to go, the host layer takes over.
    * DATA TRANSPORT
        * TRANSPORT 4
        * NETWORK 3
        * DATA LINK 2
        * PHYSICAL 1

### Open Systems Interconnection (OSI) Model

The OSI Model was developed to establish a common way to describe the communication structure for interconnected computer systems. The OSI model serves as an abstract framework, or theoretical model, for how protocols should function in an ideal world, on ideal hardware. Thus, the OSI model has become a common conceptual reference that is used to understand the communication of various hierarchical components from software interfaces to physical hardware.

The OSI model divides networking tasks into seven distinct layers. Each layer is responsible for performing specific tasks or operations with the goal of supporting data exchange (in other words, network communication) between two computers. The layers are interchangeably referenced by name or layer number. For example, Layer 3 is also known as the Network Layer. The layers are ordered specifically to indicate how information flows through the various levels of communication. Each layer communicates directly with the layer above and the layer below it. For example, Layer 3 communicates with both the Data Link (2) and Transport (4) layers.

The Application, Presentation, and Session Layers (5-7) are commonly referred to simply as data. However, each layer has the potential to perform encapsulation. Encapsulation is the addition of header and possibly a footer (trailer) data by a protocol used at that layer of the OSI model. Encapsulation is particularly important when discussing Transport, Network and Data Link layers (2-4), which all generally include some form of header. At the Physical Layer (1), the data unit is converted into binary, i.e., `01010111`, and sent across physical wires such as an ethernet cable.

It's worth mapping some common networking terminology to the OSI Model so you can see the value in the conceptual model. Consider the following examples:

* When someone references an image file like a `JPEG` or `PNG`, we are talking about the **Presentation Layer (6)**.
* When discussing logical ports such as `NetBIOS`, we are discussing the **Session Layer (5)**.
* When discussing `TCP`/`UDP`, we are discussing the **Transport Layer (4)**.
* When discussing routers sending packets, we are discussing the **Network Layer (3)**.
* When discussing switches, bridges or WAPs sending frames, we are discussing the **Data Link Layer (2)**.

Encapsulation occurs as the data moves down the OSI model from Application to Physical. As data is encapsulated at each descending layer, the previous layer’s header, payload and footer are all treated as the next layer’s payload. The data unit size increases as we move down the conceptual model and the contents continue to encapsulate.

The inverse action occurs as data moves up the OSI model layers from Physical to Application. This process is known as **de-encapsulation** (or decapsulation). The header and footer are used to properly interpret the data payload and are then discarded. As we move up the OSI model, the data unit becomes smaller.

| Layer | Name | Encapsulation Process |
| :---: | :----------- | :-------------------- |
| 7 | Application | DATA |
| 6 | Presentation | Header -> &#124; DATA |
| 5 | Session | Header -> &#124;&#124; DATA |
| 4 | Transport | Header -> &#124;&#124;&#124; DATA |
| 3 | Network | Header -> &#124;&#124;&#124;&#124; DATA |
| 2 | Data Link | Header -> &#124;&#124;&#124;&#124;&#124; DATA &#124;&#124; <- Footer |
| 1 | Physical | Header -> &#124;&#124;&#124;&#124;&#124;&#124; DATA &#124;&#124;&#124; |

### Transmission Control Protocol/Internet Protocol (TCP/IP)

The OSI model wasn’t the first or only attempt to streamline networking protocols or establish a common communications standard. In fact, the most widely used protocol today, TCP/IP, was developed in the early 1970s. The OSI model was not developed until the late 1970s. The TCP/IP protocol stack focuses on the core functions of networking.

| TCP/IP Protocol Architecture Layers | Description |
| ----------------------------------- | --------------------------------------- |
| **Application Layer** | Defines the protocols for the transport layer |
| **Transport Layer** | Permits data to move among devices |
| **Internet Layer** | Creates/inserts packets |
| **Network Interface Layer** | How data moves through the network |

The most widely used protocol suite is `TCP/IP`, but it is not just a single protocol; rather, it is a protocol stack comprising dozens of individual protocols. `TCP/IP` is a platform-independent protocol based on open standards. However, this is both a benefit and a drawback. `TCP/IP` can be found in just about every available operating system, but it consumes a significant amount of resources and is relatively easy to hack into because it was designed for ease of use rather than for security.

At the **Application Layer**, TCP/IP protocols include **Telnet**, File Transfer Protocol (**FTP**), Simple Mail Transport Protocol (**SMTP**), and Domain Name Service (**DNS**). The two primary **Transport Layer** protocols of TCP/IP are **TCP and UDP**. **TCP is a full-duplex connection-oriented protocol, whereas UDP is a simplex connectionless protocol**. In the **Internet Layer**, **Internet Control Message Protocol (ICMP)** is used to determine the health of a network or a specific link. **ICMP is utilized by `ping`, `traceroute` and other network management tools**. The `ping` utility employs ICMP echo packets and bounces them off remote systems. Thus, you can use `ping` to determine whether the remote system is online, whether the remote system is responding promptly, whether the intermediary systems are supporting communications, and the level of performance efficiency at which the intermediary systems are communicating.

* **OSI (Application, Presentation, Session)** is equivalent to **TCP/IP (Application Layer)**. Protocol suite: `FTP`, `Telnet`, `SNMP`, `LPD`, `TFTP`, `SMTP`, `NFS`, `X Window`.
* **OSI (Transport)** is equivalent to **TCP/IP (Transport Layer)**. Protocol suite: `TCP`, `UDP`.
* **OSI (Network)** is equivalent to **TCP/IP (Internet Layer)**. Protocol suite: `IGMP`, `IP`, `ICMP`.
* **OSI (Data Link, Physical)** is equivalent to **TCP/IP (Network Interface Layer)**. Protocol suite: `Ethernet`, `Fast Ethernet`, `Token Ring`, `FDDI`.

### Base concepts

* **Switch**: A device that routes traffic to the port of a known device.
* **Server**: A computer that provides information to other computers.
* **Firewall**: A device that filters network traffic based on a defined set of rules.
* **Ethernet**: A standard that defines wired communications of networked devices.
* **IP Address**: Logical address representing the network interface.
* **MAC Address**: Address that denotes the vendor or manufacturer of the physical network interface.

### Internet Protocol (IPv4 and IPv6)

`IPv4` provides a 32-bit address space. `IPv6` provides a 128-bit address space. The first one is exhausted nowadays, but it is still used because of the NAT technology. 32 bits means 4 octets of 8 bits, which is represented in a dotted decimal notation such as `192.168.0.1`, which means in binary notation `11000000 10101000 00000000 00000001`.

IP hosts/devices associate an address with a unique logical address. An `IPv4` address is expressed as four octets separated by a dot (.), for example, `216.12.146.140`. Each octet may have a value between 0 and 255. However, **0 is the network itself (not a device on that network), and 255 is generally reserved for broadcast purposes**. Each address is subdivided into two parts: **the network number and the host**. The network number assigned by an external organization, such as the Internet Corporation for Assigned Names and Numbers (ICANN), represents the organization’s network. The host represents the network interface within the network.

**To ease network administration, networks are typically divided into subnets**. Because subnets cannot be distinguished with the addressing scheme discussed so far, a separate mechanism, **the subnet mask**, is used to define the part of the address used for the subnet. The mask is usually converted to decimal notation like `255.255.255.0`. **With the ever-increasing number of computers and networked devices, it is clear that `IPv4` does not provide enough addresses for our needs.** To overcome this shortcoming, **`IPv4` was sub-divided into public and private address ranges.**

The nature of the addressing scheme established by IPv4 meant that network designers had to start thinking in terms of IP address reuse. The private address groups allow every LAN in every SOHO (small office, home office) situation to use addresses such as `192.168.2.xxx` for its internal network addresses. This table shows the private addresses available for anyone to use:

| Private Address Range |
| ----------------------------- |
| `10.0.0.0` to `10.255.255.254` |
| `172.16.0.0` to `172.31.255.254`|
| `192.168.0.0` to `192.168.255.254`|

The first octet of **127 is reserved for a computer’s loopback address**. Usually, the address `127.0.0.1` is used. **The loopback address is used to provide a mechanism for self-diagnosis and troubleshooting at the machine level**.

**IPv6** is a modernization of `IPv4`, which addressed a number of weaknesses:
* **A much larger address field**: `IPv6` addresses are **128 bits**, which supports `2^128` hosts. **This ensures that we will not run out of addresses**.
* **Improved security**: `IPsec` is an optional part of `IPv4` networks, but a **mandatory component of `IPv6` networks**. This will help ensure the integrity and confidentiality of IP packets.
* **Improved Quality of Service (QoS)**: This will help services obtain an appropriate share of a network’s bandwidth.

An IPv6 address is shown as **8 groups of four hexadecimal digits** and are separated by colons (`:`). An example IPv6 address is `2001:0db8:0000:0000:0000:ffff:0000:0001`. It can be shortened by removing leading zeros and substituting two colons (`::`) for the longest consecutive zero fields. The shortened example is `2001:db8::ffff:0:1`.

Special IPv6 addresses:
* `::1` is the local loopback address.
* The range `2001:db8::` to `2001:db8:ffff:ffff:ffff:ffff:ffff:ffff` is reserved for documentation.
* `fc00::` to `fdff:ffff:ffff:ffff:ffff:ffff:ffff:ffff` are addresses reserved for internal network use (Unique Local Addresses).

### What is WiFi?

Wireless networking is a popular method of connecting corporate and home systems because of the ease of deployment and relatively low cost. It has made networking more versatile than ever before. However, with this freedom comes additional vulnerabilities.

In a LAN, threat actors need to enter the physical space or immediate vicinity of the physical media itself. By contrast, wireless media intrusions can happen at a distance.

### Security of the Network

TCP/IP’s vulnerabilities are numerous. Improperly implemented TCP/IP stacks are vulnerable to various **DoS/DDoS attacks**, **fragment attacks**, **oversized packet attacks**, **spoofing attacks**, and **man-in-the-middle attacks**. TCP/IP is also subject to passive attacks via monitoring or sniffing.

### Ports and Protocols (Applications/Services)

* **Physical Ports**: The ports on routers, switches, servers, etc., that you connect physical cables to.
* **Logical Ports**: An address number that both ends of a communication link agree to use when transferring data. Ports allow a single IP address to support multiple simultaneous communications.
    * **Well-known ports (0–1023)**: Related to common protocols (`DNS`, `SMTP`, etc.).
    * **Registered ports (1024–49151)**: Often associated with proprietary applications (`RADIUS` on 1812, `Microsoft SQL Server` on 1433/1434).
    * **Dynamic or private ports (49152–65535)**: Used for temporary sessions.

### Secure Ports

Some network protocols transmit information in clear text and should not be used. The table below shows some insecure protocols along with recommended secure alternatives.

| Insecure Port | Description | Protocol | Secure Alternative Port | Protocol |
| :-----------: | :---------- | :------- | :---------------------: | :------- |
| 21 | FTP sends credentials in **plaintext**. | File Transfer Protocol | 22* - SFTP | Secure File Transfer Protocol |
| 23 | Telnet sends all data in **plaintext**. | Telnet | 22* - SSH | Secure Shell |
| 25 | Default unencrypted port for sending email. | Simple Mail Transfer Protocol | 587 - SMTP | SMTP with TLS |
| 37 | Legacy protocol, replaced by NTP. | Time Protocol | 123 - NTP | Network Time Protocol |
| 53 | DNS can be modified in transit. | Domain Name Service | 853 - DoT | DNS over TLS (DoT) |
| 80 | HTTP is not encrypted. | HyperText Transfer Protocol | 443 - HTTPS | HyperText Transfer Protocol (SSL/TLS) |
| 143 | IMAP traffic is not encrypted. | Internet Message Access Protocol | 993 - IMAP | IMAP for SSL/TLS |
| 161/162 | Used for managing infrastructure devices. | Simple Network Management Protocol | 161/162 - SNMP | SNMPv3 (adds encryption) |
| 445 | SMB is used for file access and is vulnerable. | Server Message Block | 2049 - NFS | Network File System |
| 389 | LDAP is not encrypted and can be manipulated. | Lightweight Directory Access Protocol | 636 - LDAPS | Lightweight Directory Access Protocol Secure |

\* *Port 22 is used for both SFTP and SSH.*

### SYN, SYN-ACK, ACK

---

## Module 2 Understand Network (Cyber) Threats and Attacks

*Domain D4.1.2, D4.2.2, D4.2.3*

### Types of Threats

* **Spoofing**: An attack to **gain access to a target system through the use of a falsified identity**.
* **Phishing**: An attack that **attempts to misdirect legitimate users to malicious websites**.
* **DoS/DDoS**: A denial-of-service attack with the **primary goal of preventing legitimate activity on a victimized system**.
* **Virus**: A **self-replicating** piece of code that spreads with user assistance (e.g., clicking a link). Its main functions are **propagation and destruction**.
* **Worm**: Propagates itself **without requiring any human intervention**.
* **Trojan**: A program that **appears benevolent but carries a malicious payload**.
* **On-path attack**: Attackers place themselves between two devices to intercept or modify information. Also known as **man-in-the-middle (MITM) attacks**.
* **Side-channel**: A **passive, noninvasive attack** to observe the operation of a device (e.g., power monitoring).
* **Advanced Persistent Threat (APT)**: Threats with an **unusually high level of technical and operational sophistication spanning months or years**.
* **Insider Threat**: Threats that **arise from individuals who are trusted by the organization**.
* **Malware**: A program inserted into a system to **compromise confidentiality, integrity, or availability**.
* **Ransomware**: Malware used to facilitate a ransom attack, often by encrypting files.

### Identify Threats and Tools Used to Prevent Them

* **Intrusion Detection System (IDS)**: Monitors to detect abnormal activity. **Identifies threats, but does not prevent them**.
* **Host-based IDS (HIDS)**: Monitors activity on a single computer.
* **Network-based IDS (NIDS)**: Monitors and evaluates network activity.
* **SIEM**: Gathers log data from various sources to understand security concerns.
* **Anti-malware/Antivirus**: Seeks to identify and block malicious software. **Identifies and prevents threats**.
* **Scans**: Evaluates the effectiveness of security controls. **Identifies threats, but does not prevent them**.
* **Firewall**: Filters network traffic based on rules. **Identifies and prevents threats**.
* **Intrusion Prevention System (IPS-NIPS/HIPS)**: Actively attempts to detect and block attacks. **Identifies and prevents threats**.

### Preventing Threats

* **Keep systems and applications up to date** with patch management.
* **Remove or disable unneeded services and protocols**.
* **Use intrusion detection and prevention systems**.
* **Use up-to-date anti-malware software**.
* **Use firewalls** (both network-based and host-based).

---

## Module 3 Understand Network Security Infrastructure

*Domain D4.3.1, D4.3.2*

### On-Premises Data Centers

Organizations can outsource or own their data center. An on-premises data center requires a building, **power, HVAC, fire suppression, and redundancy**.

* **Data Center/Closets**: Protecting access to the physical layer (wiring, servers, switches) is critical for security.
* **Heating, Ventilation and Air Conditioning (HVAC) / Environmental**: Equipment requires adequate cooling and airflow (recommended range: **18°C to 27°C**). Environmental monitoring for contaminants, water, or gas leaks is essential.
* **Power**: Data centers require constant and consistent electrical power, including backup generators and battery backups (`UPS`).
* **Fire Suppression**: Server rooms require appropriate fire suppression. Gas-based systems are often used to avoid water damage to electronics.

### Redundancy

Redundancy is designing systems with **duplicate components** so that if a failure occurs, there is a backup. This applies to power supplies, generators, communication channels, and other critical infrastructure.

### Memorandum of Understanding (MOU)/Memorandum of Agreement (MOA)

These are agreements, often called **joint operating agreements (JOA)**, where organizations agree to share resources during an emergency to maintain business continuity (`BC`) and disaster recovery (`DR`) capabilities. An `MOU`/`MOA` is less granular than a Service Level Agreement (`SLA`), focusing more on what can be done with a system or information.

### Cloud

Cloud computing is a model for enabling convenient, on-demand network access to a shared pool of configurable computing resources (`networks`, `servers`, `storage`, `applications`, `services`) that can be rapidly provisioned. (NIST SP 800-145)

#### Cloud Characteristics

* **Resource Pooling**
* **Broad Network Access**
* **Rapid Elasticity**
* **Measured Service**
* **On-Demand Self-Service**
* **Reduced cost of ownership**

### Service Models

* **Software as a Service (SaaS)**: Provides access to **software applications** (e.g., email). The provider manages everything; the user just uses the software.
* **Platform as a Service (PaaS)**: Provides a **platform for customers to build and run their own software**. The customer manages their applications, while the provider manages the underlying infrastructure.
* **Infrastructure as a Service (IaaS)**: Provides access to **traditional computing resources** (e.g., servers, storage). The customer manages the operating system, applications, and all maintenance on them.

### Deployment Models

* **Public Cloud**: Resources are available for any consumer to rent and are hosted by an external Cloud Service Provider (`CSP`).
* **Private Cloud**: Cloud infrastructure is operated solely for a single organization. It can be managed internally or by a third party.
* **Hybrid Cloud**: A combination of two or more cloud deployment models (typically public and private).
* **Community Cloud**: Shared by several organizations and supports a specific community that has shared concerns.

### Managed Service Provider (MSP)

An **MSP** is a company that remotely manages a customer's IT infrastructure and/or end-user systems, typically on a proactive basis and under a subscription model.

### Service-Level Agreement (SLA)

An **SLA** is a contract between a service provider and a customer that documents specific parameters, minimum service levels, and remedies for any failure to meet the specified requirements. It covers aspects like service availability, performance, data security, disaster recovery, and data ownership.

### Network Design

* **Network segmentation**: Controlling traffic among networked devices.
* **DMZ (Demilitarized Zone)**: A network area accessible by outside visitors but isolated from the private network.
* **VLANs (Virtual LANs)**: Created by switches to logically segment a network.
* **VPN (Virtual Private Network)**: A communication tunnel that provides point-to-point transmission over an untrusted network.
* **Defense in depth**: Using multiple layers of security controls.
* **Network Access Control (NAC)**: Controlling access to an environment through strict adherence to security policy.

### Defense in Depth

This is a layered security approach. The layers include:
1.  **Data**: Encryption, DLP, IAM.
2.  **Application**: WAFs, database monitors.
3.  **Host**: Antivirus, endpoint firewalls, patch management.
4.  **Internal network**: IDS/IPS, internal firewalls, NAC.
5.  **Perimeter**: Gateway firewalls, honeypots.
6.  **Physical**: Locks, walls, access control.
7.  **Policies, procedures, and awareness**: Administrative controls.

### Zero Trust

Zero Trust is a security model that insists that **every process or action a user attempts to take must be authenticated and authorized**. It moves defenses from static, network-based perimeters to focus on users, assets, and data. It assumes no implicit trust, even for users inside the network perimeter.

### Network Access Control (NAC)

`NAC` solutions provide network visibility and enforce security policies to control access. A `NAC` device can identify who and what is on a network, isolate noncompliant devices into a quarantined area, and help remediate them before granting access. It is crucial for managing `BYOD` and `IoT` devices.

### Network Segmentation (and DMZ)

**Network segmentation** is an effective way to achieve defense in depth. A **DMZ** is a classic example, where public-facing servers are physically or logically separated from the internal network to limit the scope of a breach.

### Segmentation for Embedded Systems and IoT

IoT and embedded systems need special attention. Network segmentation can be used to isolate these devices from the main corporate network to limit potential harm from a compromised device. This can be done with `VLANs` or by filtering traffic based on `MAC addresses`, `IP addresses`, or ports.

### Microsegmentation

**Microsegmentation** is a security technique that involves dividing a data center or cloud deployment into distinct security segments down to the individual workload level, and then defining security controls for each segment. This helps prevent lateral movement by an attacker within the data center.

### Virtual Local Area Network (VLAN)

`VLANs` allow network administrators to use switches to create software-based LAN segments. Devices on the same `VLAN` can communicate as if they were on the same physical segment, but traffic between different `VLANs` must be routed. This reduces broadcast traffic and can help contain attacks.

### Virtual Private Network (VPN)

A `VPN` is a point-to-point connection between two hosts over an untrusted network like the internet. It is not inherently encrypted, but secure protocols (`IPsec`, `TLS`) are used to create a trusted, encrypted tunnel for authentication and data traffic.
