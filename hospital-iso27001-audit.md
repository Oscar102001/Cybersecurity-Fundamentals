# Hospital Cybersecurity Audit Scenario – ISO 27001

## **Scenario Overview**

A hospital has suffered a ransomware attack affecting patient records and 
critical systems. This audit follows the ISO 27001 PDCA framework to identify 
non-conformities, assess risks, and recommend corrective actions.

**Framework**: ISO/IEC 27001  
**Audit Type**: Internal Security Audit  
**Industry**: Healthcare  
**Tools/Standards:** ISO 27001 Annex A, PIPEDA, PDCA Methodology

# Step 1: Identify the Scope of the Audit (PLAN)

### 1. Hospital Departments Included in the Audit

The audit scope should include **all departments that create, process, store, or access sensitive information**, especially those involved in the ransomware incident.

**In scope:**

- **Clinical Departments**
    - Emergency
    - Radiology
    - Surgery
    - Intensive Care Unit (ICU)
- **Health Information Management (HIM)**
    - Electronic Medical Records (EMR) systems
- **Billing & Finance**
    - Patient billing
    - Insurance claims
    - Payment systems
- **IT Department**
    - Network infrastructure
    - Servers
    - Backups
    - Endpoint devices
- **Administration & HR**
    - Employee records
    - Payroll data
- **Third-party services**
    - Cloud EMR providers
    - Medical software vendors
    - Managed IT services
    

---

### 2. Types of Data That Need Protection

According to ISO 27001 and healthcare best practices, the following information assets are critical:

- **Personal Health Information (PHI)**
    - Medical history
    - Diagnoses
    - Lab results
    - Imaging data
- **Personally Identifiable Information (PII)**
    - Names
    - Addresses
    - Phone numbers
    - Government IDs
- **Financial Data**
    - Credit card information
    - Insurance details
    - Billing records
- **Operational Data**
    - Network configurations
    - System logs
    - Backup files
- **Authentication Data**
    - User credentials
    - Access tokens
    - MFA data

These assets must be protected for CIA ( Confidentiality, Integrity, Availability)

---

### 3. Regulatory and Legal Requirements

The audit must consider **applicable laws and regulations**, which ISO 27001 requires to be identified and documented.

**PIPEDA (Canada)**

- Personal information protection
- **Local healthcare regulations**
- **ISO/IEC 27001 & ISO/IEC 27002**
    - Information security controls
- **Cybersecurity insurance requirements**

---

### 4. Audit Plan (High-Level)

A simplified ISO 27001–aligned audit plan:

### Phase 1: Planning

- Define ISMS scope
- Identify information assets
- Review policies and procedures
- Identify legal and regulatory obligations

### Phase 2: Risk Assessment

- Identify threats (e.g., ransomware, insider threats)
- Identify vulnerabilities (e.g., outdated systems, weak access control)
- Evaluate risk likelihood and impact

### Phase 3: Control Evaluation (Annex A)

Review relevant controls such as:

- A.5 – Information security policies
- A.8 – Asset management
- A.9 – Access control
- A.12 – Operations security
- A.13 – Network security
- A.17 – Business continuity
- A.18 – Compliance

### Phase 4: Reporting

- Identify nonconformities
- Document risks and gaps
- Provide corrective action recommendations

# Step 2: Conduct Risk Assessment (DO)

