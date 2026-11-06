# Bright Bean Coffee — Access Control Risk Register (v0.2 draft)

| ID | Risk (who or what harms which asset, and how) | Systems affected | L (1-3) | I (1-3) | Rating | Obligation / safeguard | Owner (proposed) | Treatment (proposed) |
| :--- | :--- | :--- | :---: | :---: | :---: | :--- | :--- | :--- |
| **R01** | A departed employee keeps working access, especially on platforms outside the main directory such as the CartSmartz Seller Portal, which managers often forget to list, and uses it to view or change confidential personnel, customer, or financial data. | Microsoft Entra ID, Microsoft 365, Payroll & HR Portal, CartSmartz Seller Portal | 3 | 3 | 9 | CIS 6.2 / POPIA s19 | IT Manager | Mitigate |
| **R02** | A privileged Muza IT technician with Global Admin access makes unauthorized or mistaken changes to core systems, and no one at Bright Bean reviews that activity. | Microsoft Azure Cloud Platform, Network & Firewall Infrastructure, Remote Monitoring & Management (RMM) | 2 | 3 | 6 | POPIA s21 / CIS 5.4 / PCI 7.2.4 | IT Manager | Mitigate |
| **R03** | An external attacker steals or phishes an administrator password and uses it to take control of directory-wide management, tenant configuration, and the password vault. | Microsoft Entra ID, Enterprise Password Manager, Microsoft Azure Cloud Platform | 2 | 3 | 6 | CIS 6.5 / POPIA s19 (*to verify: CDE scope for PCI 8.4.2*) | IT Manager | Mitigate |
| **R04** | An external attacker uses a vendor-supplied default password left enabled on perimeter hardware or production equipment to gain unauthorized access. | Network & Firewall Infrastructure, Automated Packaging Line PLC | 2 (provisional) | 3 | 6 | PCI-DSS v4.0.1 Req 2.2.2 / CIS 4.7 | IT Manager | Mitigate (verify first) |
| **R05** | An unauthorized user gains access through a dormant standard user account in Entra ID that was left active after it was no longer needed. | Microsoft Entra ID, Central Inventory & ERP Database | 3 | 2 | 6 | CIS 5.3 / PCI-DSS 8.2.6 | IT Manager | Mitigate |
| **R06** | A corporate banking credential is shared between users (*to verify*), so unauthorized or fraudulent payments cannot be traced to an individual. | Corporate Internet Banking | 2 (provisional) | 3 | 6 | NIST CSF PR.AA-01 / NIST 800-53 IA-2 (*to verify: bank mandate and dual authorization terms*) | CEO | Mitigate (verify first) |
| **R07** | If personal or unmanaged devices are allowed (*to verify*), an attacker hijacks an active remote session through the Secure VPN Gateway and reaches cloud applications. | Windows Workstations, Microsoft 365, Secure VPN Gateway | 2 (provisional) | 2 | 4 | NIST CSF PR.AA-03 / CIS 6.4 | IT Manager | Mitigate (verify first) |
| **R08** | Role changes and promotions are not followed by removal of old access, so staff accumulate privileges and can reach sensitive financial and payroll data they no longer need. | Payroll & HR Portal, Cloud Accounting Software, Microsoft Entra ID | 3 | 2 | 6 | CIS 6.1, 6.8 / PCI 7.2.2, 7.2.4 | HR Manager | Mitigate |
| **R09** | A former barista's POS PIN stays active because branch leavers are not reliably reported to IT, and the former employee, or anyone who knows the PIN, uses it at the till. | Mobile POS (Point of Sale) | 2 (provisional) | 2 | 4 | CIS 6.2 / PCI 8.2.5 (*to verify: are POS PINs in PCI scope?*) | Regional Branch Operations Manager | Mitigate (verify first) |
| **R10** | A departed Muza IT engineer's named admin account and MFA token stay active because removal is assigned to "Darren or Aisha" with no deadline, and the former engineer, or an attacker, uses it to administer core systems. | Microsoft Entra ID, Network & Firewall Infrastructure, Microsoft Azure Cloud Platform | 2 (provisional) | 3 | 6 | POPIA s21 / CIS 6.2 / PCI 8.2.5 | IT Manager | Mitigate |
| **R11** | New joiners receive permissions copied from an existing colleague instead of a defined role, so they get more access than their job needs, including payroll or banking data. | Microsoft Entra ID, Microsoft 365, Cloud Accounting Software, Payroll & HR Portal | 3 | 2 | 6 | CIS 6.1, 6.8 / PCI 7.2.2 / NIST CSF PR.AA-05 | IT Manager | Mitigate |
| **R12** | The Systems Administrator role, held by one person, administers 21 of 24 systems. If that account is compromised an attacker controls nearly everything, and if the person leaves, nobody else can administer them. | Microsoft Entra ID, Microsoft 365, Microsoft Azure Cloud Platform, Network & Firewall Infrastructure, Enterprise Password Manager, and others (`systems-inventory.md`) | 2 | 3 | 6 | CIS 5.4 / NIST CSF PR.AA-05 / PCI 7.2.2 | IT Manager | Mitigate |

*Note: This register holds the highest-priority access control risks. Owners and treatments are proposals for review.*

---

## Change Log (v0.1 to v0.2)

