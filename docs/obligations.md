# Bright Bean Coffee

## Obligations Register (v0.2 draft)

| Obligation | Type | Why it applies to Bright Bean | Where to read it |
| :--- | :--- | :--- | :--- |
| **POPIA (Protection of Personal Information Act 4 of 2013)** | Law (statutory) | Bright Bean processes personal information of South African employees, retail customers, and business contacts across 24 enterprise and cloud systems. | Condition 7 (Security Safeguards), sections 19 to 22 |
| **Muza IT operator agreement (POPIA s21)** | Contractual obligation | Bright Bean, as responsible party, must have a written contract ensuring Muza IT, as operator, establishes and maintains the section 19 security measures. Muza must also notify Bright Bean immediately of suspected unauthorised access. | POPIA section 21(1) and (2) |
| **PCI-DSS v4.0.1** | Contractual standard | Bright Bean accepts credit and debit card payments through EFTPOS terminals and connected network elements. v4.0 was retired on 31 December 2024, so v4.0.1 is the version to cite. | Requirements 7, 8 and 9 (sub-requirements listed in section 3) |
| **CIS Controls v8 (IG2, plus Safeguard 6.8 from IG3)** | Framework (voluntary) | Primary technical framework for account management, centralised access, and role-based access control in a business with 5 IT staff and an MSP. | Safeguards 4.7, 5.1, 5.3, 5.4, 6.1, 6.2, 6.4, 6.5, 6.6, 6.7, 6.8 |
| **NIST CSF 2.0** | Framework (voluntary) | Secondary governance framework for reporting and for aligning access controls to the six functions: Govern, Identify, Protect, Detect, Respond, Recover. | Category PR.AA (Identity Management, Authentication, and Access Control): PR.AA-01, -03, -05, -06 |
| **EU GDPR / UAE data protection law / US state privacy laws** | Law (statutory, international) | **To verify:** whether sales to the USA, France and Dubai trigger these laws, for example through GDPR Article 3(2). | EU GDPR Articles 3 and 32; UAE Federal Decree-Law No. 45 of 2021; US state privacy laws |

---

## 1. Governance and Implementation Choices

### CIS Implementation Group: IG2, plus Safeguard 6.8
Bright Bean adopts **Implementation Group 2 (IG2)**. IG1 covers essential cyber hygiene, but Bright Bean's complexity (5 internal IT staff, an MSP, cardholder data under PCI-DSS, and employee and customer personal information under POPIA) calls for IG2. Centralized Access Control (Safeguard 6.7) is an IG2 safeguard.

**Safeguard 6.8 (Define and Maintain Role-Based Access Control)** is listed in IG3, not IG2. Bright Bean selects it on purpose, because the Day 1 review found no role-based access and new hires' permissions are copied from existing staff. The adoption is therefore "IG2 plus selected IG3 safeguard 6.8."

### Operator Privilege Scope: Muza IT
As an operator under POPIA, **Muza IT** holds administrative access on **10 systems** (`systems-inventory.md`): Entra ID, Microsoft 365, Windows Workstations, Endpoint Detection and Response (EDR), Enterprise Password Manager, IT Service Desk, Network and Firewall Infrastructure, Remote Monitoring and Management (RMM), Secure VPN Gateway, and Microsoft Azure Cloud Platform.

---

## 2. Statutory Alignment: POPIA (Condition 7, Sections 19 to 22)

* **Section 19 (Security measures on integrity and confidentiality):** requires appropriate, reasonable technical and organisational measures to prevent unauthorised access. Section 19(2) requires reasonable measures to identify foreseeable internal and external risks, establish and maintain safeguards, regularly verify that they are implemented, and keep them updated. This is the legal basis for periodic access reviews. It does not set a frequency.
* **Section 20 (Information processed by operator or person acting under authority):** an operator (Muza IT) may process personal information only with the knowledge or authorisation of Bright Bean, and must treat it as confidential.
* **Section 21 (Security measures regarding information processed by operator):** (1) Bright Bean, as responsible party, must have a written contract with the operator requiring it to establish and maintain the section 19 safeguards. (2) The operator must notify Bright Bean **immediately** when it has reasonable grounds to believe personal information has been accessed or acquired by an unauthorised person.
* **Section 22 (Notification of security compromises):** where there are reasonable grounds to believe personal information has been accessed or acquired by an unauthorised person, Bright Bean must notify the Information Regulator and, unless their identity cannot be established, the affected data subjects. Notification must be made **as soon as reasonably possible after discovery** (s22(2)), taking account of the legitimate needs of law enforcement and measures needed to determine the scope of the compromise. POPIA sets no fixed deadline such as the GDPR's 72 hours. This matters for leaver failures and for MSP credential compromises.

---

## 3. Contractual Alignment: PCI-DSS v4.0.1

### In-Scope Systems (to be confirmed with the acquiring bank)
1. **Card Payment Terminals (EFTPOS):** hardware that captures card transactions.
2. **Mobile POS:** till software that sends transaction totals to the EFTPOS readers.
3. **Network and Firewall Infrastructure:** routers, switches, and firewalls that separate card data flows and carry traffic to the acquiring bank.

### Core Access Requirements
* **Requirement 7 (Restrict access to system components and cardholder data by business need to know):** role-based access and least privilege.
* **Requirement 8 (Identify users and authenticate access):** unique accounts, strong authentication, MFA for access into the cardholder data environment, and removal of inactive accounts.
* **Requirement 9 (Restrict physical access):** physical controls over payment terminals, cabling, and server areas.

### Sub-requirements cited in `risk-register.md`
*Confirm each number and its wording against the PCI-DSS v4.0.1 document before publishing.*

