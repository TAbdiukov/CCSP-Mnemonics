# CCSP-Mnemonics
Short list of CCSP mnemonics for those who did CISSP

## Useful resources

* **[CCSP by Alukos](https://ccsp.alukos.com/)**
* **[FREE ISC2 CCSP Quiz/Test](https://cloud.connect.isc2.org/ccsp-quiz)**
* [FREE ISC2 CCSP Flashcards](https://cloud.connect.isc2.org/ccsp-flashcards) [These may or may not be useful]

[Good productive vibes](https://www.youtube.com/watch?v=zR9F8QIuUGc)

## Domain 1

### Characteristics of cloud

* Scalability - app/solution can "scale up" well for 1000s of inputs or clients
* Elasticity - (cloud) solution is like an **elastic band** - can scale up and scale down as needed. **Elasticity implies scalability**
* Cloud **bursting** - Hybrid cloud elasticity (**bursting**)

* Multi**tenancy** - Sharing resources with everyone, including crooks

![Cuba](https://www.usatoday.com/gcdn/presto/2018/11/16/USAT/546544cc-7dbe-41b3-8945-d0242b906bfd-HAVANA_building_photo_1.jpg?width=660&height=372&fit=crop&format=pjpg&auto=webp) |
---- |
**Multitenancy**

### Cloud types

* On-prem - Your datacentre
* Private - CSP only services you (CSP is your Sugar Baby) - Expensive. 
* Hybrid - Your infrastructure 🖤 CSP's cloud. This is hard to configure well.
* Public - CSP's cloud for everyone, including crooks. Multitenancy.

* **Community** - (U.S. Intelligence) **Community** Cloud - cloud for those who share a mission!

### Trusted Computing

* TEE - Trusted Execution Environment ([≈ TCB](https://stackoverflow.com/q/63335341/12258312))
* TPM - Internal hardware for TEE/TCB
* HSM - External dongle/card for TEE/TCB

* Confidential Computing - protect data in use
* Quantum computing - protect cryptographic keys with the observer's principle

### Cloud account types

* Service - service-app only (not user)
* Shared - shared by team


### FIPS 140-2: Security Levels

1. Lowest
2. **TPM, HSM** [Cryptographic modules]
3. (TPM, HSM) + **Tamper-proof**
4. (TPM, HSM) + (Tamper-proof) + **Self-destruct on attack**

#### Mnemonics

1) **Lowest**

2) For **cryptographic** modules that protect sensitive information

3) For **physical** contractors to prevent physical tampering

4) tamper-proof control where the data on the device is **automatically erased** if it detects a physical attack

Mnemonic: **Low** adoption of **crypto** in the **physical** world due to **auto-erase**

Mnemonic 2: **Low** amount of **crypto** will cause **physical** ASIC to **self-destruct** 

### Hypervisors

* Type 1 - Bare metal (hardware)
* Type 2 - Software

Mnemonic: Hardware first, then software

### Extra auth types

* Something you know, something you have, something you are, 

* Somewhere you are, something you do

### Who does what

ISO 17789

### 5 Facets of Cloud/IOT interoperability - ISO/IEC 21823

1. (Comply with) Policy
2. (Expected) behavior
3. (Standard and secure) Transport
4. (Exchange is) Syncratic
5. (Data meaning is) Symantic


## Domain 2

### Cloud DLM - Data Lifecycle Management

The cloud data lifecycle consists of :

1) Create
2) Store
3) Use
4) Share
5) Archive
6) Destroy

* Letters: CS US AD
* Mnemonic: CompSci (of) US (created) ActiveDirectory
* Mnemonic 2: Cloud SUS ActiveDirectory

### Storage types

#### By access chain

* RAW - Direct hands-on low-level access some drive (including access to S.M.A.R.T. and drive firmware!). Access directly: `You → Drive`. Direct access means "Direct responsibility" for data remanence caused and found.
* Volume-storage - High-level, abstractioned, indirect, access to a (likely virtual) drive in a cluster: `You → Cluster of drives → (Subcluster of drives? It's a cloud architecture after all) →  Drive`
	* File-storage - Store files in an abstract vacuum - like in Cisco devices.
	* Block-storage - Store blocks of data like on hard drives - you can orchestrate filesystems, NTFS Master File Tables, folders, files, file attributes etc.

