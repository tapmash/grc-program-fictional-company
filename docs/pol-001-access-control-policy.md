# POL-001 Access Control Policy

## 1. Purpose
This policy establishes the rules governing access to Bright Bean Coffee’s systems, data, and physical premises. It protects enterprise assets against unauthorized access, creeping privilege accumulation, unrecorded approvals, and lingering access from departed staff or third-party contractors. Compliance with this policy supports alignment of access controls with statutory requirements under the Protection of Personal Information Act (POPIA), contractual mandates under PCI-DSS v4.0.1, and technical safeguards defined in CIS Controls v8 (IG2) and NIST CSF 2.0 (PR.AA).

## 2. Scope
This policy applies to:

**Who:** All Bright Bean Coffee personnel (full-time and part-time staff across all 8 branches, head office, and Midrand depot), third-party operators and managed service providers (specifically Muza IT technicians and account managers), and external contractors. Physical site visitors and delivery personnel (such as J&T logistics) carry no logical system access and are governed under physical escort rules.

**What:** All 24 enterprise, cloud, database, network, and operational technology (OT) systems formally documented in **systems-inventory.md**, as well as all identity providers, service accounts, and data assets contained within them. Tier-based security controls (including multi-factor authentication, access review frequency, and approval workflows) strictly follow the tier assignments defined in **systems-tiering.md.**

**Where:** All physical locations owned or operated by Bright Bean Coffee—including the Cape Town head office (including the roastery, warehouse and canteen), Midrand distribution depot, and retail store branches—as well as any location where personnel work remotely or in the field.

## 3. Roles and Responsibilities

* **IT Manager (Darren):** Approves privileged access requests and their 12-month renewals, conducts monthly reviews of Global Admin accounts and Muza admin activity, acts as backup for Muza account removal, approves policy exceptions up to 90 days (requiring system owner sign-off for Tier 1 systems), and manages technical oversight of the Muza IT contract.
* **Systems Administrator (Aisha):** Executes standard and privileged provisioning tickets, enforces mandatory MFA configurations, acts as secondary backup for exit ticket processing, owns the 45-day inactivity disabling sweep, and executes same-day removal of Muza IT technician accounts upon notification.
* **IT Helpdesk (Hugo):** Logs and tracks all access control requests via Service Desk tickets, provisions standard user accounts, removes prior-role access on role-change tickets, serves as primary role responsible for disabling accounts on exit tickets, and maintains request approval records for three years.
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

  ### 4.2 Movers 

* **4.2.1 Notification and Ticket Submission:** When an employee or contractor changes job roles, transfers departments, or moves to a different branch, their new Line Manager or Branch Manager must submit a role-change access ticket via the IT Service Desk prior to or on the effective date of the change.
* **4.2.2 Same-Day Revocation of Prior Access:** Except as permitted under 4.2.4, all system access and permissions associated strictly with the individual's former role must be revoked by IT on the effective date of the role change. Old access entitlements must not be retained "just in case" or for convenience.
* **4.2.3 Provisioning New Role Entitlements:** Access for the new role must be provisioned strictly in accordance with the baseline defined in the role-to-access matrix and must satisfy the approval tiering requirements specified in Section 4.1.4.
* **4.2.4 Transition Exceptions:** If temporary access to former role systems is genuinely required for handover purposes, it must be requested and documented as a formal policy exception under Section 5 (Exceptions), capped at a maximum of 14 calendar days, and approved under Section 5 with the former System Owner’s agreement.

  ### 4.3 Leavers

* **4.3.1 Exit Notification and Ticket Raising:** HR must submit a formal exit ticket via the IT Service Desk on or before the employee's or contractor's last working day, or immediately upon notice for a dismissal. For a dismissal, HR must alert the IT Manager or IT Helpdesk before the individual is notified, so access can be revoked at that moment.
* **4.3.2 Same-Day Access Revocation:** All logical access across all enterprise systems, cloud platforms, and third-party portals (including the CartSmartz Seller Portal) must be revoked on the same day. For dismissals, revocation must occur immediately at the exact moment the individual is notified.
* **4.3.3 Account Disablement Protocol:** Departing personnel and contractor accounts must be disabled on the same day under 4.3.2. Accounts must be locked and disabled rather than deleted.
* **4.3.4 Comprehensive System Verification:** IT must compile the list of systems from the systems inventory and the individual’s directory account, not from the manager’s input alone. The IT Helpdesk and the E-Commerce Integration Specialist must verify and confirm that access has been terminated across all systems and third-party vendor platforms. The exit ticket must remain open until every system on the verified list is confirmed disabled.
* **4.3.5 Physical Asset Return and Checklist Sign-Off:** All physical keys, door cards, fobs, and equipment must be returned by the individual on their last working day and formally signed off using the joint HR and Facilities leaver checklist.
* **4.3.6 Branch POS Card and PIN Deactivation:** The Branch IT Technician (Keanu) must disable and deactivate the departing individual's POS physical login card and personal PIN on the same day as their exit.
* **4.3.7 Applicability to Contractors and Temporary Personnel:** The leaver revocation, asset return, and sign-off procedures apply equally to all full-time staff, part-time staff, temporary workers, consultants, and third-party contractor personnel ending their engagement with Bright Bean Coffee. Muza IT technician accounts follow Section 4.7.

 ### 4.4 Authentication (MFA and POS cards)