* **Impact method changed:** impact is now scored on the harm in each scenario, capped by system tier (see Impact Rule). This changed R05 (9 to 6), R07 (6 to 4) and R08 (9 to 6).
* **R01:** CartSmartz Seller Portal added to the systems affected, matching the Day 1 finding that third-party platforms are forgotten at offboarding.
* **R02:** wording changed. Muza accounts are logged and Darren approves privileged access (`company-profile.md`), so the risk is that nobody reviews the activity, not that access is unchecked.
* **R06, R07:** reworded as unverified conditions and marked provisional.
* **R09 to R12 added** from the Day 1 findings (see Finding Trace).
* **Owner and Treatment columns added.**
* **Likelihood 3 evidence corrected:** it now cites the current-state description in `company-profile.md` (informal email and messaging, no standard ticket), not an IT Service Desk process.

---

## Risk Score Legend and Justifications

### Impact Rule
The highest-tier system a risk could harm, per `systems-tiering.md`, sets the **maximum** impact: Tier 1 = 3, Tier 2 = 2, Tier 3 = 1. The score within that cap reflects the harm in the scenario, such as what the specific account or credential can actually reach.

### Likelihood (1 to 3)
* **1 (Unlikely):** Rare; needs several failures together or targeted malicious intent that existing constraints make improbable.
* **2 (Possible):** Occurs periodically through operational friction, ordinary external threat activity, or lack of automated enforcement.
  * *R02:* Muza IT holds Global Admin access (`company-profile.md`) and administers 10 of Bright Bean's 24 systems (`systems-inventory.md`). *To verify: whether Muza admin activity is logged and reviewed.*
  * *R03:* Entra ID has three administrative parties (Systems Administrator, Internal IT Helpdesk, Muza IT); the Password Manager and Azure each have two (Systems Administrator, Muza IT) (`systems-inventory.md`). More privileged credentials means more credentials that could be stolen.
  * *R04 (provisional):* *To verify: whether default credentials were changed on network boundary gear and factory floor equipment when deployed.*
  * *R06 (provisional):* Corporate Internet Banking has four users (CEO, COO, Senior Accountant, AP Officer) and the IT Manager as administrator (`systems-inventory.md`). *To verify: whether banking credentials are individual or shared.*
  * *R07 (provisional):* Field sales staff connect through the Secure VPN Gateway (`systems-inventory.md`). *To verify: whether personal or unmanaged devices are permitted, and what session controls exist.*
  * *R09 (provisional):* The Day 1 review described how branch baristas are added but not how they are removed. *To verify: who tells IT when a branch employee leaves.*
  * *R10 (provisional):* Removal of Muza engineers' accounts is assigned to "Darren or Aisha" with no stated deadline (Day 1 finding). *To verify: contract terms and the actual removal steps.*
  * *R12:* One role administers 21 of 24 systems (`systems-inventory.md`). Compromise or absence of that one person is possible but not routine.
* **3 (Likely):** Probable in normal operations while lifecycle steps depend on manual, informal handling.
  * *R01, R05, R08, R11:* The current state (`company-profile.md`) is that access requests are handled informally by email or messaging, new users' permissions are copied from existing staff, old access is rarely removed when roles change, and third-party platforms are sometimes overlooked at offboarding. Across 81 staff, delays and orphan accounts are likely over time.

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

### Risk Rating Bands
* **1 to 2 (Low):** Acceptable; monitor through routine management.
* **3 to 4 (Medium):** Tolerable with existing controls; requires periodic review and scheduled remediation.
* **6 to 9 (High):** Unacceptable; needs prompt policy enforcement, mandatory MFA, and strict privilege reviews.

---

## Finding Trace (Day 1 findings to this register)

| Day 1 finding | Where covered |
| :--- | :--- |
| No written access policy; informal requests | Addressed by the policy itself; the informal handling is the evidence behind likelihood 3 on R01, R05, R08, R11 |
| No role-based access; permissions copied from others | R11, R08 |
| Approvals implicit, no record | **Open:** add a risk or cover in the policy's approval section |
| HR and managers notify IT separately, no standard form | R01 |
| Permission creep on role changes | R08 |
| Leavers: late notice; third-party platforms forgotten | R01 |
| Keys and cards collected by Facilities or HR, no checklist | **Open:** physical access not yet in this register |
| Branch POS PINs on leaving | R09 |
| Muza engineer removal has no owner or deadline | R10 |
| Systems Administrator on 21 of 24 systems | R12 |
| Card terminals administered only by the external bank | **Open:** add to Coverage Gaps after verifying who manages terminals day to day |

---

## Coverage Gaps Note

| Safeguard / Requirement | Description | Existing Control | To Verify | Revisit Plan |
| :--- | :--- | :--- | :--- | :--- |
| **PCI-DSS 8.6.1** | Service accounts used interactively only by exception. | None documented. The CartSmartz Sync API runs under an "Automated System Service" account (owner: COO; administrators: E-Commerce Integration Specialist, Systems Administrator) (`systems-inventory.md`). | Verify inventory and interactive usage logs for all automated service and API accounts. | Revisit at the Access Control Policy review. |
| **PCI-DSS 9.5.1 / NIST PR.AA-06** | Physical protection of payment terminals (EFTPOS) from tampering. | Card Payment Terminals are administered by the Acquiring Merchant Bank and owned by the Senior Accountant (`systems-inventory.md`); no physical facility checklists documented. | Verify physical inspection logs and tamper-evident seals on all deployed Card Payment Terminals across retail branches. | Revisit at the Access Control Policy review. |