#### By longevity

* Ephemeral - RAM, RAMDisk (ephemeral volume), SWAP/Pagefile, temporarily LiveCD (whether RAM or HDD) destroyed after a session.
* Long-Term - HDD RAID or **LT**O tapes for use after session (for example, for work on next day and backup)
	* Archival - (likely a subset of long-term storage) - good for archiving, but very slow data retrieval (hours/days).

### Data types

* Structured - SQL Database
* Semi-structured - CSV, JSON, XML.
* Unstructured - Files and everything else

### Data Dispersion

is a KISS term: "Store data in many places"

A bit like RAID, can be used to achieve diametrically opposed goals:
* Availability (by orchestrating multiple compies of data)
* ~~[Two-person control]~~ multi-person control (by splitting data into many pieces - thus potentially jeopardizing availability), and

### DLP deployment

(Rough unofficial order)

1) First, eDiscover your data

2) Prioritize and categorize: thus label the data

3) Then tag the data
For CCSP : Tags for DLP; Labels for classification
(Tags explain the data, labels show sensitivity)

4) After the data is tagged, set up DLP policies

5) Deploy DLP

6) Let DLP train on data (you can help, but for CCSP: DLP will work fine on its own)

### Data DEclassification

* Anonymization - Remove sensitive data and make the subject **anonymous** (like a hacker group). Can be required by GDPR.
* Masking - Permanently mask and damage data, suboptions:
	* Randomize - meaningful parts of data replaced with meaningless random data
	* Hash - John Smith" becomes "0xDEA4B884"
	* Shuffle - Everyone's data is shuffled, rendering data dirty and meaningless
	* Mask - Card number `**** **** **** 9608` expiry `09/25` cvv `***`
	* Delete - Delete
* Tokenization - split sensitive and non-sensitive tables, use meaningless **tokens** to uniquely identify subjects where needed.

### Other 

* IRM System = eDRM System - like Adobe Digital Editions.

## Domain 3

### Recovery sites

(same as CISSP, plus):

Cloud site - much more cost-effective than hot site, however, takes longer to reallocate to. Is a viable replacement to Hot and Warm sites.

### Uptime Institute: Availability tiers

1) 99.**6**71%
2) 99.**7**41%
3) 99.9**8**2%
4) 99.**99**5%

**Mnemonic:** 

```
TIERS1234
123456789
-----6789
```

### (Compass)-bound communication 
#### Occurs in SDNs

![Cisco](https://learningnetwork.cisco.com/sfc/servlet.shepherd/version/renditionDownload?rendition=THUMB720BY480&versionId=0683i000001rnMl&operationContext=CHATTER&contentId=05T3i00000ACKHA&page=0)

### Ping, power, pipe
*For designing a datacenter*

1) **Ping** = **Ping** to remote access (RDP/SSH)
2) **Power** = Electric **Power**
3) **Pipe** = ISP/internet/You**Tube**

### How to develop a datacenter

Step 1: Redundancy is key
Step 2: ????????
Step 3: PROFIT!

## Domain 4

### Threat Modeling Approaches

* **D**rea**D** - **D**amages (by attacker) - developed by Microsoft - replaced with STRIDE. **DREAD** is forced away by **STRIDE**
* STRIDE - Main one by Microsoft 
* PASTA - for code. PASTA (spaghetti) code.
* ATASM - Like Serial ATA (SATA) is serial - ATASM is Serial. ATASM is also a metamodel. **ATASM - ATA Serial Metamodel**.
	* **A**rchitecture (Analysis)
	* **T**hreats (existing: actors, goals)
	* **A**ttack **S**urface (existing)
	* **M**itigations (existing)

(Architecture Threats - Attack Surface - Mitigations)

