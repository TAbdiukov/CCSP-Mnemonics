# CCSP-Mnemonics
Short list of CCSP mnemonics for those who did CISSP

## Useful resources

* **[CCSP by Alukos](https://ccsp.alukos.com/)**
* **[FREE ISC2 CCSP Quiz/Test](https://cloud.connect.isc2.org/ccsp-quiz)**
* [FREE ISC2 CCSP Flashcards](https://cloud.connect.isc2.org/ccsp-flashcards) [These may or may not be useful]
* [CSA Security Guidance](https://downloads.cloudsecurityalliance.org/assets/research/security-guidance/security-guidance-v4-FINAL.pdf) *(recommended by Reddit)*

### Other

* [Surprisingly on-topic vieo by Jeremy's IT Lab](https://www.youtube.com/watch?v=_S3greGajJA)

[Good productive vibes](https://www.youtube.com/watch?v=zR9F8QIuUGc)

## Domain 1

### NIST 800-145 Essential characteristics of cloud

1. On-demand **self-service** - **service self**
2. **Broad** network **access** - **broad access** over internet or WAN
3. **Resource pooling** - **Resources** are *somewhere* in that cloud **pool** (within chosen geographic location)

![pool](https://png.pngtree.com/thumb_back/fw800/background/20190612/pngtree-watermark-background-of-blue-swimming-pool-image_117749.jpg)
---- |
Swimming **pool** with **resources**

4. Rapid **elastic**ity - (Repeat) (cloud) solution is like an **elastic band** - can scale up and scale down as needed. **Elasticity implies scalability**
5. **Measured** service - pay **exactly the measured amount**

### Other characteristics of cloud

* **Scal**ability - app/solution can "**scale** up" well for thousands of inputs or clients
* **Elastic**ity - (cloud) solution is like an **elastic band** - can scale up and scale down as needed. **Elasticity implies scalability**
* Cloud **bursting** - Hybrid cloud elasticity (**bursting**)
* Multi**tenancy** - Sharing resources with everyone, including crooks

![Cuba](https://www.usatoday.com/gcdn/presto/2018/11/16/USAT/546544cc-7dbe-41b3-8945-d0242b906bfd-HAVANA_building_photo_1.jpg?width=660&height=372&fit=crop&format=pjpg&auto=webp) |
---- |
**Multitenancy**


### Cloud types

* On-prem - Your datacenter
* Private - CSP only services you (CSP is your Sugar Baby) - Expensive. 
	* **Community** - (U.S. Intelligence) **Community** Cloud - cloud for those who share a mission!
* Hybrid - Your infrastructure 🖤 CSP's cloud. This is hard to configure well.
* Public - CSP's cloud for everyone, including crooks. Multitenancy.

### Trusted Computing

* TEE - Trusted Execution Environment ([≈ TCB](https://stackoverflow.com/q/63335341/12258312))
* TPM/vTPM - Internal hardware for TEE/TCB (+ Secure Boot)
* HSM - External dongle/card for TEE/TCB (+ Secrets Management)

### Computing types

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

* 1-3: Something you know, something you have, something you are, 
* 4-5: Somewhere you are, something you do

### Who does what

ISO 17789

### 5 Facets of Cloud/IOT interoperability - ISO/IEC 21823

1. (Comply with) Policy
2. (Expected) behavior
3. (Standard and secure) Transport
4. (Exchange is) Syncratic
5. (Data meaning is) Symantic


### Cloud Leadership

* Governance - Policy & Central control
* Orchestration - manage workloads
	* Scheduling - Orchestrate on automatic schedule
		* Distributed Resource Scheduling - VMWare-proprietary schedule optimization
* Migration - from on-prem to cloud

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

#### Mnemonic 1

```
TIERS1234
123456789
-----6789
```

#### Mnemonic 2:

```
TIER
1234
9876
```



### (Compass)-bound communication 
#### Occurs in SDNs

![Cisco](https://learningnetwork.cisco.com/sfc/servlet.shepherd/version/renditionDownload?rendition=THUMB720BY480&versionId=0683i000001rnMl&operationContext=CHATTER&contentId=05T3i00000ACKHA&page=0)

### CSA CIR

Cloud IR framework by CSA. Based on NIST 800-61

#### NIST 800-61

4 stages of Incident Response,

1. Preparation
2. Detection & Analysis
3. Containment, Eradication and Recovery
4. Post-mortem

(Reminiscent of CISSP's DRMRRRL)

### Ping, power, pipe
*For designing a datacenter*

1) **Ping** = **Ping** to remote access (RDP/SSH)
2) **Power** = Electric **Power**
3) **Pipe** = ISP/internet/You**Tube**

### How to design a datacenter

Step 1: Pick a legal heaven location with access to water.
Step 2: Redundancy is key
Step 3: Add LOTS of cables everywhere
Step 4: ????????
Step 5: PROFIT!

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

#### SDLC and Security

1) Security starts as early as **Define** stage.
2) Security inserts controls at **Design** stage.

### SOAP vs REST

* **SOAP** - (Endless) **SOAP** opera of using Microsoft's XML - just like Microsoft's Internet Explorer.
* **REST** - **REST**ructured (modern) API using URIs



### FAM, DAM
*Neither is an IDS/IPS*

* File Activity Monitoring (FAM) - **Audit** user activities intelligently (on) **Files** 
* Database Acivity Monitoring (DAM) - **Audit** user activities intelligently (on) **Databases**

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

### Secure coding guidelines

(taken directly from Alukos + my notes)
* **OWASP** Application Security - guidelines
* OWASP's **ASVS** - AppSec metric Standard for: SAST, DAST, IAST. ASVS has 3 levels
* Software Assurance Forum for Excellence in Code (SAFECode)

### Other

* Abuse Case Testing - (Intentional) misuse case testing. [more info](https://sqa.stackexchange.com/a/1806/43034)
	* (Abuse Case Testing ≈ Misuse Case Testing)


## Domain 5

### Cloud security standards

* ISO/IEC 20000-1 - IT Service Management (Directly to Domain 5, like ITILv4)

* Mnemonic 1: **SLA downtime should all be 0s**
* Mnemonic 2: At **0** years you work in **IT** Support, at 7 years you work in Security Management
* Mnemonic 3: 0s are for IT staff, 7s (as in Boeing 777) are for Security

------------------------

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

-------------------
#### ISO RMF

* ISO 31000 - Overall/general RMF
	* ISO 27000-5 - InfoSec RMF

### CRS

* OWASP CRS - Managed best firewall practices

### Configuration Management

* CI - Configuration Item - configuration for one app
* CMDB - Collection of CIs (Configuration Items) - configuration for many apps.

* CMB - Configuration Management **Board** (not baseline)

### Guessed Configuration Management (CM) Steps

1. Asset inventory
2. Create baseline
3. Establish a CMB board (like CAB)
4. Deploy baselined assets
5. Dicument approved deviations (if needed)

### Terms

* VPC - Virtual Private Cloud - cloud 'VLAN/intranet' area
* RDM - Release & Deployment Management (plan/policy)
* Virtual Client ≈ VDI

### Cloud forensic eDiscovery standards

* CSA Domain 3 - Legal concerns: security, privacy, SLAs.
* NIST IR 8006 - Guidance on DFIR in the cloud

#### ISO

* ISO/IEC 27037 - Initial: Identify, Collect, Preserve e-evidence (Digital Forensics)
* ISO/IEC 27050 - eDiscovery

### IAPP

* ISO/IEC 27041 - Investigate
* ISO/IEC 27042 - Analyse (evidence)
* ISO/IEC 27043 - Principles & Processes

IAPP - Investigate, Analyze, Principles&Processes

```
DF-IAPP
37-1233
```


#### Another meaning of IAPP.

Also IAPP - International Association of Privacy Professionals. Another acronym found in CCSP, about similar topics.
So privacy=IAPP. eDiscovery=IAPP.

### Legal

* CLOUD Act 2018 - FBI can access CLOUD even outside the U.S. (in violation of GDPR)

### SOC

* **Sentiment Analysis** - AI + ML to gain people's **Sentiment** on social media (like Cambridge Analytica to target  **Sentiment** to Donald Trump)

### Problem vs Incident

**Trick**: Replace "Problem" with "Bad Driver"

Bad Drivers are a **Problem** - car crashes as a result of their driving are **Incidents**

All ~~problems~~ bad drivers potentially cause incidents, but not all bad drivers result in incidents.

**Trick 2**: My boyfriend is a **walking problem**! He'll eventually beat me down.

### ITILv4

(This is optional knowledge, but commonly referenced)

#### Availability Management

1) **Designing** services for Availability
2) Availability **Testing**
3) Availability **Monitoring** and Reporting

#### IR 

Is to Recover

#### Capacity and Performance Management

![Highway](https://www.vinci-concessions.com/uploads/2019/06/cofiroute-usa-1920x1106.jpg)

Manage highways & their components

#### Continual Service Improvement (CSI)

* Process **Owner** ≈ Data Owner
* Process Architect ≈ Data Custodian
* CSI **Manager** - **Mid-level managers** who just ensure ITSM (clue: mid-level managers are suckers for fancy job titles)

#### Service-level Management (SLM)

1) **Identification** service requirements
2) Agreement sign-off and service **activation**
3) Service-level **monitoring** and reporting
4) **Maintenance** of SLM framework

#### Disaster Recovery Management

* ITIL "recovery plan" - Detailed master plan for BCP/DRP, can also include data restoration to RPO.
* BCP Strategy - Strategy for business (functions)
* IT Service Continuity - Specific cases continuity plan (i.e. if a specific host failed)
* BCP **Invocation** Guidelines - **Invocation**

### Vulnerability Scanning Requirements from CSP

1) Only scan your internal systems
2) Don't impact other customers
3) Date and time - for detailed scanning

