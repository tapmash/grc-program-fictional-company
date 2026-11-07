# Bright Bean Coffee — Access Control Risk Register (v1.0)

| ID | Risk (who or what harms which asset, and how) | Systems affected | L (1-3) | I (1-3) | Rating | Obligation / safeguard | Owner | Treatment |
| :--- | :--- | :--- | :---: | :---: | :---: | :--- | :--- | :--- |
| **R01** | A departed employee keeps working access, especially on platforms outside the main directory such as the CartSmartz Seller Portal, which managers often forget to list, and uses it to view or change confidential personnel, customer, or financial data. | Microsoft Entra ID, Microsoft 365, Payroll & HR Portal, CartSmartz Seller Portal | 3 | 3 | 9 | CIS 6.2 / POPIA s19 | IT Manager | Mitigate |
| **R02** | A privileged Muza IT technician with Global Admin access makes unauthorized or mistaken changes to core systems, and no one at Bright Bean reviews that activity. | Microsoft Azure Cloud Platform, Network & Firewall Infrastructure, Remote Monitoring & Management (RMM) | 2 (P) | 3 | 6 | POPIA s21 / CIS 5.4 / PCI 7.2.4 | IT Manager | Mitigate (validate first) |
| **R03** | An external attacker steals or phishes an administrator password and uses it to take control of directory-wide management, tenant configuration, and the password vault. | Microsoft Entra ID, Enterprise Password Manager, Microsoft Azure Cloud Platform | 2 | 3 | 6 | CIS 6.5 / POPIA s19 / PCI 8.4.2 (V1) | IT Manager | Mitigate |
| **R04** | An external attacker uses a vendor-supplied default password left enabled on perimeter hardware or production equipment to gain unauthorized access. | Network & Firewall Infrastructure, Automated Packaging Line PLC | 2 (P) | 3 | 6 | PCI-DSS v4.0.1 Req 2.2.2 / CIS 4.7 | IT Manager | Mitigate (validate first) |
| **R05** | An unauthorized user gains access through a dormant standard user account in Entra ID that was left active after it was no longer needed. | Microsoft Entra ID, Central Inventory & ERP Database | 3 | 2 | 6 | CIS 5.3 / PCI-DSS 8.2.6 | IT Manager | Mitigate |
| **R06** | A corporate banking credential is shared between users, so unauthorized or fraudulent payments cannot be traced to an individual. | Corporate Internet Banking | 2 (P) | 3 | 6 | NIST CSF PR.AA-01 | Chief Executive Officer | Mitigate (validate first) |
| **R07** | If personal or unmanaged devices are allowed, an attacker hijacks an active remote session through the Secure VPN Gateway and reaches cloud applications. | Windows Workstations, Microsoft 365, Secure VPN Gateway | 2 (P) | 2 | 4 | NIST CSF PR.AA-03 / CIS 6.4 | IT Manager | Mitigate (validate first) |
| **R08** | Role changes and promotions are not followed by removal of old access, so staff accumulate privileges and can reach sensitive financial and payroll data they no longer need. | Payroll & HR Portal, Cloud Accounting Software, Microsoft Entra ID | 3 | 2 | 6 | CIS 6.1, 6.8 / PCI 7.2.2, 7.2.4 | HR Manager | Mitigate |
| **R09** | A former barista's POS PIN stays active because branch leavers are not reliably reported to IT, and the former employee, or anyone who knows the PIN, uses it at the till. | Mobile POS (Point of Sale) | 2 (P) | 2 | 4 | CIS 6.2 / PCI 8.2.5 (V2) | Regional Branch Operations Manager | Mitigate (validate first) |
| **R10** | A departed Muza IT engineer's named admin account and MFA token stay active because removal is assigned to "Darren or Aisha" with no deadline, and the former engineer, or an attacker, uses it to administer core systems. | Microsoft Entra ID, Network & Firewall Infrastructure, Microsoft Azure Cloud Platform | 2 (P) | 3 | 6 | POPIA s21 / CIS 6.2 / PCI 8.2.5 | IT Manager | Mitigate (validate first) |
| **R11** | New joiners receive permissions copied from an existing colleague instead of a defined role, so they get more access than their job needs, including payroll or banking data. | Microsoft Entra ID, Microsoft 365, Cloud Accounting Software, Payroll & HR Portal | 3 | 2 | 6 | CIS 6.1, 6.8 / PCI 7.2.2 / NIST CSF PR.AA-05 | IT Manager | Mitigate |
| **R12** | The Systems Administrator role, held by one person, administers 21 of 24 systems. If that account is compromised an attacker controls nearly everything, and if the person leaves, nobody else can administer them. | Microsoft Entra ID, Microsoft 365, Microsoft Azure Cloud Platform, Network & Firewall Infrastructure, Enterprise Password Manager, and others (`systems-inventory.md`) | 2 | 3 | 6 | CIS 5.4 / NIST CSF PR.AA-05 / PCI 7.2.2 | IT Manager | Mitigate |
| **R13** | Access is granted on informal approvals (email, Teams or verbal requests to Darren or Hugo) that are not recorded, so Bright Bean cannot show who authorized an access right and excessive or unauthorized access goes unnoticed. | Microsoft Entra ID, Microsoft 365, Payroll & HR Portal, Cloud Accounting Software | 3 | 2 | 6 | CIS 6.1 / POPIA s19 / PCI-DSS documented approval of privileges (V3) | IT Manager | Mitigate |
| **R14** | Keys and access cards of leavers are collected by Facilities or HR with no checklist, so a former employee keeps physical entry to the roastery, warehouse or server area. | Physical Access Control & CCTV | 2 (P) | 2 | 4 | PCI-DSS Req 9 (V4) / NIST CSF PR.AA-06 | Facilities Maintenance Lead | Mitigate (validate first) |
| **R15** | Card payment terminals are administered only by the acquiring merchant bank, so Bright Bean has no internal administrator and cannot tell who changed terminal settings or whether a terminal was tampered with. | Card Payment Terminals (EFTPOS) | 2 (P) | 3 | 6 | PCI-DSS 9.5.1 / NIST CSF PR.AA-06 | Senior Accountant | Mitigate (validate first) |