### Terms

* CSA - Cloud Security Alliance (organization)
* SBOM - List software's **BOM**bay-made libraries
	* SCA - Actions upon SBOM 
* SCM - Software Configuration Management (software in secure configuration - protect against **scummy** configurations like `allowlist *.*`)
* Dynamic Secrets - JIT secrets.
* KMS - Key Management Service = Secrets Server.

### SDLC

1. Planning Analysis (for ongoing project) 
2. Requirements Analysis (to finish project) **[for CCSP: separate phase]**
3. Define (goals with user)
4. Design (map technical parts plane)
5. Develop (implement)
6. Test (verify)
7. Deploy/Release/Maintain

PR DDD TD

### SOAP vs REST

* **SOAP** - (Endless) **SOAP** opera of using Microsoft's XML - just like Microsoft's Internet Explorer.
* **REST** - **REST**ructured (modern) API



### FAM, DAM
*Neither is an IDS/IPS*

* File Activity Monitoring (FAM) - Audit user activities intelligently (on) **Files** 
* Database Acivity Monitoring (DAM) - Audit user activities intelligently (on) **Databases**

### Gateways

* SWG (Secure Web) Gateway/Virtual Security Appliance (VSA) = Virtual Cloud Firewall host. Heavy duty, advanced functionality.
* API Gateway = API WAF/IPS and monitoring
* XML Gateway = XML (SOAP) WAF/IPS and monitoring.


### Encryption

* Cryptoshredding - Secure data deletion with double-encryption. Great for cloud.
* Full Disk Encryption (FDE) - BitLocker/dm-crypt
* **Transparent** Data Encryption (TDE) - JIT encryption/decryption of data, **transparent** to the legacy app (no app changes required)

### Functional vs Non-Functional Testing

* **Functional** - (non-descriminatory) - Does app **Function** as expected
* **Non-Functional** - (descriminatory) - Is the app *beefy, too slow, and has a ugly UI*?

### Testing Target

* Static (**SAST**) - Code
* Dynamic (**DAST**) - Runtime
* **IAST** - **Interactive** AST - Agent on backend to show where the error is,

![IAST](https://www.getastra.com/blog/wp-content/uploads/2017/06/Server-Error-Message.png) | ![IAST](https://i.stack.imgur.com/LOB5R.png)
---- | ----
**IAST** Example | **IAST** Example


### Other

* OWASP ASVS - AppSec Verification: Standard for: SAST, DAST, IAST. ASVS has 3 levels.
* Abuse Case Testing - (Intentional) misuse case testing. [more info](https://sqa.stackexchange.com/a/1806/43034)
	* (Abuse Case Testing ≈ Misuse Case Testing)


## Domain 5

### Cloud security standards

* ISO/IEC 27001 - Base
* ISO/IEC 27002 - Base lite (for gap analysis - fits like LEGO with 27001) 

-------------------------

* ISO/IEC 27001 - Base
* ISO/IEC 270**17** - Base + Cloud
* ISO/IEC 270**18** - Base + Cloud + PII. HIGH level of assurance.

-----------------------

* ISO/IEC 27001 - Base
* ISO/IEC 27**7**01 - Base + Privacy focus

-----------------

* ISO 27036 - Supply Chain Risk Management (SCM/SCRM) for ISO 27001 users.

### CRS

* OWASP CRS - Managed best firewall practices

### Terms

* VPC - Virtual Private Cloud - cloud 'VLAN/intranet' area

### Cloud forensic eDiscovery standards

* CSA Domain 3 - Legal concerns: security, privacy, SLAs.

* NIST IR 8006 - Guidance on DFIR in the cloud

* ISO/IEC 27050 - 4 parts framework for: Forensics, eDiscovery, Evidence management

* ISO/IEC 27037 - Identify, collect, preserve

### IAPP


* ISO/IEC 27041 - Investigate
* ISO/IEC 27042 - Analyse (evidence)
* ISO/IEC 27043 - Principles & Processes

IAPP - Investigate, Analyze, Principles&Processes

#### Another meaning of IAPP.

Also IAPP - International Association of Privacy Professionals. Another acronym found in CCSP, about similar topics.
So privacy=IAPP. eDiscovery=IAPP.


### Legal

* CLOUD Act 2018 - FBI can access CLOUD even outside the U.S. (in violation of GDPR)

### SOC

* **Sentiment Analysis** - AI + ML to gain people's **Sentiment** on social media (like Cambridge Analytica to target  **Sentiment** to Donald Trump)

## Domain 6

### Laws

* **Stored Communications** Act (SCA) 1986 - **Stored Communications** (Discord, email) are **private communications**. Dated, but in force.
* **GAPP** - U.S. Optional (**gapp**ed) GDPR

### Compliance

* AICPA → SSAE → SOC (1/2/3)
* IAAS → ISAE → ISAE 3402
* ISAE ≈ SSAE
* ISAE 3402 ≈ SSAE SOC 2

#### CSA

CSA → STAR

CSA STAR - for CSPs. Lightweight assurance method used by CSP, customer, auditor, consultant. 

##### CSA Levels,

1) Self-assessment (internal audit, low assurance)
2) Third-party audit (external audit, high assurance)
3) Continuous auditing

