# Bright Bean Coffee 
## Systems Inventory & Classification Matrix

### 1. Microsoft Entra ID
* **What it does:** Central identity directory managing user accounts, authentication passwords, MFA, and SSO policies
* **Main users:** Executive, Finance, HR, IT, Sales, Facilities Maintenance Lead, Master Roaster, Production Floor Supervisor, Packaging Line Supervisor, Warehouse Manager
* **System Owner:** IT Manager
* **Administrator(s):** Systems Administrator, Internal IT Helpdesk, Muza IT
* **Data Held:** Password hashes, MFA tokens, domain credentials, user identities
* **Classification:** Restricted
* **Criticality:** High

---

### 2. Microsoft 365
* **What it does:** Enterprise email, team collaboration, file storage, intranet, and office productivity software
* **Main users:** Executive, Finance, HR, IT, Sales, Facilities Maintenance Lead, Production Floor Supervisor, Warehouse Manager, Branch Managers
* **System Owner:** IT Manager
* **Administrator(s):** Internal IT Helpdesk, Systems Administrator, Muza IT
* **Data Held:** Executive email, contracts, HR files, financial spreadsheets containing personal information
* **Classification:** Restricted
* **Criticality:** High

---

### 3. Windows Workstations
* **What it does:** Local operating system running on company laptops and desktop PCs for daily business tasks and local software access
* **Main users:** Executive, Finance, HR, IT, Sales, Facilities Maintenance Lead, Warehouse Manager, Branch Managers
* **System Owner:** IT Manager
* **Administrator(s):** Internal IT Helpdesk, Systems Administrator, Muza IT
* **Data Held:** Cached domain credentials, local authentication tokens, localized HR and financial working files
* **Classification:** Restricted
* **Criticality:** Medium

---

### 4. Endpoint Detection & Response (EDR)
* **What it does:** Endpoint security agent installed on laptops and servers to detect, isolate, and respond to malware threats
* **Main users:** All workstation and server end-users monitored by IT and MSP
* **System Owner:** IT Manager
* **Administrator(s):** Muza IT, Systems Administrator
* **Data Held:** Security telemetry, device event logs, process execution trees
* **Classification:** Internal
* **Criticality:** Medium

---

### 5. Mobile POS
* **What it does:** Tablet and terminal till application used for customer checkout, order entry, and daily sales logging
* **Main users:** Regional Branch Operations Manager, Branch Managers, Branch Supervisors, Senior Baristas, Baristas / Cashiers, Canteen Supervisor
* **System Owner:** Regional Branch Operations Manager
* **Administrator(s):** IT Support Technician - Branch Hardware & Networks, Systems Administrator
* **Data Held:** Daily store sales logs, retail orders, live till transaction data
* **Classification:** Confidential
* **Criticality:** High

---

### 6. Card Payment Terminals (EFTPOS)
* **What it does:** Standalone and integrated payment card readers processing credit and debit card transactions at checkout points
* **Main users:** Baristas / Cashiers, Canteen Supervisor, Branch Staff
* **System Owner:** Senior Accountant
* **Administrator(s):** Acquiring Merchant Bank
* **Data Held:** Payment card PANs, EMV chip transaction data, authorization tokens
* **Classification:** Restricted
* **Criticality:** High

---

### 7. CartSmartz Seller Portal
* **What it does:** Web portal provided by CartSmartz for managing online store product listings, pricing updates, seller dashboards, payout reconciliations, and order overrides
* **Main users:** Head of International Sales, Key Accounts Manager, E-Commerce Sales Coordinator, Accounts Receivable & CartSmartz Reconciliation Specialist
* **System Owner:** Head of International Sales
* **Administrator(s):** E-Commerce Integration Specialist, Systems Administrator
* **Data Held:** Customer shipping addresses, contact numbers, e-commerce order histories
* **Classification:** Restricted
* **Criticality:** Medium

---

### 8. CartSmartz Sync API
* **What it does:** Custom automated integration script syncing stock levels and incoming online sales orders between CartSmartz and central database
* **Main users:** Automated System Service
* **System Owner:** Chief Operating Officer
* **Administrator(s):** E-Commerce Integration Specialist, Systems Administrator
* **Data Held:** API secret keys, order sync logs, system authentication payload streams
* **Classification:** Restricted
* **Criticality:** Medium

