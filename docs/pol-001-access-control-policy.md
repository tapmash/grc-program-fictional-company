# POL-001 Access Control Policy

## 1. Purpose
This policy establishes the rules governing access to Bright Bean Coffee’s systems, data, and physical premises. It protects enterprise assets against unauthorized access, creeping privilege accumulation, unrecorded approvals, and lingering access from departed staff or third-party contractors. Compliance with this policy supports alignment of access controls with statutory requirements under the Protection of Personal Information Act (POPIA), contractual mandates under PCI-DSS v4.0.1, and technical safeguards defined in CIS Controls v8 (IG2) and NIST CSF 2.0 (PR.AA).

## 2. Scope

This policy applies to all Bright Bean Coffee personnel, including full-time and part-time staff across the head office, branches, and distribution depot, as well as third-party operators, managed service providers, and external contractors who have access to Bright Bean systems, data, or premises. It applies to all enterprise, cloud, database, network, and operational technology systems documented in the systems inventory, and to all identity providers, service accounts, and data assets within them, with tier-based requirements following the tier assignments in the systems tiering standard. It applies at all physical locations owned or operated by Bright Bean Coffee and at any location where personnel work remotely or in the field. Visitors and delivery personnel have no logical system access and are governed by the physical escort rules in Section 4.8. Where a requirement of this policy is not technically supported by a system, the system must use the strongest available control, and the deviation must be documented and approved as an exception under Section 5.

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

* **4.1.1 Mandatory Request Channel:** All requests for new access, access modifications, or entitlement changes must be submitted through the formal IT Service Desk ticketing platform. Requests made verbally, by email, or by instant message must not be acted on by IT personnel. Written notices from Muza IT under Section 4.7 must be logged as a ticket by the IT Helpdesk before action is taken.
* **4.1.2 Ticket Authoring:** Access request tickets must be raised by the requester's Line Manager, Branch Manager, or HR (for exit tickets). Personnel must not raise access request tickets for their own accounts.
* **4.1.3 Role-Based Provisioning:** Access must be provisioned based on the role-to-access matrix and documented operational necessity. IT personnel must not copy access permissions from another employee or colleague.
* **4.1.4 Approval Tiering:** Access requests must be approved by the requester's Line Manager or Branch Manager. Access to systems in higher tiers, as classified in `systems-tiering.md`, additionally requires approval by the System Owner, as defined in the Access Control Standard. Privileged access additionally follows Section 4.5.
* **4.1.5 Prohibition of Self-Approval:** Personnel must not approve their own access requests, privilege changes, or policy exceptions. Access requests for the IT Manager must be approved by the Chief Operating Officer (COO), who also provides the System Owner approval where the IT Manager owns the system.
* **4.1.6 Audit Record Retention:** The IT Helpdesk must retain complete records of access request tickets, including approvals, timestamps, and fulfilment, for the period set in the Access Control Standard.

### 4.2 Movers (Role Changes)

* **4.2.1 Notification and Ticket Submission:** When a person changes job role, department, or branch, their new Line Manager or Branch Manager must submit a role-change access ticket via the IT Service Desk before or on the effective date of the change.
* **4.2.2 Revocation of Prior Access:** Except as permitted under 4.2.4, access associated with a person's former role must be removed when the role change takes effect. Old access must not be retained "just in case" or for convenience.
* **4.2.3 Provisioning New Role Entitlements:** Access for the new role must be provisioned in line with the role-to-access matrix and the approval requirements in Section 4.1.4.
* **4.2.4 Transition Exceptions:** Temporary access to former-role systems for handover must be requested and approved as an exception under Section 5, with the former System Owner's agreement, and for no longer than the maximum set in the Access Control Standard.

### 4.3 Leavers

