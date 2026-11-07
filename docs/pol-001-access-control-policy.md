# POL-001 Access Control Policy

## 1. Purpose
This policy establishes the rules governing access to Bright Bean Coffee’s systems, data, and physical premises. It protects enterprise assets against unauthorized access, creeping privilege accumulation, unrecorded approvals, and lingering access from departed staff or third-party contractors. Compliance with this policy supports alignment of access controls with statutory requirements under the Protection of Personal Information Act (POPIA), contractual mandates under PCI-DSS v4.0.1, and technical safeguards defined in CIS Controls v8 (IG2) and NIST CSF 2.0 (PR.AA).

## 2. Scope
This policy applies to:

**Who:** All Bright Bean Coffee personnel (full-time and part-time staff across all 8 branches, head office, and Midrand depot), third-party operators and managed service providers (specifically Muza IT technicians and account managers), and external contractors. Physical site visitors and delivery personnel (such as J&T logistics) carry no logical system access and are governed under physical escort rules.

**What:** All 24 enterprise, cloud, database, network, and operational technology (OT) systems formally documented in **systems-inventory**, as well as all identity providers, service accounts, and data assets contained within them. Tier-based security controls (including multi-factor authentication, access review frequency, and approval workflows) strictly follow the tier assignments defined in systems-tiering.md.

**Where:** All physical locations owned or operated by Bright Bean Coffee—including the Cape Town head office (including the roastery, warehouse and canteen), Midrand distribution depot, and retail store branches—as well as any location where personnel work remotely or in the field.

## 3. Roles and Responsibilities

* **IT Manager (Darren):** Approves privileged access requests and their 12-month renewals, conducts monthly reviews of Global Admin accounts and Muza admin activity, acts as backup for Muza account removal, approves policy exceptions up to 90 days (requiring system owner sign-off for Tier 1 systems), and manages technical oversight of the Muza IT contract.
* **Systems Administrator (Aisha):** Executes standard and privileged provisioning tickets, enforces mandatory MFA configurations, acts as secondary backup for exit ticket processing, owns the 45-day inactivity disabling sweep, and executes same-day removal of Muza IT technician accounts upon notification.
* **IT Helpdesk (Hugo):** Logs and tracks all access control requests via Service Desk tickets, provisions standard user accounts, serves as primary role responsible for disabling accounts on exit tickets, and maintains request approval records for three years.
* **Branch IT Technician (Keanu):** Issues and configures individual POS physical login cards and personal PINs for store staff upon receiving approved Service Desk tickets, disables a leaver’s card and PIN on the same day, and disables lost POS cards immediately upon report.
* **E-Commerce Integration Specialist:** Removes departed personnel and contractor access from the CartSmartz Seller Portal on the same day an exit ticket is received.
* **System Owners:** Approve user access requests for their Tier 1 and 2 systems and conduct quarterly access reviews for all their systems.
* **Line Managers and Branch Managers:** Submit onboarding, role-change, and offboarding tickets, approve baseline team access requests, and raise a ticket for any lost key or card reported by their staff.
* **HR:** Submits formal Service Desk exit tickets on or before an employee's last working day (or immediately upon dismissal) and co-signs the physical leaver checklist.
* **Facilities:** Collects physical keys, fobs, and access cards on an employee's last working day, co-signs the physical leaver checklist, disables lost door cards and fobs on report, escorts and logs physical visitors and J&T logistics personnel, and conducts quarterly active card checks against the staff roster.
* **COO:** Approves all access requests and policy exceptions for the IT Manager, and reviews Darren’s user access quarterly.
* **Muza IT:** Provides same-day written notice for departing or reassigned technicians, maintains technical and organizational security measures under POPIA s21, and submits a verified technician list quarterly.
* **All Personnel:** Maintain strict confidentiality of personal credentials, never share cards, PINs, or passwords, use assigned access strictly for authorized business functions, report lost keys or cards within four hours, and report suspicious activity promptly.

## 4. Policy Statements

### 4.1 Access Requests and Approval

* **4.1.1 Mandatory Request Channel:** All requests for new access, access modifications, or system entitlement changes must be submitted exclusively through the formal IT Service Desk ticketing platform. Verbal, email, or instant messaging requests must not be acted upon by IT personnel. Written notices from Muza IT under section 4.7 must be logged as a ticket by the IT Helpdesk before action is taken.
* **4.1.2 Ticket Authoring:** Access request tickets must be raised exclusively by the requester’s direct Line Manager, Branch Manager, or HR (for exit tickets). Personnel must not submit access request tickets for their own accounts.
* **4.1.3 Role-Based Provisioning:** Access entitlements must be provisioned strictly based on the role-to-access matrix and documented operational necessity. IT personnel must not clone or duplicate access permissions from another employee or colleague.
* **4.1.4 Approval Tiering:** Baseline access requests for Tier 3 systems require written sign-off from the requester's direct Line Manager or Branch Manager. Access requests for Tier 1 and Tier 2 systems require dual sign-off from both the direct Line Manager and the designated System Owner prior to provisioning. Privileged access additionally follows section 4.5.
* **4.1.5 Prohibition of Self-Approval:** Personnel are strictly prohibited from approving their own access requests, privilege upgrades, or policy exceptions under any circumstances. Access requests for the IT Manager (Darren) must be reviewed and approved by the Chief Operating Officer (COO). The COO also provides the System Owner sign-off where the IT Manager owns the system.
* **4.1.6 Audit Record Retention:** The IT Helpdesk must retain complete records of all access request tickets, including authorization sign-offs, ticket timestamps, and fulfillment records, for a minimum of three (3) years.

  ### 4.2 Movers (Role Changes)

* **4.2.1 Notification and Ticket Submission:** When an employee or contractor changes job roles, transfers departments, or moves to a different branch, their new Line Manager or Branch Manager must submit a role-change access ticket via the IT Service Desk prior to or on the effective date of the change.
* **4.2.2 Same-Day Revocation of Prior Access:** Except as permitted under 4.2.4, all system access and permissions associated strictly with the individual's former role must be revoked by IT on the effective date of the role change. Old access entitlements must not be retained "just in case" or for convenience.
* **4.2.3 Provisioning New Role Entitlements:** Access for the new role must be provisioned strictly in accordance with the baseline defined in the role-to-access matrix and must satisfy the approval tiering requirements specified in Section 4.1.4.
* **4.2.4 Transition Exceptions:** If temporary access to former role systems is genuinely required for handover purposes, it must be requested and documented as a formal policy exception under Section 5 (Exceptions), capped at a maximum of 14 calendar days, and approved under Section 5 with the former System Owner’s agreement.