---

### 9. Central Inventory & ERP Database
* **What it does:** Core relational database tracking green coffee bean stock, finished product batches, warehouse levels, and branch allocations
* **Main users:** Master Roaster, Production Floor Supervisor, Packaging Line Supervisor, Warehouse Manager, Systems Administrator
* **System Owner:** Chief Operating Officer
* **Administrator(s):** Systems Administrator
* **Data Held:** Proprietary roast blend recipes, inventory stock volumes, batch cost data
* **Classification:** Confidential
* **Criticality:** High

---

### 10. Warehouse & Dispatch System
* **What it does:** Barcode scanning and shipping label generation software for local courier dispatch and regional distribution tracking
* **Main users:** Warehouse Manager, International Dispatch Clerk, Receiving & Inbound Goods Clerk, Logistics Drivers
* **System Owner:** Warehouse Manager
* **Administrator(s):** Internal IT Helpdesk, Systems Administrator
* **Data Held:** Delivery recipient names, personal street addresses, dispatch tracking details
* **Classification:** Restricted
* **Criticality:** Medium

---

### 11. Export Documentation Portal
* **What it does:** Specialized web service used to generate, log, and submit international shipping manifests, bills of lading, and export compliance documents
* **Main users:** Head of International Sales, Export Documentation Clerk, International Dispatch Clerk
* **System Owner:** Head of International Sales
* **Administrator(s):** Systems Administrator
* **Data Held:** Commercial invoices, customs tariff declarations, international client trade data
* **Classification:** Confidential
* **Criticality:** Medium

---

### 12. Cloud Accounting Software
* **What it does:** Core financial accounting platform handling general ledger, invoicing, accounts payable/receivable, bank reconciliations, and financial reporting
* **Main users:** Chief Executive Officer, Chief Operating Officer, Senior Accountant, Accounts Payable Officer, Accounts Receivable & CartSmartz Reconciliation Specialist, Financial Analyst
* **System Owner:** Chief Executive Officer
* **Administrator(s):** IT Manager, Systems Administrator
* **Data Held:** General ledger records, supplier bank account details, customer tax invoices
* **Classification:** Restricted
* **Criticality:** Medium

---

### 13. Payroll & HR Portal
* **What it does:** Cloud platform managing employee salaries, tax deductions, leave requests, employee records, and payslip distribution
* **Main users:** Chief Executive Officer, Chief Operating Officer, HR Manager, Learning & Development Officer, Talent Acquisition Specialist, Payroll Administrator, All Staff
* **System Owner:** HR Manager
* **Administrator(s):** Systems Administrator, IT Manager
* **Data Held:** Employee SA ID numbers, tax numbers, personal bank details, salary structures
* **Classification:** Restricted
* **Criticality:** Medium

---

### 14. Corporate Internet Banking
* **What it does:** Online commercial banking portal for processing inward foreign payments, batch EFT supplier payouts, and branch cash drop reconciliations
* **Main users:** Chief Executive Officer, Chief Operating Officer, Senior Accountant, Accounts Payable Officer
* **System Owner:** Chief Executive Officer
* **Administrator(s):** IT Manager
* **Data Held:** Company bank balances, outgoing EFT payment batches, commercial statements
* **Classification:** Restricted
* **Criticality:** Medium

---

### 15. Enterprise Password Manager
* **What it does:** Centralized encrypted password vault for securely storing, sharing, and auditing corporate credentials and vendor portal logins
* **Main users:** Executive, Finance, HR, IT, Sales, Branch Managers
* **System Owner:** IT Manager
* **Administrator(s):** Systems Administrator, Muza IT
* **Data Held:** Master vault keys, shared administrative credentials, vendor portal logins
* **Classification:** Restricted
* **Criticality:** High

---

### 16. IT Service Desk
* **What it does:** Standardized ticketing platform for submitting, tracking, and approving IT access requests, equipment issues, and JML onboarding tickets
* **Main users:** All Staff, Internal IT Team, Muza IT
* **System Owner:** IT Manager
* **Administrator(s):** Internal IT Helpdesk, Systems Administrator, Muza IT
* **Data Held:** IT support tickets, user access requests, hardware asset assignment logs
* **Classification:** Internal
* **Criticality:** Medium

