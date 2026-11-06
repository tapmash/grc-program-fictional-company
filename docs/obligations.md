# Bright Bean Coffee — Obligations Register & Framework Mapping

| Obligation | Type | Why it applies to Bright Bean | Where to read it |
| :--- | :--- | :--- | :--- |
| **POPIA (Protection of Personal Information Act 4 of 2013)** | Law (Statutory) | Processing personal information of SA employees, retail customers, and business contacts across 24 enterprise and cloud systems. | Condition 7 (Security Safeguards), Sections 19–22 |
| **Muza IT Operator Agreement** | Contractual Obligation | Mandates that third-party operators (Muza IT) processing data for Bright Bean must establish and maintain Section 19 security safeguards under a binding written contract. *To verify: locate the signed Muza contract and check it contains the s21 clauses.* | POPIA Section 21(1) & 21(2) |
| **PCI-DSS v4.0.1** | Contractual Standard | Direct acceptance of credit/debit card payments via EFTPOS terminals and associated cardholder data network elements. | Requirements 7.2.1, 7.2.2, 7.2.4, 8.2.1, 8.2.2, 8.2.5, 8.2.6, 8.4.2, 8.4.3, 8.6.1, 9.5.1 |
| **CIS Controls v8** | Framework (Voluntary) | Primary technical framework selected to govern account management, centralized access, and role-based access control (RBAC) across an SMB with 5 IT staff and an MSP. | Safeguards 4.7, 5.1, 5.3, 5.4, 6.1, 6.2, 6.3, 6.4, 6.5, 6.6, 6.7, 6.8 |
| **NIST CSF 2.0** | Framework (Voluntary) | Secondary governance framework used for executive reporting and aligning access controls to high-level functions (Identify, Protect, Detect, Respond, Recover). | PR.AA-01, PR.AA-02, PR.AA-03, PR.AA-04, PR.AA-05, PR.AA-06 |
| **EU GDPR / US State Laws / UAE Data Protection Law** | Law (Statutory - International) | To verify: Potential applicability based on whether direct international sales trigger extraterritorial targeting provisions (GDPR Art. 3(2)). *To verify: check if UAE buyers operate on mainland UAE (Federal Decree-Law No. 45/2021) or within free zones like DIFC (DIFC Law No. 5/2020).* | EU GDPR Art. 3 & 32; UAE Federal Decree-Law No. 45/2021 / DIFC Law No. 5/2020; US State Privacy Acts |

---

## 1. Statutory Alignment: POPIA (Condition 7, Sections 19–22)

* **Section 19 (Security measures on integrity and confidentiality):** Mandates technical and organizational measures to prevent unauthorized access. Specifically, **Section 19(2)(a)** requires identifying reasonably foreseeable internal and external risks to personal information, **Section 19(2)(b)** requires establishing and maintaining appropriate safeguards against those risks, **Section 19(2)(c)** requires verifying that safeguards are effectively implemented, and **Section 19(2)(d)** requires ensuring that safeguards are continually updated in response to new risks or deficiencies.
* **Section 20 (Information processed by operator):** Requires an operator (Muza IT) to process personal information only with the knowledge or authorization of Bright Bean and treat all data as strictly confidential.
* **Section 21 (Security measures regarding operator):**
  * **21(1):** Requires Bright Bean (Responsible Party) to ensure via a written contract that Muza IT (Operator) establishes and maintains Section 19 security safeguards.
  * **21(2):** Mandates that Muza IT must immediately notify Bright Bean where there are reasonable grounds to believe that personal information has been accessed or acquired by any unauthorized person.
* **Section 22 (Notification of security compromises):** Requires that where there are reasonable grounds to believe personal information has been accessed by an unauthorized person, Bright Bean must notify the Information Regulator and affected data subjects as soon as reasonably possible after discovering the compromise.

### Operator Privilege Scope: Muza IT
Muza IT holds administrative privileges across 10 of Bright Bean’s 24 systems: Entra ID, Microsoft 365, Windows Workstations, Endpoint Detection & Response (EDR), Enterprise Password Manager, IT Service Desk, Network & Firewall Infrastructure, Remote Monitoring & Management (RMM), Secure VPN Gateway, and Microsoft Azure Cloud Platform.

---

## 2. Contractual Alignment: PCI-DSS v4.0.1

### In-Scope Systems
1. **Card Payment Terminals (EFTPOS):** Direct card transaction capture hardware.
2. **Mobile POS:** Till software generating transaction totals sent to EFTPOS readers.
3. **Network & Firewall Infrastructure:** Routers, switches, and firewalls isolating cardholder data flows to acquiring banks.