*Note: This register holds the highest-priority access control risks. **(P)** = provisional: the likelihood rests on a fact not yet validated (see Validation Items). **(V1 to V4)** = obligation reference to be validated against the source standard.*

---

## Validation Items

| Ref | Item to validate | Affects |
| :--- | :--- | :--- |
| R02 | Whether Muza admin activity is logged and reviewed by Bright Bean. | Likelihood |
| R04 | Whether default credentials were changed on network boundary gear and factory floor equipment when deployed. | Likelihood |
| R06 | Whether banking credentials are individual or shared, and the bank mandate and dual authorization terms. | Likelihood |
| R07 | Whether personal or unmanaged devices are permitted, and what session controls exist. | Likelihood |
| R09 | Who tells IT when a branch employee leaves. | Likelihood |
| R10 | Muza contract terms and the actual removal steps for departed engineers. | Likelihood |
| R14 | Whether a key and card return log exists, and how often leavers' cards stay active. | Likelihood |
| R15 | Who manages the terminals day to day, and whether physical inspections happen. | Likelihood |
| V1 | PCI-DSS 8.4.2: whether the cardholder data environment (CDE) is in scope. | Obligation reference |
| V2 | PCI-DSS 8.2.5: whether POS PINs are in PCI scope. | Obligation reference |
| V3 | PCI-DSS requirement number for documented approval of privileges. | Obligation reference |
| V4 | PCI-DSS Req 9: the specific sub-requirement for physical access. | Obligation reference |

---

## Version History

| Version | Changes |
| :--- | :--- |
| v1.0 | R13 (informal approvals), R14 (physical keys and cards) and R15 (card terminals administered only by the bank) added. R02 and R10 treatments aligned with their provisional likelihoods. NIST 800-53 reference removed from R06 (the obligations register covers NIST CSF 2.0 only). Owners checked against `systems-inventory.md` and the R14 tier against `systems-tiering.md`. Validation Items table added. |
| v0.2 | Impact scoring changed to the harm in each scenario, capped by system tier (R05 9 to 6, R07 6 to 4, R08 9 to 6). R01 systems updated with the CartSmartz Seller Portal. R02 reworded. R06 and R07 reworded as unvalidated conditions. R09 to R12 added. Owner and Treatment columns added. Likelihood 3 evidence now cites the informal current-state process in `company-profile.md`. |
| v0.1 | Initial register, R01 to R08. |

---

## Risk Score Legend and Justifications

### Impact Rule
The highest-tier system a risk could harm, per `systems-tiering.md`, sets the **maximum** impact: Tier 1 = 3, Tier 2 = 2, Tier 3 = 1. The score within that cap reflects the harm in the scenario, such as what the specific account or credential can actually reach.

### Likelihood (1 to 3)
* **1 (Unlikely):** Rare; needs several failures together or targeted malicious intent that existing constraints make improbable.
* **2 (Possible):** Occurs periodically through operational friction, ordinary external threat activity, or lack of automated enforcement.
  * *R02 (P):* Muza IT holds Global Admin access (`company-profile.md`) and administers 10 of Bright Bean's 24 systems (`systems-inventory.md`). Whether its activity is logged and reviewed is not yet validated.
  * *R03:* Entra ID has three administrative parties (Systems Administrator, Internal IT Helpdesk, Muza IT); the Password Manager and Azure each have two (Systems Administrator, Muza IT) (`systems-inventory.md`). More privileged credentials means more credentials that could be stolen.
  * *R04 (P):* Whether default credentials were changed on deployment is not yet validated.
  * *R06 (P):* Corporate Internet Banking has four users (CEO, COO, Senior Accountant, AP Officer) and the IT Manager as administrator (`systems-inventory.md`). Whether credentials are individual or shared is not yet validated.
  * *R07 (P):* Field sales staff connect through the Secure VPN Gateway (`systems-inventory.md`). Whether personal or unmanaged devices are permitted is not yet validated.
  * *R09 (P):* The current-state review described how branch baristas are added but not how they are removed. Who tells IT when a branch employee leaves is not yet validated.
  * *R10 (P):* Removal of Muza engineers' accounts is assigned to "Darren or Aisha" with no stated deadline (current-state finding). Contract terms and the actual removal steps are not yet validated.
  * *R12:* One role administers 21 of 24 systems (`systems-inventory.md`). Compromise or absence of that one person is possible but not routine.
  * *R14 (P):* Keys and cards are collected by Facilities or HR with no checklist (current-state finding). Whether a return log exists is not yet validated.
  * *R15 (P):* Terminals are administered by the Acquiring Merchant Bank and owned by the Senior Accountant (`systems-inventory.md`). Who manages them day to day is not yet validated.
