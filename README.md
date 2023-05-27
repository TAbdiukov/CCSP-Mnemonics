# CCSP-Mnemonics
Short list of CCSP mnemonics for those who did CISSP

[Good productive vibes](https://www.youtube.com/watch?v=zR9F8QIuUGc)

## Domain 2

### Cloud DLM - Data Lifecycle Management

**Note:** This is a CSA model.

The cloud data lifecycle consists of :

1) Create
2) Store
3) Use
4) Share
5) Archive
6) Destroy

* Letters: CS US AD
* Mnemonic: CompSci (of) US (created) ActiveDirectory

## Domain 4

### Threat Modeling Approaches

* STRIDE - Main one by Microsoft
* **D**rea**D** - **D**amages (by attacker)
* PASTA - for code. PASTA (spaghetti) code.
* ATASM - Like Serial ATA (SATA) is serial - ATASM is Serial. ATASM is also a metamodel. **ATASM - ATA Serial Metamodel**.
	* **A**rchitecture (Analysis)
	* **T**hreats (existing: actors, goals)
	* **A**ttack **S**urface (existing)
	* **M**itigations (existing)

### CSA/SCA etc

* CSA - Cloud Security Alliance (organization)
* SCA - Analysis to detect software vulnerabilities 
	* SBOM - Benchmark software against **BOM**bay-made libraries
* SCM - Software Configuration Management (software in secure configuration - protect against **scummy** configurations like `allowlist *.*`)


### Testing Target

* Static (SAST) - Code
* Dynamic (DAST) - Runtime
* IAST - Agent on backend to show where the error is,

![IAST](https://www.getastra.com/blog/wp-content/uploads/2017/06/Server-Error-Message.png)

### SOAP vs REST

* **SOAP** - (Endless) **SOAP** opera of using XML - just like Internet Explorer.
* **REST** - **REST**ructured (modern) API

### FAM, DAM

* File Activity Monitoring (FAM) - Audit user activities intelligently (on) **Files**
* Database Acivity Monitoring (DAM) - Audit user activities intelligently (on) **Databases**

### Gateways

* API Gateway = API WAF/IPS and monitoring
* XML Gateway = XML (SOAP) WAF/IPS and monitoring.


### Other

* Abuse Case Testing - (Intentional) misuse case testing. [more info](https://sqa.stackexchange.com/questions/1804/abuse-cases-and-misuse-cases)
	* (Abuse Case Testing ≈ Misuse Case Testing)
* Virtual Security Appliance (VSA) - Virtual Cloud Firewall host

## Domain 5

### Cloud security standards

* ISO/IEC 27001 - Base
* ISO/IEC 27002 - Base lite (for gap analysis - fits like LEGO with 27001) 

* ISO/IEC 27001 - Base
* ISO/IEC 270**17** - Base + Cloud
* ISO/IEC 270**18** - Base + Cloud + PII. HIGH level of assurance.

* ISO/IEC 27001 - Base
* ISO/IEC 27**7**01 - Base + Privacy focus

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

### CSA Cloud Controls matrix

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

[Big 'MSA' & many sow](https://www.cargill.com/image/1432078231924/hero-can-sow-1280x510.jpg)

* **M**SA - **Master** Services Provided
* **S**OW - **Small (sow)** Jobs Worked-on

* SLA - Performance Expected