### Core Sub-Requirement Mapping
* **7.2.1:** Role-based access control (RBAC) is defined and covers all system components.
* **7.2.2:** Access is granted to individuals based on job function and least privilege.
* **7.2.4:** User access accounts and their respective access privileges—including third-party and vendor accounts—are reviewed at least once every six months.
* **8.2.1:** All users are assigned a unique ID before being allowed access to system components.
* **8.2.2:** Shared, group, or generic IDs and credentials are used only on an exception basis, when necessary for business operations, and must be explicitly approved and managed to ensure individual accountability.
* **8.2.5:** Access for terminated users is immediately revoked.
* **8.2.6:** Inactive user accounts are removed or disabled within 90 days (Bright Bean enforces a stricter 45-day limit per CIS 5.3).
* **8.4.2:** Multi-Factor Authentication (MFA) is implemented for all access into the Cardholder Data Environment (CDE).
* **8.4.3:** MFA is implemented for all remote network access originating outside the entity network.
* **8.6.1:** Accounts belonging to systems and applications (service accounts) are used interactively only by exception and with explicit authorization.
* **9.5.1:** POI (Point of Interaction) payment card devices are protected from tampering and unauthorized replacement.

> **Status:** *To verify: merchant processing level and which Self-Assessment Questionnaire (SAQ B, SAQ B-IP, SAQ P2PE, SAQ C, SAQ C-VT, or other specific retail/terminal SAQ types) applies, via the acquiring bank.*

---

## 3. CIS Implementation Group Selection
Bright Bean adopts CIS Controls v8 **Implementation Group 2 (IG2)** to establish role-based access control and centralized authentication across its 5 internal IT staff and MSP managed environment. While basic hygiene is covered by IG1, IG2 safeguards (and targeted IG3 safeguards like 6.8) are necessary to secure cardholder data and POPIA-regulated personal records across 24 systems.

---

## 4. NIST CSF 2.0 Identity & Access Subcategories (PR.AA)
* **PR.AA-01:** Identities and credentials for authorized users, services, and hardware are managed by the organization.
* **PR.AA-02:** Identities are proofed and bound to credentials based on the context of interactions.
* **PR.AA-03:** Users, services, and hardware are authenticated.
* **PR.AA-04:** Identity assertions are protected, conveyed, and verified.
* **PR.AA-05:** Access permissions, entitlements, and authorizations are defined in a policy, managed, enforced, and reviewed, and incorporate the principles of least privilege and separation of duties.
* **PR.AA-06:** Physical access to assets is managed, monitored, and enforced commensurate with risk.

---

## 5. CIS Controls v8 Safeguard Inventory & IG Mapping

| Safeguard | CIS Safeguard Title | IG | Policy Application |
| :--- | :--- | :--- | :--- |
| **4.7** | Manage Default Accounts on Enterprise Assets and Software | IG1 | Disable or change default credentials across hardware, firewalls, and applications. |
| **5.1** | Establish and Maintain an Inventory of Accounts | IG1 | Maintain an active inventory of user and administrative accounts. |
| **5.3** | Disable Dormant Accounts | IG1 | Automatically disable accounts inactive for more than 45 days (where supported). |
| **5.4** | Restrict Administrator Privileges to Dedicated Administrator Accounts | IG1 | Require administrators to use separate, dedicated admin accounts for administrative tasks. |
| **6.1** | Establish an Access Granting Process | IG1 | Standardize onboarding/role-change procedures for granting access (Joiners & Movers). |
| **6.2** | Establish an Access Revoking Process | IG1 | Revoke access immediately upon employee termination or role change (Leavers). |
| **6.3** | Require MFA for Externally-Exposed Applications | IG1 | Enforce MFA for all public-facing and SaaS applications (e.g., M365, CartSmartz). |
| **6.4** | Require MFA for Remote Network Access | IG1 | Enforce MFA for all remote network access (e.g., Secure VPN Gateway). |
| **6.5** | Require MFA for Administrative Access | IG1 | Enforce mandatory MFA for all administrative accounts across all 10 admin systems. |
| **6.6** | Establish and Maintain an Inventory of Authentication and Authorization Systems | IG2 | Maintain an inventory of all authentication systems (Entra ID, local DBs, vendor portals). |
| **6.7** | Centralize Access Control | IG2 | Enforce SSO and centralized access control via Entra ID across enterprise applications. |
| **6.8** | Define and Maintain Role-Based Access Control | IG3 | Implement RBAC matrix linking job roles directly to system access rights. Adopted as an intentional IG3 override to secure POPIA and PCI systems. |

---

## 6. Open "To Verify" Items
1. Locate the signed Muza IT contract and confirm it contains the POPIA s21 clauses.
2. Confirm merchant level and applicable SAQ with the acquiring bank.
3. Confirm GDPR Article 3(2) applicability for EU sales, and whether UAE buyers fall under the mainland law or DIFC.
4. Confirm US state privacy law applicability by state of sale.
