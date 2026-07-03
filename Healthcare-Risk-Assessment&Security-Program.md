# Healthcare Risk Assessment & Security Program (Kinexa)

## **Overview**

A complete GRC (Governance, Risk & Compliance) project for a fictional medium-sized healthcare provider, "Kinexa". This covers organizational profiling, asset inventory, a risk register mapped to ISO 27001 controls, risk treatment strategy, and a 30-60-90 day security build-up plan.

**Category:** GRC / Risk Management  
**Frameworks:** ISO/IEC 27001, ISO 27002 (Annex A controls)  
**Deliverable Type:** Security assessment & program roadmap

# 1. Organization profile

## 1.1. Workforce & Systems

Kinexa is a medium-sized healthcare provider with approximately 250 employees operating across clinical, administrative and executive functions. 

| Category | Details |
| --- | --- |
| Total Employees | 250 ( clinical: 120, administrative: 80, IT: 30, executive 20 ) |
| Endpoints | 280 devices ( workstations, laptops, tablets, mobile devices ) |
| Servers | 12 physical servers ( database, backups, etc. ) |
| Cloud Services | Microsoft 365, Microsoft Azure, secondary cloud backup |
| Medical Devices | 35 connected diagnostic and monitoring devices |
| Network | Corporate LAN, Clinical VLAN, Guest Wi-Fi |

## 1.2. Key Digital Assets

This table represents Kinexa highest-value data and system inventory. Asset critically is assigned based on sensitivity and operational dependency.

| Asset | Location | Criticality |
| --- | --- | --- |
| Patient Health Care Records | Servers | High |
| Clinical & Diagnostic Data | Servers | High |
| HR Records | Servers | High |
| Network Infrastructure | Firewalls, Routers, Switches | High |
| Medical Devices | Connected equipment | High |
| Cloud Services & Backup | Azure, Backup repositories | High |
| Communication Systems | Microsoft 365 | Medium |
| Web Applications | Patient Portal | Low |

# 2. Risk Assessmentw

The following risk assessment identifies the five most significant cyber security threats. Each threat is mapped to affected assets, rated by likelihood and impact and linked to the relevant ISO 27001 Control.

$$
Risk = Likelihood\quad X\quad Impact
$$

| ID | Threat | Affected Assets | Potencial Impact | Likelihood | ISO 27001 Control |
| --- | --- | --- | --- | --- | --- |
| K-1 | Ransomware Attack | File Servers, Backup Systems | Critical - Patient data encrypted, clinical operations interrupted | HIGH | 8.7 Protection against malware, 8.13 Information backup, 8.16 Monitoring activities, 5.30 ICT readiness for business continuity |
| K-2 | Phishing | Staff Email Accounts, HR Systems, Executive Credentials | High - Credential theft, unauthorized connection, unauthorized access to patient records | HIGH | 6.3 Information security awareness, 8.5 Secure authentication, 5.17 Authentication information, 8.16 Monitoring activities  |
| K-3 | Unpatched Systems | Medical devices, Legacy Servers, Legacy desktops | Critical - Attackers could exploit the existent vulnerabilities, data exfiltration. | HIGH | 8.8 Management of technical vulnerabilities, 8.9 Configuration management, 8.19 Installation of software on operational systems |
| K-4 | Insider Threat | Patient records, Network Infrastructure, Medical equipment, etc.  | Critical - the whole infrastructure could be in danger depending on the range of the insider | MEDIUM | 5.15 Access control, 5.18 Access rights, 8.15 Logging, 8.16 Monitoring activities, 6.3 Awareness training |
| K-5 | Third-Party Supply Chain Attack | Vendor Connections, Cloud Services | High - Unauthorized access via trusted vendor channel | MEDIUM | 5.19 Supplier relationships, 5.20 Supplier agreements, 5.21 ICT supply chain security, 5.22 Monitoring supplier services |

## 2.1. Risk Treatment Approach

For each identified threat, Kinexa will adopt the following ISO 27001 controls aligned risk treatment options.

- Mitigate: Implement technical and organizational controls to lower likelihood or impact to an acceptable level.
- Transfer: Buy cyber insurance.
- Accept: Document formally risks in the Risk Register ( list of security risks ).
- Avoid: Stop any high-risk tasks we don’t absolutely need.

## Priority Controls

**Secure Authentication**

Enforce MFA across all systems, eliminate shared credentials in clinical environments.

**Malware Protection**

Deploy enterprise Endpoint Detection and Response (EDR) with behavioral detection; enforce application whitelisting on servers.