* **4.3.1 Exit Notification and Ticket Raising:** HR must submit an exit ticket via the IT Service Desk on or before the person's last working day, or immediately on notice for a dismissal. For a dismissal, HR must alert the IT Manager or IT Helpdesk before the individual is notified, so access can be revoked at that moment.
* **4.3.2 Prompt Access Revocation:** All logical access across enterprise systems, cloud platforms, and third-party portals (including the CartSmartz Seller Portal) must be revoked promptly, within the timeframe set in the Access Control Standard. For dismissals, revocation must occur at the moment the individual is notified.
* **4.3.3 Account Disablement:** Leaver accounts must be disabled in line with 4.3.2. Accounts must be disabled rather than deleted.
* **4.3.4 System Verification:** IT must compile the list of systems from the systems inventory and the individual's directory account, not from the manager's input alone. The IT Helpdesk and the E-Commerce Integration Specialist must verify that access has been terminated across all systems and third-party platforms. The exit ticket must remain open until every system on the verified list is confirmed disabled.
* **4.3.5 Physical Asset Return and Checklist Sign-Off:** All physical keys, door cards, fobs, and equipment must be returned on the person's last working day and signed off on the joint HR and Facilities leaver checklist.
* **4.3.6 Branch POS Card and PIN Deactivation:** The Branch IT Technician must disable the departing individual's POS login card and PIN within the timeframe set in 4.3.2.
* **4.3.7 Applicability to Contractors and Temporary Personnel:** The leaver revocation, asset return, and sign-off requirements apply equally to full-time staff, part-time staff, temporary workers, consultants, and third-party contractor personnel ending their engagement with Bright Bean Coffee. Muza IT technician accounts follow Section 4.7.

### 4.4 Authentication

* **4.4.1 Authentication Requirements:** Access to Bright Bean Coffee systems must be protected by authentication that is appropriate to the risk of the system and the account. The IT Manager must define, maintain, and communicate the specific authentication requirements in the Access Control Standard.
* **4.4.2 Multi-Factor Authentication:** Multi-factor authentication must be used for privileged accounts, remote access, and systems of higher risk, as specified in the Access Control Standard.
* **4.4.3 Point-of-Sale Authentication:** Access to point-of-sale terminals must use authentication that is unique to each individual and meets the requirements of the Access Control Standard.
* **4.4.4 Individual Accountability:** Except for service accounts governed by 4.4.7, every account and credential must be assigned to one identifiable individual and must not be shared.
* **4.4.5 Default Credentials:** Vendor-supplied default credentials must be changed before a system or device is put into use.
* **4.4.6 Authentication Exceptions:** Exceptions to authentication requirements must follow Section 5. Exceptions must not be granted for privileged accounts.
* **4.4.7 Service Accounts:** Service accounts must have a named owner and must not be used for interactive logon unless approved as an exception under Section 5.

### 4.5 Privileged Access

* **4.5.1 Privileged Access Approval:** All requests for privileged or administrative access must be approved by the IT Manager. Privileged access requests for the IT Manager must be approved by the COO.
* **4.5.2 Privileged Access Expiry and Renewal:** All privileged access grants must expire after the maximum period set in the Access Control Standard. Continued privileged access requires re-approval under 4.5.1 before the expiry date.
* **4.5.3 Separate Administrative Accounts:** Administrators must use dedicated, separate administrative accounts for privileged tasks and must not use their standard day-to-day user accounts for administrative functions.
* **4.5.4 Separation of System Ownership and Administration:** To prevent conflict of interest and concentration of risk, the System Owner and the person administering the system must be different individuals.
* **4.5.5 Named Privileged Accounts:** Except for service accounts governed by 4.4.7, all privileged and administrative accounts, including those used by Muza IT technicians, must be uniquely named and assigned to an individual. Group accounts, generic admin logins, and shared privileged credentials are prohibited.
* **4.5.6 Privileged Access Review Inclusion:** All privileged accounts and administrative entitlements must be included in the scheduled access reviews. Global Admin accounts are additionally reviewed under Section 4.6.2.
* **4.5.7 Backup Administrator Assignment:** The IT Manager must ensure each Tier 1 system has a named backup administrator, so that no system depends on a single person.

### 4.6 Reviews and Inactivity

