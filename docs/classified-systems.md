# Bright Bean Coffee 
## Systems Inventory & Governance Matrix

### 1. Microsoft Entra ID
* **What it does:** Central identity directory managing user accounts, authentication passwords, MFA, and SSO policies
* **Main users:** Executive, Finance, HR, IT, Sales, Facilities Maintenance Lead, Master Roaster, Production Floor Supervisor, Packaging Line Supervisor, Warehouse Manager, Branch Managers
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
* **Main users:** Senior Baristas, Baristas / Cashiers, Canteen Supervisor
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
* **What it does:** Barcode scanning and shipping label generation software for local