* **4.4.1 Mandatory MFA for Tier 1 and Tier 2 Systems:** Multi-factor authentication (MFA) must be enforced and enabled for all user accounts accessing Tier 1 and Tier 2 systems. 
* **4.4.2 Mandatory MFA for Administrative Accounts:** Multi-factor authentication (MFA) must be enforced for all administrative and privileged accounts across all tiers without exception.
* **4.4.3 Mandatory MFA for Remote Access:** MFA must be required for all remote access, including access to cloud applications from outside Bright Bean premises.
* **4.4.4 POS Card and PIN Authentication:** At retail point-of-sale (POS) terminals, authentication must consist of a physical card combined with a unique personal identification number (PIN), which together constitute mandatory multi-factor authentication for till access.
* **4.4.5 POS Card Issuance and Uniqueness:** POS physical login cards and personal PINs must be issued exclusively upon receipt of an approved Service Desk ticket. Each card and PIN must be unique to an individual staff member and must never be shared, pooled, or used by another person.
* **4.4.6 Individual Credential Accountability:** Except for service accounts governed by 4.4.7, every system account, user ID, and login credential must be assigned to a single, identifiable individual. Credential sharing, group accounts, or shared logins (including corporate banking credentials) are strictly prohibited.
* **4.4.7 Service Account Management:** Service accounts must have a named owner and must not be used for interactive logon unless approved as an exception under Section 5.
* **4.4.8 Default Credential Modification:** All vendor-supplied default passwords, factory-set usernames, and pre-configured administrative credentials on new systems, hardware devices, or software applications must be changed immediately upon installation and prior to going live in the production environment.

  ### 4.5 Privileged Access

* **4.5.1 Privileged Access Approval:** All requests for privileged or administrative access must be approved by the IT Manager (Darren). Privileged access requests for the IT Manager (Darren) must be approved by the Chief Operating Officer (COO).
* **4.5.2 Twelve-Month Privileged Expiry and Renewal:** All privileged access grants must expire after a maximum of 12 months. Continued privileged access requires formal re-approval under 4.5.1 before the expiry date.
* **4.5.3 Separate Administrative Accounts:** Administrators must use dedicated, separate administrative accounts for performing privileged tasks and must not use their standard day-to-day user accounts for administrative functions.
* **4.5.4 Separation of System Ownership and Administration:** To prevent conflict of interest and concentration of risk, the designated System Owner and the person administering the system must be distinct, separate individuals.
* **4.5.5 Named Privileged Accounts:** Except for service accounts governed by 4.4.7, all privileged and administrative accounts—including those utilized by Muza IT technicians—must be uniquely named and assigned to an individual user. Group accounts, generic admin logins, and shared privileged credentials are strictly prohibited.
* **4.5.6 Privileged Access Review Inclusion:** All privileged accounts and administrative entitlements must be subjected to access reviews as part of the scheduled quarterly system access reviews. Global Admin accounts are additionally reviewed monthly under 4.6.2.
* **4.5.7 Backup Administrator Assignment:** The IT Manager must ensure each Tier 1 system has a named backup administrator, so that no system depends on a single person.

### 4.6 Reviews and Inactivity