### CSA Cloud Controls matrix (CSA CCMv4)

TODO

### ISMS vs IISCS

* ISMS - Identify and monitor risk
* IISCS - Mitigate risk

### Risk

* Profile - Current risks and corresponding mitigations
* Posture - How well organization holds (poses) against risks.
* Appetite = Tolerance - How hungry is the organization to take more risk.
* Treatment = Management

### GDPR Roles

* Data Protection **Officer** (DPO) - Mandatory **compliance officer**
* Data Controller = Data Owner (controls data life)

### MSA, SLA, SOW

![Big 'MSA' & many sow](https://www.cargill.com/image/1432078231924/hero-can-sow-1280x510.jpg)

* **M**SA - **Master** Services Provided
* **S**OW - **Small (sow)** Jobs Worked-on

* SLA - Performance Expected

## Domain 7 (meta-domain)

![World 9-1](https://mario.wiki.gallery/images/7/7d/SMB_NES_World_9-1_Title_Card.png)

### CSA

![CSA](https://damassets.autodesk.net/content/dam/autodesk/images/trust/csa-logo-thumb-384x288.png)

* CSA "Egregious 11" - Top cloud threats
* CSA Checklists - VERY SAFE baseline guides
* CSA Cloud Controls Matrix (CCMv4) - Cloud Risk Management framework by CSA, mapped to trusted organizations
* CSA Domain 3: Legal Issues - Security guidance of legal issues
* CSA STAR - Lightweight complince standard. Level 1 - Internal audit. Level 2 - External audit.

### Comparisons

* anti-DDoS: CDN > CSP's anti-DDoS capabilities
* anti-DDoS: API Gateway > IPS [API Gateway can help understand DDoS traffic]
* anti-DDoS: Authentication > Scale
* AuthN of (cloud) hosts: Host digital certificates
* SSO - One org; Federation - 2+ orgs.

### IaaS, PaaS, SaaS

![IPS](https://assets1.cbsnewsstatic.com/hub/i/2010/06/07/74ecadc6-a642-11e2-a3f0-029118418759/phprF09uBsteve-jobs-wwdc-81.jpg)

* IaaS - Many hosts Infrastructure. Best if your app really requires complex infrastructure (such as 5 databases, 10 firewalls etc).
* PaaS - One host. Best if: your app can run on 1 host, and you are concerned about: liability, security, time and money wasted configuring code and infrastructure. PaaS is much more liability-optimal than IaaS. **PaaS** your **code** - so IaC is PaaS.
* SaaS - Service. Service is the most affordable, and has least liability to the customer and the cheapest, but it takes time to configure code to work with SaaS and cloud.

Finally

* FaaS - serverless IaC, cheaper and simplier than PaaS.

### Other

* Tampering - always of data, but not of systems