**Backup Strategy**

Implement **3-2-1-1-0**: 3 copies, 2 media types, 1 offsite, 1 air-gapped, 0 errors.

**Supplier Relations**

All Protected Health Information access vendors must sign updated **Business Associate Agreement (** BAAs ) and complete annual security assessments.

**Security Awareness**

Mandatory annual training + quarterly phishing simulations for all 250 employees.

**Monitoring**

24/7 Security Information and Event Management (SIEM) with automated alerting on PHI access anomalies and failed logins.

# 3. 30-60-90 Day Cybersecurity Recovery & Build-Up Plan

Four ISO 27001-aligned options applied per threat:

- **Mitigate** — technical/organizational controls to reduce likelihood or impact
- **Transfer** — cyber insurance
- **Accept** — formally document in the Risk Register
- **Avoid** — stop high-risk activities that aren't essential

### Days 1-30 | IMMEDIATE RESPONE

| **Initiative**  | **Actions**  |
| --- | --- |
| **Activate Incident Response**  | Isolate affected systems, preserve forensic evidence and notify. |
| **Asset Inventory** | Catalog all systems, devices, cloud servers, etc. |
| **Vulnerability Scan** | Run authenticated scans (Nessus/OpenVAS) across all network segments. |
| **Access Control Audit** | Disable orphaned accounts, enforce Multi-Factor Authentication (MFA) on all privileged accounts. |
| **Patch Critical CVEs** | Apply all CVSS patches if possible. |
| **Legal & Regulatory Reporting** | Engage healthcare legal counsel |

### Days 31-60 | BUILD & HARDEN SECURITY LAYERS

| **Initiative**  | **Actions** |
| --- | --- |
| **Network Segmentation** | Isolate infected systems on dedicated VLANs implementing zero-trust segmentation for clinical zones. |
| **Security Information and Event Management ( SIEM )** | Deploy Splunk, configure log ingestions. |
| **Email Security Gateway** | Implement Proofpoint |
| **Privileged Access Management** | Deploy Privileged Access Management ( PAM ) solution |
| **Data Loss Prevention (DLP)** | Configure DLP policies to detect and block unauthorized protected information transmission via email or USB. |
| **ISO 27001 Analysis**  | Perform formal assessment against all the controls. |
| Security Policies | Draft core policies: Password Policy, Incident Response, Data Classification |
| Staff Security Awareness - Phase 1 | Mandatory training for all the employees  |
| Third-Party Risk Review | Audit all agreements, inventory vendor access. If necessary terminate unnecessary connections. |

### Days 61-90 | FORMALIZE TEAMS, TEST DEFENSES

| Initiative | Actions |
| --- | --- |
| SOC / Blue Team Establishment | Create or hire teams |
| Red Team / Penetration Test | External penetration test ( network, web app ) . |
| Incident Response Plan | Finalize IRP. |
| Compliance Roadmap | Publish roadmap to ISO 27001 certification. |
| Staff Awareness - Phase 2 | Role-based training. developers, clinical staff, executives. |

## **4. 30-60-90 Day Security Build-Up Plan**

### **Days 1–30 — Immediate Response**

Activate incident response, full asset inventory, authenticated vulnerability
scans (Nessus/OpenVAS), access control audit (disable orphaned accounts, enforce
MFA on privileged accounts), patch critical CVEs, engage legal counsel.

### **Days 31–60 — Build & Harden**

Network segmentation (zero-trust VLANs for clinical zones), deploy SIEM (Splunk),
email security gateway, Privileged Access Management (PAM), Data Loss Prevention
(DLP), formal ISO 27001 gap assessment, draft core security policies, staff
awareness phase 1, third-party risk review.

### **Days 61–90 — Formalize & Test**

Establish SOC/blue team, conduct external penetration test (network + web app),
finalize Incident Response Plan, publish ISO 27001 certification roadmap,
role-based awareness training phase 2.

# 5. Recommended Security Policies

| **Policy Names** | **Scope** |
| --- | --- |
| Information Security | Master policy establishing Information Security Management System (ISMS) scope, objectives, and management commitment. |
| Access Control & Password Policy | MFA, password complexity, role-based access, privileged access management |
| Incident Respond Policy  | Detection, containment, eradication, recovery, learn. |
| Vendor & Third-Party Security Policy  | Vendor risk assessment, access termination procedures |
| Data Backup & Recovery  | Backup frequency, offsite/offline storage, test schedules |