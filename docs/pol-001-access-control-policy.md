# POL-001 Access Control Policy

## Section 1. Purpose
This policy establishes the rules governing access to Bright Bean Coffee’s systems, data, and physical premises. It protects enterprise assets against unauthorized access, creeping privilege accumulation, unrecorded approvals, and lingering access from departed staff or third-party contractors. Compliance with this policy supports alignment of access controls with statutory requirements under the Protection of Personal Information Act (POPIA), contractual mandates under PCI-DSS v4.0.1, and technical safeguards defined in CIS Controls v8 (IG2) and NIST CSF 2.0 (PR.AA).

## Section 2. Scope
This policy applies to:

Who: All Bright Bean Coffee personnel (full-time and part-time staff across all 8 branches, head office, and Midrand depot), third-party operators and managed service providers (specifically Muza IT technicians and account managers), and external contractors. Physical site visitors and delivery personnel (such as J&T logistics) carry no logical system access and are governed under physical escort rules.

What: All 24 enterprise, cloud, database, network, and operational technology (OT) systems formally documented in systems-inventory.md, as well as all identity providers, service accounts, and data assets contained within them. Tier-based security controls (including multi-factor authentication, access review frequency, and approval workflows) strictly follow the tier assignments defined in systems-tiering.md.

Where: All physical locations owned or operated by Bright Bean Coffee—including the Cape Town head office (including the roastery, warehouse and canteen), Midrand distribution depot, and retail store branches—as well as any location where personnel work remotely or in the field.

## 3. Roles and Responsibilities

* **IT Manager (Darren):** Approves privileged access requests and their 12-month renewals, conducts monthly reviews of Global Admin accounts and Muza admin activity, acts as backup for Muza account removal, approves policy exceptions up to 90 days (requiring system owner sign-off for Tier 1 systems), and manages technical oversight of the Muza IT contract.
* **Systems Administrator (Aisha):** Executes standard and privileged provisioning tickets, enforces mandatory MFA configurations, acts as secondary backup for exit ticket processing, owns the 45-day inactivity disabling sweep, and executes same-day removal of Muza IT technician accounts upon notification.
* **IT Helpdesk (Hugo):** Logs and tracks all access control requests via Service Desk tickets, provisions standard user accounts, serves as primary role responsible for disabling accounts on exit tickets, and maintains request approval records for three years.
* **Branch IT Technician (Keanu):** Issues and configures individual POS physical login cards and personal PINs for store staff upon receiving approved Service Desk tickets, disables a leaver’s card and PIN on the same day, and disables lost POS cards immediately upon report.
* **E-Commerce Integration Specialist:** Removes departed personnel and contractor access from the CartSmartz Seller Portal on the same day an exit ticket is received.
* **System Owners:** Approve user access requests for their designated systems (Tiers 1 and 2) and conduct quarterly access reviews for assigned system accounts.
* **Line Managers and Branch Managers:** Submit onboarding, role-change, and offboarding tickets, approve baseline team access requests, and raise a ticket for any lost key or card reported by their staff.
* **HR:** Submits formal Service Desk exit tickets on or before an employee's last working day (or immediately upon dismissal) and co-signs the physical leaver checklist.
* **Facilities:** Collects physical keys, fobs, and access cards on an employee's last working day, co-signs the physical leaver checklist, disables lost door cards and fobs on report, escorts and logs physical visitors and J&T logistics personnel, and conducts quarterly active card checks against the staff roster.
* **COO:** Approves all access requests and policy exceptions for the IT Manager, and reviews Darren’s user access quarterly.
* **Muza IT:** Provides same-day written notice for departing or reassigned technicians, maintains technical and organizational security measures under POPIA s21, and submits a verified technician list quarterly.
* **All Personnel:** Maintain strict confidentiality of personal credentials, never share cards, PINs, or passwords, use assigned access strictly for authorized business functions, report lost keys or cards within four hours, and report suspicious activity promptly.