| Non-Conformity | Risk Level | Potential Impact | ISO 27001 Annex A Control |
| --- | --- | --- | --- |
| Doctors share user accounts to access patient records | **HIGH** | Patient data leaks, lack of accountability, unauthorized access | **A.9.2.1** User registration and de-registration |
| No Multi-Factor Authentication (MFA) for EMR access | HIGH | Credential compromise, ransomware spread | **A.9.4.2** Secure log-on procedures |
| Outdated operating systems on medical workstations | HIGH | Malware infection, system compromise | **A.12.6.1** Management of technical vulnerabilities |
| Infrequent data backups (weekly only) | HIGH | Permanent loss of patient data after ransomware | **A.12.3.1** Information backup |
| Backups stored on same network as production systems | HIGH | Backups encrypted by ransomware | **A.17.1.3** Verify, review and evaluate information security continuity |
| Excessive user privileges for nurses and interns | MEDIUM | Accidental or malicious data modification | **A.9.1.2** Access to networks and network services |
| Lack of security awareness training for hospital staff | MEDIUM | Phishing success, credential theft | **A.7.2.2** Information security awareness, education and training |
| No centralized log monitoring or SIEM | MEDIUM | Delayed detection of attacks | **A.12.4.1** Event logging |
| Third-party EMR vendor not formally risk-assessed | MEDIUM | Supply chain compromise | **A.15.1.1** Information security policy for supplier relationships |

---

# Step 3: Test ISO 27001 Controls (CHECK)

In this phase, the auditor **verifies whether ISO 27001 Annex A controls are implemented, effective, and producing evidence**.

Testing is done through:

- Document review (policies, procedures)
- Technical verification (systems, configurations)
- Interviews and observation (staff awareness)

---

## Control Testing Areas

### 1. Policy Review (Administrative Controls)

- Information Security Policy
- Data Protection Policy
- Access Control Policy
- Incident Response Policy
- Backup & Business Continuity Policy

---

### 2. Technical Control Testing

- Encryption of EMRs (at rest & in transit)
- Access controls and authentication
- Backup configuration and restore testing
- Logging and monitoring
- Network segmentation

---

### 3. Human Factor & Awareness

- Security awareness training
- Phishing simulations
- Staff knowledge of incident reporting

| ISO 27001 Control | Audit Question | Compliance | Findings / Evidence |
| --- | --- | --- | --- |
| **A.5.1.1** Information security policies | Are security policies documented and approved? | Partial | Policies exist but not reviewed in last 2 years |
| **A.6.1.2** Information security roles | Are security roles defined and assigned? | Yes | Roles documented, but not communicated |
| **A.7.2.2** Security awareness training | Have employees received cybersecurity training? | **No** | No formal training records found |
| **A.9.2.3** Privileged access management | Are privileged accounts restricted and reviewed? | No | Doctors share accounts |
| **A.9.4.2** Secure log-on procedures | Is MFA enforced for EMR access? | No | Password-only authentication |
| **A.10.1** Cryptographic controls | Is patient data encrypted? | Partial | Encryption at rest only |
| **A.12.3.1** Backup management | Are backups performed and tested? | Partial | Backups exist, restore not tested |
| **A.12.4.1** Event logging | Are security logs collected and reviewed? | No | No centralized log monitoring |
| **A.13.1.3** Network segregation | Are medical systems isolated from office IT? | No | Flat network |
| **A.16.1.1** Incident management | Is there an incident response process? | Partial | Informal response, no documentation |

## Sample Evidence Collected

- Missing training attendance logs
- Screenshots of shared EMR accounts
- Backup schedules without restore test reports
- Network diagrams showing lack of segmentation
- Absence of SIEM or log review records

---

## Key Non-Conformities Identified

### Major Non-Conformities

- No security awareness training (A.7.2.2)
- Shared user accounts (A.9.2.3)
- No MFA for EMR systems (A.9.4.2)
- No tested backups (A.12.3.1)

### Minor Non-Conformities

- Policies outdated
- Partial encryption
- Informal incident response process

---

# Step 4: Recommended Corrective Actions (ACT)

In this phase, students must **define concrete actions** to eliminate the root causes of non-conformities and **improve the ISMS**.

