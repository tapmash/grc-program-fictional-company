# BRIGHT BEAN COFFEE — OVERVIEW

> *Notice: All content, company details, employee names, and operational structures in this document are entirely fictional and designed solely for educational and training purposes.*

## Company Summary

Bright Bean Coffee is a South African high-end coffee manufacturer, distributor, and retailer with an 81-person workforce. Operations include bean roasting, national retail, on-site catering, and international export.

## Locations & Site Operations

* **Cape Town Head Office:** The main corporate and operational facility housing Executive Offices, Finance, HR, IT, Sales, the central Master Roaster, QA Lab, primary Distribution Warehouse, and the Head Office Canteen (open to staff and public).

* **Retail Branches (8 Locations):** Local retail and espresso operations serving customers in major urban centers:
  * *Greater Cape Town Area (3):* V&A Waterfront, Century City, Claremont
  * *Johannesburg (2):* Rosebank, Sandton
  * *Durban (2):* Umhlanga, Florida Road
  * *Port Elizabeth / Gqeberha (1):* Boardwalk

* **Gauteng Logistics Hub (Midrand Depot):** A specialized cross-docking bay receiving bulk shipments from Cape Town and staging local distribution for Johannesburg branches, corporate accounts, and regional stockists.

* **Export Markets:** USA, France, Dubai

* **E-Commerce Partner:** CartSmartz Platform (integrated via API)

## Headcount Breakdown (81 Total)

| Department | Headcount | Key Focus & Roles |
| :--- | :---: | :--- |
| **Executive** | 3 | Jeff (CEO/Owner), COO (Sipho Khumalo), Executive Assistant |
| **Finance** | 5 | Olwen (Sr. Accountant), Accounts Payable, Accounts Receivable & CartSmartz Reconciliation, Financial Analyst, Payroll |
| **Human Resources** | 4 | HR Manager (Thandiwe Ncube), L&D Officer, Talent Acquisition, HR Admin |
| **IT Department** | 5 | Darren (IT Manager), Hugo (Helpdesk), Systems Admin, Branch Tech, E-Com Specialist |
| **Production** | 12 | Kobus Meyer (Master Roaster), Steven Arendse (Floor Supervisor), Assistant Roaster, Packaging Supervisor, QA, Maintenance |
| **Warehouse & Logistics** | 10 | Coleen (Primary Driver), Warehouse Manager, International Dispatch, Forklift Operators, Fleet Drivers (Cape Town & Joburg) |
| **Sales & Export** | 8 | Head of International Sales, Key Accounts, CartSmartz Coordinator, Regional Reps (Gauteng & KZN), Corporate Accounts |
| **Facilities** | 4 | Julie (Sr. Cleaner), Maintenance Lead, Hygiene Cleaner, Security Supervisor |
| **Canteen & Operations Overhead** | 6 | Kayal (Barista), Canteen Supervisor, Kitchen Assistant, Canteen Cleaner, Regional Branch Ops Manager, National Trainer |
| **Retail Branches** | 24 | 8 Branches (3 Staff per Branch: Manager/Supervisor, Senior Barista, Barista/Cashier) |
| **Total Headcount** | **81** | |

## Remote and Field Work

* **Internal IT Helpdesk (Hugo):** Operates under a hybrid arrangement (2 days per week remote, 3 days on-site).
* **Head of International Sales:** Fully mobile / remote, traveling frequently to export markets in the USA, France, and Dubai.
* **Regional Sales Representatives (Gauteng & KZN):** 100% field-based, traveling to commercial client sites, retail stockists, and regional partners.
* **Regional Branch Operations Manager & National Training Barista:** Hybrid field roles, spending 2–3 days per week visiting and auditing the 8 national branches.
* **Key Accounts & Corporate Sales Managers:** Hybrid field roles, spending 2–3 days per week meeting with commercial buyers and office clients.
* **Logistics & Delivery Drivers:** Field-based during daily regional delivery runs.

## IT Architecture & Access Control Authority

* **In-House IT (Darren's Team):** Manages end-user tickets, hardware setups, local branch POS PINs, standard employee account creation (Microsoft 365, internal folders), and CartSmartz API data sync.
* **Muza IT (MSP):** External service provider holding Global Administrator rights. Manages core cloud infrastructure, firewalls, network security, server hosting, and backups.
* **Privileged Access Governance:** Darren (IT Manager) retains explicit authority for approving all privileged or elevated access requests across internal systems and cloud infrastructure. Revocation of privileged access or MSP accounts is performed by Darren or delegated internally to Systems Administration staff upon approval.

## Current State of Access Management

Bright Bean Coffee currently lacks a formal written access control policy. Access requests are handled informally via email or messaging to IT, and new user permissions are typically provisioned by copying from existing employees. When employees transfer or take on new roles, legacy access is rarely revoked, resulting in permission creep. Additionally, third-party platform access (such as the CartSmartz seller portal) is sometimes overlooked during employee offboarding.

## Third-Party Vendors & Dependencies

1. **Muza IT (MSP):** Core network, cloud tenant, firewall administration, and cloud infrastructure management.
2. **J&T Confectionaries:** Canteen food supplier (twice-weekly escorted physical deliveries; no IT access).
3. **CartSmartz:** National online retail marketplace integrated via custom APIs.