### ISO 20000-1 → Capacity Management

Capacity management of YOUR:
* Business
* Service
* Component

## Domain 6

### Laws

* **Stored Communications** Act (SCA) 1986 - **Stored Communications** (Discord, email) are **private communications**. Dated, but in force.
* **GAPP** - U.S. Optional (**gapp**ed) GDPR
* Privacy Shield - DEAD privacy partnership between the US and EU (For CCSP OPT - it is still alive)

### 3rd party organizations and standards

* **BICSI** - like **SCSI** - cables organization
* N**E**RC/CIP - Electro NERD

![NERC CIP](https://i.ytimg.com/vi/dCIGUU01Leo/hqdefault.jpg) 

### Compliance

* SAS 70 - **outdated like the 70s** SOC 1
* SSAE 16 - outdated SSAE 18
* AICPA (USA) → SSAE → SOC (1/2/3)
* IAAS (EU) → ISAE → ISAE 3402
* ISAE ≈ SSAE
* ISAE 3402 ≈ SSAE SOC 2
* FedRAMP - **Fed**erally screened CSPs for being **RAMP**s

#### CSA

CSA → STAR

CSA STAR - for CSPs. Lightweight assurance method used by CSP, customer, auditor, consultant. 

##### CSA STAR Levels,

1) Self-assessment (internal audit, low assurance)
2) Third-party audit (external audit, high assurance)
3) Continuous auditing