* **4.6.1 System Access Reviews:** System Owners must review access for all their systems at the frequency set in the Access Control Standard, verifying that active user entitlements remain necessary for assigned job roles.
* **4.6.2 Global Admin and Muza Reviews:** The IT Manager must review all Global Admin accounts and Muza IT administrative activity at the frequency set in the Access Control Standard, to detect anomalous or unauthorized use of privilege.
* **4.6.3 Inactivity Disabling:** Accounts that remain inactive beyond the period set in the Access Control Standard must be disabled by the Systems Administrator, not deleted. Accounts of staff on approved long leave may be retained under an exception in Section 5.
* **4.6.4 Inactivity Re-activation:** An account disabled for inactivity must not be re-activated automatically. Re-activation requires a Service Desk ticket from the Line Manager and re-approval under Section 4.1.4.
* **4.6.5 Review Independence:** A reviewer must not review their own access. The COO reviews the IT Manager's access.
* **4.6.6 Review Remediation and Records:** Access found to be unnecessary during a review must be removed within the timeframe set in the Access Control Standard. Review records must be retained for the period set in the Access Control Standard.

### 4.7 Third Parties (Muza IT and Vendors)

* **4.7.1 Muza IT Departure Notice:** Muza IT must give Bright Bean written notice, within the timeframe set in the Access Control Standard, when a Muza technician leaves or is reassigned away from the Bright Bean account. The IT Helpdesk must log this notice as a Service Desk ticket in accordance with Section 4.1.1.
* **4.7.2 Muza Account Removal:** The Systems Administrator must remove or disable the departing or reassigned technician's access promptly after the notice is received, within the timeframe set in the Access Control Standard. The IT Manager is the backup if the Systems Administrator is unavailable.
* **4.7.3 Muza Technician Roster:** Muza IT must give the IT Manager a verified, written list of all active technicians with access to Bright Bean systems at the frequency set in the Access Control Standard, for reconciliation against active accounts. Any account not matched to an active technician must be disabled promptly.
* **4.7.4 Muza Administrative Review Cross-Reference:** Reviews of Muza IT administrative activity and account entitlements must be conducted in accordance with Section 4.6.2.
* **4.7.5 Muza Named Accounts:** All Muza IT administrative and technical accounts must comply with the individual naming and accountability requirements in Section 4.5.5. Shared vendor credentials are prohibited.
* **4.7.6 Operator Agreement and POPIA Compliance:** The service agreement between Bright Bean Coffee and Muza IT must bind Muza to these access control obligations, in line with POPIA Section 21 operator requirements.
* **4.7.7 Security Compromise Notification:** Muza IT must notify Bright Bean immediately of any suspected or actual security compromise affecting Bright Bean systems or data, including as required by POPIA s21(2) where personal information is involved. Notification to the Information Regulator under POPIA s22 is handled outside this policy.
* **4.7.8 General Third-Party and Contractor Access:** Any third-party vendor, external consultant, or contractor (other than Muza IT) requiring system access must be provisioned through an approved Service Desk ticket and must have a defined access end date that matches the contract expiry date. Access requests follow Section 4.1.

### 4.8 Physical Access

* **4.8.1 Lost Key and Card Reporting:** Any lost physical key, access card, key fob, or POS login card must be reported to the person's Line Manager or Branch Manager promptly, within the timeframe set in the Access Control Standard. The manager must raise a Service Desk ticket immediately.
* **4.8.2 Deactivation of Lost Access Media:** On receiving the ticket, Facilities must disable lost door cards and fobs, and the Branch IT Technician must disable lost POS cards. Lost physical keys must be recorded by Facilities.
* **4.8.3 Visitor Escort and Logging:** All external visitors, contractors, and guests, including J&T delivery personnel, entering Bright Bean premises must be signed in, escorted at all times while on site, and logged.
* **4.8.4 Physical Access Reconciliation:** Facilities must compare active access cards and keyholders against the current staff roster at the frequency set in the Access Control Standard. Any card or key not matched to current personnel must be disabled or recovered promptly.
* **4.8.5 Least Privilege for Physical Access:** Physical keys, access cards, and electronic fobs must be provisioned only for the operational areas required for the individual's job role.
* **4.8.6 Payment Terminal Inspection:** Retail payment terminals and POS card readers must be physically inspected by the Branch Manager at the frequency set in the Access Control Standard, to detect skimming devices, tampering, or unauthorized hardware changes. A record of each inspection must be kept.