| Non-Conformity | Corrective Action (What must be done?) | ISO 27001 Control |
| --- | --- | --- |
| Doctors share user accounts | Enforce **unique user IDs** for all medical staff and prohibit shared accounts through policy and technical controls | A.9.2.1 |
| No MFA for EMR systems | Implement **Multi-Factor Authentication (MFA)** for all users accessing EMRs, especially remote access | A.9.4.2 |
| No cybersecurity awareness training | Design and deploy **mandatory annual security awareness training** for all hospital employees | A.7.2.2 |
| Outdated operating systems | Establish a **patch management program** and upgrade unsupported systems | A.12.6.1 |
| Backups not tested | Perform **regular backup restore tests** and document results | A.12.3.1 |
| Backups stored on same network | Implement **offline or immutable backups** (air-gapped or cloud with immutability) | A.17.1.3 |
| Excessive user privileges | Apply **role-based access control (RBAC)** and conduct quarterly access reviews | A.9.1.2 |
| No centralized log monitoring | Deploy a **SIEM or centralized logging solution** with alerting | A.12.4.1 |
| Flat network architecture | Implement **network segmentation** separating medical devices, servers, and office IT | A.13.1.3 |
| Informal incident response | Develop and approve a **formal Incident Response Plan**, including ransomware playbooks | A.16.1.1 |
| Third-party risks not assessed | Conduct **supplier security risk assessments** and update contracts with security clauses | A.15.1.1 |

---

# Additional Questions

1. How does ISO 27001 differ from HIPAA in hospital cybersecurity?

| Aspect | ISO/IEC 27001 | HIPAA |
| --- | --- | --- |
| Type | **International standard** | **US federal law** |
| Purpose | Establishes an **Information Security Management System (ISMS)** | Protects **Protected Health Information (PHI)** |
| Scope | All information assets (clinical, financial, HR, IT) | PHI only |
| Approach | **Risk-based**, continuous improvement (PDCA) | **Rule-based** compliance |
| Certification | Can be **certified** by an external auditor | No certification (legal compliance) |
| Applicability | Any organization, any country | US healthcare entities & partners |
| Controls | Flexible (Annex A controls selected via risk assessment) | Required administrative, physical, and technical safeguards |

*ISO 27001 tells hospitals **how to manage security holistically**, while HIPAA tells them **what must be protected legally***.

2. What security controls should apply to mobile healthcare apps?

Mobile healthcare apps handle **high-risk patient data**, so controls must cover **device, app, and user security**.

### Required Security Controls (ISO 27001–Aligned)

### Access & Authentication

- Strong authentication (MFA)
- Automatic session timeout
- Role-based access control (RBAC)

### Data Protection

- End-to-end encryption (TLS)
- Encrypted local storage
- No plaintext PHI on device

### Device Security

- Mobile Device Management (MDM)
- Remote wipe capability
- Jailbreak/root detection

### Application Security

- Secure coding practices (OWASP Mobile Top 10)
- Regular security testing
- API access control

### Compliance & Monitoring

- Logging of access to patient data
- Privacy consent management
- Regular risk assessments

**Relevant ISO Controls:**

- A.9 Access control
- A.10 Cryptography
- A.12 Operations security
- A.14 Secure system development
    
    

3. If a USB drive with patient records was lost, how should the hospital respond?

This is a **security incident involving potential data breach**.

### Step-by-Step Incident Response (ISO 27001)

### 1️⃣ Contain

- Confirm what data was on the USB
- Determine if data was encrypted
- Disable related user access if needed

### 2️⃣ Assess Impact

- Identify number of affected patients
- Evaluate confidentiality breach risk
- Determine legal notification obligations

### 3️⃣ Notify

- Report internally to the incident response team
- Notify regulators (e.g., HIPAA, PIPEDA, GDPR) if required
- Inform affected patients within legal timeframes

### 4️⃣ Recover

- Ensure no further data exposure
- Monitor for misuse of exposed data

### 5️⃣ Prevent Recurrence

- Ban or restrict USB usage
- Enforce encryption on removable media
- Provide staff training on data handling

**Relevant ISO Controls:**

- A.16.1.1 Incident management
- A.8.3.2 Disposal of media
- A.13.2.1 Information transfer policies
- A.7.2.2 Security awareness training

## Summary

This audit identified 4 major and 4 minor non-conformities across access
control, backup management, network security, and staff awareness.
Immediate priorities include enforcing MFA, implementing unique user accounts,
deploying a SIEM, and establishing a formal incident response plan.