* **3 (Likely):** Probable in normal operations while lifecycle steps depend on manual, informal handling.
  * *R01, R05, R08, R11, R13:* The current state (`company-profile.md`) is that access requests are handled informally by email, messaging or verbally, new users' permissions are copied from existing staff, old access is rarely removed when roles change, and third-party platforms are sometimes overlooked at offboarding. Across 81 staff, delays, orphan accounts and unrecorded approvals are likely over time.

### Impact (1 to 3)
* **1 (Minor):** Negligible downtime, no legal exposure, no financial loss or data leakage.
* **2 (Serious):** Noticeable disruption, localized data exposure, or moderate financial or regulatory impact requiring containment and reporting.
* **3 (Severe):** Major commercial impact, significant POPIA exposure, breach of restricted records at scale, or irreversible cash loss.
  * *R01 (3):* A departed employee's account can reach personnel, payroll and customer data. Tier 1 systems are involved.
  * *R02, R10 (3):* Global Admin or named admin access can change or disable core systems. Tier 1 systems are involved.
  * *R03 (3):* A stolen administrator credential reaches the directory, tenant and password vault, all Tier 1.
  * *R04 (3):* A default password on perimeter hardware gives control of the network boundary (Tier 1).
  * *R05 (2):* A dormant standard account reaches only what that user could. The Tier 1 cap is not reached.
  * *R06 (3):* Fraudulent payments are irreversible cash loss (Corporate Internet Banking is Tier 1 by override).
  * *R07 (2):* A hijacked standard remote session reaches what that user can reach.
  * *R08, R11 (2):* Over-privileged existing staff cause localized exposure of financial and payroll data.
  * *R09 (2):* A stale PIN reaches till functions at one branch (Tier 2 cap).
  * *R12 (3):* The role administers nearly all systems, including Tier 1 systems.
  * *R13 (2):* Missing approval records weaken accountability and make over-granting hard to detect. The harm is indirect, so it stays below the Tier 1 cap.
  * *R14 (2):* A former employee's physical entry is limited to the areas the card or key opens (Physical Access Control & CCTV is Tier 2, so the cap is 2).
  * *R15 (3):* Terminal tampering can capture card data at scale (Card Payment Terminals are Tier 1).

### Risk Rating Bands
* **1 to 2 (Low):** Acceptable; monitor through routine management.
* **3 to 4 (Medium):** Tolerable with existing controls; requires periodic review and scheduled remediation.
* **6 to 9 (High):** Unacceptable; needs prompt policy enforcement, mandatory MFA, and strict privilege reviews.

---

## Finding Trace (current-state findings to this register)

| Current-state finding | Where covered |
| :--- | :--- |
| No written access policy; informal requests | Addressed by the policy itself; the informal handling is the evidence behind likelihood 3 on R01, R05, R08, R11, R13 |
| No role-based access; permissions copied from others | R11, R08 |
| Approvals implicit, no record | R13 |
| HR and managers notify IT separately, no standard form | R01 |
| Permission creep on role changes | R08 |
| Leavers: late notice; third-party platforms forgotten | R01 |
| Keys and cards collected by Facilities or HR, no checklist | R14 |
| Branch POS PINs on leaving | R09 |
| Muza engineer removal has no owner or deadline | R10 |
| Systems Administrator on 21 of 24 systems | R12 |
| Card terminals administered only by the external bank | R15 |

---

## Coverage Gaps Note

| Safeguard / Requirement | Description | Existing Control | To Validate | Revisit Plan |
| :--- | :--- | :--- | :--- | :--- |
| **PCI-DSS 8.6.1** | Service accounts used interactively only by exception. | None documented. The CartSmartz Sync API runs under an "Automated System Service" account (owner: COO; administrators: E-Commerce Integration Specialist, Systems Administrator) (`systems-inventory.md`). | Inventory and interactive usage logs for all automated service and API accounts. | Revisit at the Access Control Policy review. |
| **PCI-DSS 9.5.1 / NIST PR.AA-06** | Physical protection of payment terminals (EFTPOS) from tampering. | Card Payment Terminals are administered by the Acquiring Merchant Bank and owned by the Senior Accountant (`systems-inventory.md`); no physical facility checklists documented. Risk recorded as R15. | Physical inspection logs and tamper-evident seals on all deployed Card Payment Terminals across retail branches. | Revisit at the Access Control Policy review. |