CSA STAR - SEC (Self, External, Continuous)

### ISMS vs IISCS

* ISMS - Identify and monitor risk
* IISCS - Mitigate risk

**Trick**: I**SMS** is a radar that sends **SMS**, **IIS**C**S** is a fighter jet with **2 I**-shaped harpoon rockets and **2 S**-shaped hooks.

![ISMS](https://live.staticflickr.com/3238/2388570728_68522c2e34_c.jpg) | ![IISCS](https://www.thedrive.com/content/2020/04/234fgggs.jpg)
---- | ----
**ISMS** | **IISCS**

### Risk

* Profile - **Risks** (profiles) that stand up to the organization
* Posture - How well organization holds (poses) against risks.
* Appetite = Tolerance - How hungry is the organization to take more risk.
* Treatment = Management

### GDPR Roles

* Data Protection **Officer** (DPO) - Mandatory **compliance officer**
* Data Controller = Data Owner (controls data life)

### MSA, SLA, SOW, MOU, etc

![Big 'MSA' & many sow](https://www.cargill.com/image/1432078231924/hero-can-sow-1280x510.jpg)

* **M**SA - **Master** Services Provided. **Masters of airways**
* **S**OW - **Small (sow)** Jobs Worked-on
* MOU - Completely different beast - Confirms **understanding** of each-other's "moo" talk.
* SLA - Performance Expected
* OLA - Like Windows OLE (internal, under-the-hood) - under-the-hood 'SLA' internal agreement between (C)SP and its brokers.
* NDA - Confidential clauses (SLA is not suitable)
* BPA - **BiPlane** Joint-Venture agreement

### Vendor - sticky situations

* **Via**bility - Vendor may die like [**Via**com](https://en.wikipedia.org/wiki/Viacom_(2005%E2%80%932019))
* Lock-in - Proprietary infrastructure forces you to stay with vendor
* Lock-out - cannot access living vendor. Can also sometimes mean "Viability".

### Other

* **P**IA - like BIA - **Privacy** impact analysis.
* Doctrine of **Proper** Law - **properly** defines jurisdiction of law applied in a case 

## Domain 7 (meta-domain)

![World 9-1](https://mario.wiki.gallery/images/7/7d/SMB_NES_World_9-1_Title_Card.png)

### CSA

![CSA](https://damassets.autodesk.net/content/dam/autodesk/images/trust/csa-logo-thumb-384x288.png)

* CSA Cloud Controls Matrix (CCMv4) - Cloud Risk Management framework by CSA, mapped to trusted organizations&frameworks like ISO, ISACA, PCI. **CSA's best product! Simplify regulatory compliance!**
	* Trick: ISACA has CISM, CSA has ISACA in CCM
* CSA "Egregious 11" - Top cloud threats
* CSA Checklists - VERY SAFE baseline guides
* CSA CIR - Cloud IR framework by CSA. Based on NIST 800-61.
* CSA Domain 3: Legal Issues - Security guidance of legal issues
* CSA STAR - Lightweight complince standard. Level 1 - Internal audit. Level 2 - External audit.
* CSA CAIQ - Consensus Assessment Initiative Questionnaire - optional IQ questions to access CSP Security

### Comparisons

* anti-DDoS: CDN > CSP's anti-DDoS capabilities
* API anti-DDoS: API Gateway > IPS [API Gateway can help understand DDoS traffic]
* anti-DDoS: Authentication > Scale
* AuthN of (cloud) hosts: Host digital certificates
* SSO - One org (+IDaaS); Federation - 2+ orgs.

### IaaS, PaaS, SaaS

![IPS](https://assets1.cbsnewsstatic.com/hub/i/2010/06/07/74ecadc6-a642-11e2-a3f0-029118418759/phprF09uBsteve-jobs-wwdc-81.jpg)

* IaaS - Many hosts Infrastructure. Best if your app really requires complex infrastructure (such as 5 databases, 10 firewalls etc).
* PaaS - One host. Best if: your app can run on 1 host, and you are concerned about: liability, security, time and money wasted configuring code and infrastructure. PaaS is much more liability-optimal than IaaS. PaaS is the easiest to administer. **PaaS** your **code** - so IaC is PaaS.
* SaaS - Service. Service is the most affordable, and has least liability to the customer and the cheapest, but it takes time to configure code to work with SaaS and cloud.

Finally

* FaaS - serverless (fatherless) IaC, cheaper and simplier than PaaS.

### Other

* Tampering - always of data, but not of systems
