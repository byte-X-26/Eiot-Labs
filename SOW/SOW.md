# Annex A — Statement of Work (SOW)
**Penetration Testing Engagement**  
Between **X-CYBER** (“Provider”) and **VET ASSOCIATES** (“Client”)

This Statement of Work (“SOW”) is incorporated into the Penetration Testing Services Agreement (“Agreement”).  
All testing activities described herein are governed by the terms of the master Agreement.

---

# Table of Contents
1. [Engagement Overview](#1-engagement-overview)  
2. [Objectives of the Engagement](#2-objectives-of-the-engagement)  
3. [In-Scope Assets & Testing Targets](#3-in-scope-assets--testing-targets)  
   - [Network & Infrastructure Scope](#31-network--infrastructure-scope)  
   - [AWS & Cloud Environment Scope](#32-aws--cloud-environment-scope)  
   - [Application Scope](#33-application-scope)  
   - [API Scope](#34-api-scope)  
   - [IAM Systems in Scope](#35-iam-systems-in-scope)  
   - [Out-of-Scope Assets](#36-out-of-scope-assets)  
4. [Testing Approach & Methodology](#4-testing-approach--methodology)  
5. [Testing Schedule & Windows](#5-testing-schedule--windows)  
6. [Authorization & Access Requirements](#6-authorization--access-requirements)  
   - [X-CYBER Test Accounts](#61-ldwit-test-accounts-required)  
   - [Breakglass Access](#62-breakglass-access-if-approved)  
7. [Whitelisting & Network Controls](#7-whitelisting--network-controls)  
8. [Backups & Risk Acceptance](#8-backups--risk-acceptance)  
   - [Backup Confirmation](#81-backup-confirmation)  
   - [Production Testing](#82-production-testing-if-requested)  
9. [Deliverables & Reporting Schedule](#9-deliverables--reporting-schedule)  
10. [Data Retention & Destruction](#10-data-retention--destruction)  
11. [Compliance Considerations](#11-compliance-considerations)  
12. [Architecture & Environment Documentation](#12-architecture--environment-documentation)  
13. [Acceptance & Approval](#13-acceptance--approval)

---

# 1. Engagement Overview

**Engagement Title:** ______________________________________________  
**Version:** ____________________  
**Date Issued:** ____________________  
**Prepared By (X-CYBER):** ____________________  
**Client Point of Contact (POC):** ____________________  
**Backup POC:** ____________________

### Engagement Summary  
Provide a high-level description of the systems, cloud environments, applications, and IAM components to be tested.

---

# 2. Objectives of the Engagement

This section defines the security objectives and key questions the penetration test aims to answer.

### Primary Objectives
- Identify vulnerabilities across cloud, on-premises, and hybrid systems.
- Assess IAM strength (OAuth2, OIDC, SAML, API keys, session management).
- Evaluate application/API resilience against OWASP Top 10 and cloud threats.
- Validate controls supporting HIPAA, GDPR, and FedRAMP-aligned environments.
- Identify realistic exploitation paths, privilege escalation routes, and data exposure risks.

**Additional Custom Objectives:**  
____________________________________________________________________________  
____________________________________________________________________________  

---

# 3. In-Scope Assets & Testing Targets

## 3.1 Network & Infrastructure Scope

| Category | Description |
|---------|-------------|
| On-Prem IP Ranges | ______________________________________________ |
| Cloud VPC(s) | ______________________________________________ |
| Subnets (Public/Private) | ______________________________________________ |
| VPN Gateways | ______________________________________________ |
| Load Balancers | ______________________________________________ |
| Firewalls/WAF | ______________________________________________ |
| Other Devices | ______________________________________________ |

---

## 3.2 AWS & Cloud Environment Scope

| AWS Account Name/ID | Environment | Primary Services in Scope |
|---------------------|-------------|----------------------------|
| ___________________ | Dev/Staging/Test/Prod | EC2, RDS, Lambda, API Gateway, S3, IAM, etc. |
| ___________________ | Dev/Staging/Test/Prod | ____________________________________________ |
| ___________________ | Dev/Staging/Test/Prod | ____________________________________________ |

**Cloud Testing Notes:**  
- Testing is limited to **Client-controlled configurations** (IAM, VPC, S3, security groups, etc.).  
- AWS-owned infrastructure is **strictly out of scope**.

---

## 3.3 Application Scope

| Application Name | URL / Domain | Environment | Technologies | Notes |
|------------------|--------------|-------------|--------------|-------|
| _________________ | _________________ | Test/Staging | React, Node.js, etc. | |
| _________________ | _________________ | Test/Staging | Java, Spring Boot, etc. | |
| _________________ | _________________ | Test/Staging | Python, Flask, etc. | |

---

## 3.4 API Scope

| API Name | Endpoint Base URL | Auth Method (OAuth2/OIDC/API Key) | Notes |
|----------|-------------------|------------------------------------|-------|
| _________ | _________________________ | ____________________________ | |
| _________ | _________________________ | ____________________________ | |

---

## 3.5 IAM Systems in Scope

| System / Flow | Technology | In Scope? | Notes |
|----------------|------------|-----------|-------|
| OAuth2 Authorization Code Flow | OAuth2/OIDC | Yes/No | |
| OpenID Connect Authentication | OIDC | Yes/No | |
| SAML SSO | SAML 2.0 | Yes/No | |
| MFA/2FA | TOTP, SMS, Push | Yes/No | |
| JWT Token Handling | Tokens | Yes/No | |
| IAM Privilege Escalation Testing | AWS IAM | Yes/No | |

---

## 3.6 Out-of-Scope Assets  

List all systems that **must not** be tested.

____________________________________________________________________________  
____________________________________________________________________________  

---

# 4. Testing Approach & Methodology

Testing will follow the methodology defined in the master Agreement, including:

- Planning  
- Reconnaissance  
- Enumeration  
- Vulnerability Discovery  
- Controlled Exploitation  
- Post-Exploitation  
- Reporting  

**Engagement-Specific Notes:**  
____________________________________________________________________________  
____________________________________________________________________________  

---

# 5. Testing Schedule & Windows

| Activity | Dates | Notes |
|----------|--------|--------|
| Reconnaissance | __________ | |
| Network Testing | __________ | |
| Cloud/IAM Testing | __________ | |
| Application/API Testing | __________ | |
| Reporting & Review | __________ | |

### Testing Time Windows  
- Allowed Testing Hours: __________________________  
- High-Risk Testing Hours: ________________________  
- Maintenance Window Testing (Optional): __________  

---

# 6. Authorization & Access Requirements

## 6.1 X-CYBER Test Accounts Required

| Account Type | Access Level | Environment | Purpose |
|--------------|--------------|-------------|---------|
| Test User | Standard User | Test/Staging | IAM/Auth testing |
| Test Admin | Limited Admin | Test/Staging | Cloud & IAM escalation testing |
| API Keys / Tokens | Limited Scope | Test/Staging | API testing |

---

## 6.2 Breakglass Access (If Approved)

| Breakglass Method | Approved By | Conditions |
|--------------------|-------------|-----------|
| Temporary IAM Role | ____________ | Only for IAM lockouts |
| Temporary Elevated Admin | ____________ | Only with explicit written approval |

---

# 7. Whitelisting & Network Controls

VET ASSOCIATES must configure whitelisting for X-CYBER’s IP addresses.

| X-CYBER IP / Range | Purpose | Services to Whitelist |
|------------------|---------|------------------------|
| _________________ | Recon/Testing | WAF, Firewall, VPN |
| _________________ | API Testing | API Gateway, Reverse Proxy |

---

# 8. Backups & Risk Acceptance

## 8.1 Backup Confirmation

VET ASSOCIATES confirms that all in-scope systems have been backed up.

| System / Environment | Backup Completed? | Date | Verified By |
|----------------------|-------------------|------|--------------|
| ____________________ | Yes/No | ______ | ______ |
| ____________________ | Yes/No | ______ | ______ |

> **Note:** X-CYBER may refuse testing if backups are incomplete.

---

## 8.2 Production Testing (If Requested)

Production testing is **not included by default**.

If requested:

- Risks acknowledged? Yes / No  
- Guardrails defined? Yes / No  
- Written authorization provided? Yes / No  

**Production Testing Guardrails:**  
____________________________________________________________________________  
____________________________________________________________________________  

---

# 9. Deliverables & Reporting Schedule

| Deliverable | Description | Due Date |
|-------------|-------------|----------|
| Full Report | Technical findings, PoC, remediation | __________ |
| Executive Summary | Leadership overview | __________ |
| Live Readout (Optional) | Walkthrough session | __________ |
| Remediation Guidance (Optional) | Technical Q&A | __________ |

Severity scoring will follow:  
- **CVSS v3.1** for infrastructure/network/cloud findings  
- **OWASP Application Risk Rating** for application/API/IAM findings  

---

# 10. Data Retention & Destruction

## 10.1 Retention Period  
Select one:

- ☐ 30 days  
- ☐ 60 days  
- ☐ 90 days  
- ☐ Other: ________________

---
## 10.2 Destruction Method  
Select one:

- ☐ Secure wipe (file-level)  
- ☐ Cryptographic erase  
- ☐ Return to VET ASSOCIATES (encrypted)  
- ☐ Other: _______________________  

VET ASSOCIATES may request a destruction confirmation document.

---

# 11. Compliance Considerations

## 11.1 Regulatory Factors (Check All That Apply)

- ☐ HIPAA  
- ☐ FedRAMP-aligned testing  
- ☐ GDPR  
- ☐ CCPA / state privacy laws  
- ☐ PCI-DSS  
- ☐ Other: ____________________

---

## 11.2 Compliance Notes

____________________________________________________________________________  
____________________________________________________________________________  

---

# 12. Architecture & Environment Documentation

## 12.1 Client-Provided Documentation

- ☐ Network Diagrams  
- ☐ AWS Architecture Diagram  
- ☐ IAM Role Map  
- ☐ API Documentation  
- ☐ Application Architecture  
- ☐ Data Flow Diagrams  
- ☐ Logging/Monitoring Overview  

---

## 12.2 Attachments  
(Add any reference documents)

____________________________________________________________________________  
____________________________________________________________________________  

---


# 13. Acceptance & Approval

By signing below, both Parties approve this SOW and authorize X-CYBER to perform the testing described.

**X-CYBER – Authorized Representative**  
Name: ___________________________  
Title: ____________________________  
Signature: ________________________  
Date: _____________________________  

**VET ASSOCIATES – Authorized Representative**  
Name: ___________________________  
Title: ____________________________  
Signature: ________________________  
Date: _____________________________  