| Sub-requirement | Subject |
| :--- | :--- |
| 2.2.2 | Vendor default accounts changed or disabled |
| 7.2.2 | Access assigned by job classification and function, with least privilege |
| 7.2.4 | User and vendor access reviewed at least every six months |
| 8.2.5 | Terminated users' access revoked immediately |
| 8.2.6 | Inactive user accounts removed or disabled within 90 days |
| 8.4.2 | MFA for access into the cardholder data environment |
| 8.6.1 | System and application accounts used interactively only by exception |
| 9.5.1 | Payment terminals protected from tampering and substitution |

> **Status: to verify with the acquiring bank:** merchant level and Self-Assessment Questionnaire (SAQ) type. SAQ A and SAQ A-EP are for **e-commerce (card-not-present)** merchants, so they do not fit in-store terminals. For in-person terminals the candidates are **SAQ B-IP** (standalone, PTS-approved, IP-connected terminals, isolated from other systems) or **SAQ P2PE** (a validated point-to-point encryption solution). Because the Mobile POS till software feeds the terminals, isolation may not hold, so SAQ C or SAQ D could apply instead. Also confirm that online orders placed through CartSmartz never expose card data to Bright Bean's systems.

---

## 4. International Market Assessment (GDPR Article 3 Test)

The extraterritorial reach of the EU GDPR is tested under **Article 3**:
* **Article 3(1) (establishment):** applies if processing happens in the context of an EU establishment.
* **Article 3(2) (targeting):** applies to non-EU organisations if processing relates to (a) offering goods or services to people in the EU, or (b) monitoring their behaviour in the EU.

> **Status: to verify.** Confirm with international sales leads whether foreign transactions involve end-consumer personal data directly, or run only through third-party platforms (for example CartSmartz) and business distributors. The UAE and US state laws need the same check.

---

## 5. CIS Controls v8 Safeguard Mapping

Access Control policy statements map to these safeguards. Names follow CIS's wording. State in the final policy whether you cite v8 or v8.1.

| Safeguard | Name | What it requires (summary) |
| :--- | :--- | :--- |
| 4.7 | Manage Default Accounts on Enterprise Assets and Software | Manage, disable, or change default accounts and credentials. |
| 5.1 | Establish and Maintain an Inventory of Accounts | Keep an account inventory and validate that all active accounts are authorized, at least quarterly. |
| 5.3 | Disable Dormant Accounts | Delete or disable dormant accounts after 45 days of inactivity, where supported. |
| 5.4 | Restrict Administrator Privileges to Dedicated Administrator Accounts | Use separate administrator accounts, not daily-use accounts, for admin work. |
| 6.1 | Establish an Access Granting Process | Grant access on new hire, rights grant, or role change through a defined process (joiner and mover). |
| 6.2 | Establish an Access Revoking Process | Disable accounts immediately on termination, rights revocation, or role change (leaver and mover). |
| 6.4 | Require MFA for Remote Network Access | MFA for remote connections such as the VPN. |
| 6.5 | Require MFA for Administrative Access | MFA on all administrative accounts, where supported. |
| 6.6 | Establish and Maintain an Inventory of Authentication and Authorization Systems | Inventory the systems that authenticate and authorize users (Entra ID, VPN, Password Manager: `systems-inventory.md`). |
| 6.7 | Centralize Access Control (IG2) | Centralize access control through a directory or SSO service such as Entra ID. |
| 6.8 | Define and Maintain Role-Based Access Control (IG3, selected) | Define and document the access rights each role needs. |

---

## 6. NIST CSF 2.0 Mapping (category PR.AA)

| Subcategory | Meaning (summary) | Used in |
| :--- | :--- | :--- |
| PR.AA-01 | Identities and credentials for authorized users, services, and hardware are managed by the organization. | R06 |
| PR.AA-03 | Users, services, and hardware are authenticated. | R07 |
| PR.AA-05 | Access permissions, entitlements, and authorizations are defined in a policy, managed, enforced, and reviewed, applying least privilege and separation of duties. | R11, R12 |
| PR.AA-06 | Physical access to assets is managed, monitored, and enforced commensurate with risk. | Coverage Gaps note |

---

## 7. Drafting Notes for the Access Control Policy

1. **Inactive accounts:** CIS 5.3 says 45 days and PCI 8.2.6 says 90 days. State **45 days** in the policy, which satisfies both.
2. **Access reviews:** PCI 7.2.4 requires reviews at least every six months, and CIS 5.1 requires account validation at least quarterly. A **quarterly** review satisfies both. POPIA s19(2) supports regular verification but sets no frequency.
3. **Breach reporting:** Muza must tell Bright Bean immediately (s21(2)). Bright Bean must then notify the Regulator and data subjects as soon as reasonably possible (s22). The Incident Response policy needs to reflect both steps.
4. **Role-based access:** 6.8 is a deliberate IG3 selection and needs a documented role-to-access matrix.

---

## 8. Verification Status

| Item | Status |
| :--- | :--- |
| POPIA Condition 7 covers ss19 to 22; s21 written contract and immediate operator notice; s22 timing ("as soon as reasonably possible") | Checked against published legal sources and Information Regulator material |
| PCI-DSS v4.0.1 is the only active version; v4.0 retired 31 December 2024 | Checked against PCI SSC and secondary sources |
| SAQ types (A and A-EP e-commerce; B-IP and P2PE for terminals) | Checked against PCI SSC-derived guidance; final SAQ **to verify with acquiring bank** |
| CIS safeguard names, 45-day rule, quarterly account validation, IG placement of 6.6 to 6.8 | Checked against CIS Controls v8 text and the IG handout; confirm in the CIS spreadsheet before publishing |
| PCI sub-requirement numbers and NIST PR.AA subcategory wording | **Confirm against the source documents** |
| GDPR, UAE, US state applicability | **To verify** |