---

### 17. Network & Firewall Infrastructure
* **What it does:** Physical and virtual firewalls, core switches, and managed Wi-Fi access points securing corporate and branch network traffic
* **Main users:** Internal IT Team, Muza IT
* **System Owner:** IT Manager
* **Administrator(s):** Muza IT, IT Support Technician - Branch Hardware & Networks, Systems Administrator
* **Data Held:** Firewall rules, Wi-Fi PSKs, network routing tables, admin credentials
* **Classification:** Restricted
* **Criticality:** High

---

### 18. Remote Monitoring & Management (RMM)
* **What it does:** Endpoint management tool used by the MSP to deploy software patches, track hardware health, and run background management scripts
* **Main users:** Muza IT, Internal IT Team
* **System Owner:** IT Manager
* **Administrator(s):** Muza IT
* **Data Held:** Endpoint health status, software patch levels, remote execution script logs
* **Classification:** Internal
* **Criticality:** Medium

---

### 19. Secure VPN Gateway
* **What it does:** Encrypted tunnel allowing remote and field staff to connect securely to internal network resources, files, and central databases
* **Main users:** Internal IT Helpdesk, Head of International Sales, Regional Sales Representatives, Key Accounts Manager, Corporate Office Accounts Manager, Regional Branch Operations Manager, National Training Barista & Quality Auditor, Muza IT
* **System Owner:** IT Manager
* **Administrator(s):** Muza IT, Systems Administrator
* **Data Held:** Active VPN session tokens, tunnel traffic logs, user authentication keys
* **Classification:** Restricted
* **Criticality:** Medium

---

### 20. Microsoft Azure Cloud Platform
* **What it does:** Cloud infrastructure host running virtual machines, central SQL database servers, storage buckets, and daily automated cloud backups
* **Main users:** Internal IT Team, Muza IT
* **System Owner:** IT Manager
* **Administrator(s):** Muza IT, Systems Administrator
* **Data Held:** Encrypted database backups, server image snapshots, cloud storage archives
* **Classification:** Restricted
* **Criticality:** High

---

### 21. Roastery Control Software
* **What it does:** Specialized machine control interface connected to industrial coffee roasters for managing roast profiles, thermal curves, and batch logs
* **Main users:** Master Roaster, Production Floor Supervisor, Assistant Roaster
* **System Owner:** Master Roaster
* **Administrator(s):** Systems Administrator
* **Data Held:** Roast thermal profiles, drum speed configurations, roast profile recipes
* **Classification:** Confidential
* **Criticality:** High

---

### 22. Automated Packaging Line PLC
* **What it does:** Touchscreen interface on the packaging line for weight calibration, pouch sealing, and date stamping
* **Main users:** Production Floor Supervisor, Packaging Line Supervisor, Packaging Machine Specialist
* **System Owner:** Production Floor Supervisor
* **Administrator(s):** Systems Administrator
* **Data Held:** Packaging line speed parameters, pouch weight logs, batch date codes
* **Classification:** Internal
* **Criticality:** Low

---

### 23. Physical Access Control & CCTV
* **What it does:** Keycard or fob door readers, biometric scanners, and IP security cameras for building security, loading dock monitoring, and restricted site areas
* **Main users:** Head Office Staff, Facilities Maintenance Lead, Senior Cleaner, Grounds & Security Supervisor, Logistics Drivers, Warehouse Manager
* **System Owner:** Facilities Maintenance Lead
* **Administrator(s):** Systems Administrator
* **Data Held:** Biometric templates, electronic door access logs, CCTV video archives
* **Classification:** Restricted
* **Criticality:** Medium

---

### 24. Vehicle Fleet Tracking System
* **What it does:** Telematics GPS portal for monitoring real-time locations, fuel efficiency, driver security, and delivery routes of transport vehicles
* **Main users:** Warehouse Manager, Primary Logistics Driver, Local Fleet Drivers, Gauteng Hub Driver
* **System Owner:** Warehouse Manager
* **Administrator(s):** Systems Administrator
* **Data Held:** Real-time vehicle GPS coordinates, delivery routes, driver speed telemetry
* **Classification:** Internal
* **Criticality:** Low