* **4.6.1 Comprehensive System Access Reviews:** System Owners must conduct comprehensive access reviews for all systems on a quarterly basis, verifying that all active user entitlements remain operationally necessary for their assigned job roles.
* **4.6.2 Monthly Global Admin and Muza Reviews:** The IT Manager (Darren) must conduct a monthly review of all Global Admin accounts and Muza IT administrative activity logs to detect anomalous or unauthorized privilege utilization.
* **4.6.3 Inactivity Disabling:** User accounts that remain inactive for a consecutive period of 45 days must be disabled by the Systems Administrator, not deleted. Accounts of staff on approved long leave may be retained under an exception in Section 5.
* **4.6.4 Inactivity Re-activation Protocol:** Re-activation of an account disabled due to 45-day inactivity must not occur automatically; it requires a formal Service Desk ticket submitted by the Line Manager and re-approved in accordance with Section 4.1.4.
* **4.6.5 Review Independence and Self-Review Prohibition:** A reviewer must not review their own access. The COO reviews the IT Manager’s access.
* **4.6.6 Review Remediation and Record Retention:** Any access found to be unnecessary during a review must be removed within 5 working days, and all review records must be retained for 3 years.
* **4.4.9 MFA Exceptions:** Any technical or operational deviation from mandatory MFA requirements cannot be bypassed or excused for convenience; it must be formally submitted, reviewed, and approved as a policy exception under Section 5. Administrative accounts covered by 4.4.2 cannot be granted an MFA exception.

  ### 4.7 Third Parties (Muza IT and Vendors)

* **4.7.1 Muza IT Engineer Departure Notice:** Muza IT must provide written notice to Bright Bean on the same day any Muza technician leaves their company or is reassigned away from the Bright Bean account. The IT Helpdesk must log this notice as an IT Service Desk ticket in accordance with Section 4.1.1.
* **4.7.2 Same-Day Muza Account Removal:** The Systems Administrator must remove or disable the departing or reassigned Muza technician's access on the same day the notice is received. The IT Manager (Darren) serves as the mandatory backup responsible for executing this removal if the Systems Administrator is unavailable.
* **4.7.3 Quarterly Muza Technician Roster:** Muza IT must provide a verified, written list of all active technicians with access to Bright Bean systems on a quarterly basis to the IT Manager for reconciliation against active enterprise accounts. Any account not matched to an active technician must be disabled the same day.
* **4.7.4 Muza Administrative Review Cross-Reference:** Monthly reviews of Muza IT administrative activity logs and account entitlements must be conducted in accordance with Section 4.6.2.
* **4.7.5 Muza Named Account Mandate:** All Muza IT administrative and technical accounts must comply with the individual naming and accountability requirements specified in Section 4.5.5. Shared vendor credentials are strictly prohibited.
* **4.7.6 Operator Agreement and POPIA Compliance:** The formal service agreement between Bright Bean Coffee and Muza IT must legally bind Muza to these access control obligations in accordance with POPIA Section 21 operator requirements.
* **4.7.7 Security Compromise Notification:** Muza IT must notify Bright Bean immediately of any suspected or actual security compromise affecting Bright Bean systems or data, including as required by POPIA s21(2) where personal information is involved. Notification to the Information Regulator under POPIA s22 is handled outside this policy.
* **4.7.8 General Third-Party and Contractor Access:** Any third-party vendor, external consultant, or contractor (other than Muza IT) requiring system access must be provisioned solely via an approved Service Desk ticket, and must have a predefined access end date that strictly matches their contract expiry date. Access requests follow Section 4.1.

### 4.8 Physical Access

* **4.8.1 Lost Key and Card Reporting:** Any lost physical key, access card, key fob, or retail point-of-sale (POS) login card must be reported by the staff member immediately, and no later than 4 hours after discovering the loss, to their Line Manager or Branch Manager. The manager must raise a Service Desk ticket immediately.
* **4.8.2 Immediate Deactivation of Lost Access Media:** Upon receiving the ticket, Facilities immediately disables door cards and fobs, and the Branch IT Technician disables lost POS cards. Lost physical keys are recorded by Facilities.
* **4.8.3 Visitor Escort and Logging:** All external visitors, contractors, and guests—including J&T delivery personnel—entering Bright Bean premises must be signed in, continuously escorted at all times while on-site, and logged upon departure.
* **4.8.4 Quarterly Physical Access Audit:** Facilities must conduct a quarterly reconciliation review comparing active access cards and keyholders against the current staff roster to ensure all departed or transferred personnel have had their physical access revoked. Any card or key not matched to current personnel must be disabled or recovered the same day.
* **4.8.5 Principle of Least Privilege for Physical Access:** Physical keys, access cards and electronic fobs must be provisioned only for the operational areas required for the individual’s job role.
* **4.8.6 Payment Terminal Physical Inspection:** All retail payment terminals and POS card readers must undergo quarterly physical and visual inspections by the Branch Manager to detect any signs of skimming devices, tampering, or unauthorized hardware modifications, with a record maintained of each inspection.
