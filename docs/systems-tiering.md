# Bright Bean Coffee — System Protection Tiers & Governance Standard

## 1. Purpose
This standard establishes a tiered framework for grouping Bright Bean Coffee's 24 systems into protection levels. By bucketing systems into Tiers 1 through 3 based on sensitivity and business operational impact, access control rules—such as access approval workflows, Multi-Factor Authentication (MFA) enforcement, and access review frequencies—can be applied consistently without maintaining 24 distinct policy sets.

## 2. Classification Levels
Data classification indicates the severity of impact or damage resulting from unauthorized access, leakage, or loss:

* **Public:** Information intended for public consumption. Leakage causes no operational or financial harm (e.g., website pricing, public marketing).
* **Internal:** Information restricted to staff. Leakage is embarrassing or inconvenient but causes no direct operational, legal, or financial harm.
* **Confidential:** Sensitive business information. Leakage causes real financial, commercial, or operational damage (e.g., proprietary roast recipes, financial margins, trade logistics).
* **Restricted:** Highly sensitive data protected by law or regulatory standards. Leakage causes severe legal, regulatory, or financial damage (e.g., POPIA Personal Information, biometric templates, cardholder data, system credentials, bank account numbers).

## 3. Criticality Levels
Criticality measures operational impact and how rapidly business operations degrade if a system becomes unavailable:

* **High:** Core operations halt or major financial loss occurs within hours of system failure (e.g., primary identity provider, coffee roasting machinery, live payment terminals).
* **Medium:** Significant operational disruption occurs, but manual workarounds exist to sustain short-term operations.
* **Low:** Inconvenient or minor disruption only; workarounds easily sustain normal operations.

## 4. Tier Assignment Rule
Baseline system tiers are determined automatically by combining the **Classification** and **Criticality** assigned in the *Full Systems Inventory & Governance Matrix*:

| Tier Level | Name | Trigger Rule |
| :--- | :--- | :--- |
| **Tier 1** | Critical | **Restricted** classification AND **High** criticality |
| **Tier 2** | Important | **Restricted** classification (Medium/Low criticality) OR **Confidential** classification (High criticality) |
| **Tier 3** | Standard | All other combinations |

## 5. Overrides
To address systemic supply chain vulnerabilities and immediate financial cash-out risks, up to three systems may be overridden upward from their rule-based tier:

1. **Corporate Internet Banking:** Raised from Tier 2 to **Tier 1** because unauthorized access allows immediate and irreversible financial cash out.
2. **Endpoint Detection & Response (EDR):** Raised from Tier 3 to **Tier 2** because compromising core security monitoring compromises all endpoints simultaneously.
3. **Remote Monitoring & Management (RMM):** Raised from Tier 3 to **Tier 2** because central management execution power allows rapid, silent takeover of all endpoints.

## 6. System Tiers Table

| System | Tier |
| :--- | :--- |
| **Microsoft Entra ID** | Tier 1 |
| **Microsoft 365** | Tier 1 |
| **Windows Workstations** | Tier 2 |
| **Endpoint Detection & Response (EDR)** | Tier 2 |
| **Mobile POS** | Tier 2 |
| **Card Payment Terminals (EFTPOS)** | Tier 1 |
| **CartSmartz Seller Portal** | Tier 2 |
| **CartSmartz Sync API** | Tier 2 |
| **Central Inventory & ERP Database** | Tier 2 |
| **Warehouse & Dispatch System** | Tier 2 |
| **Export Documentation Portal** | Tier 3 |
| **Cloud Accounting Software** | Tier 2 |
| **Payroll & HR Portal** | Tier 2 |
| **Corporate Internet Banking** | Tier 1 |
| **Enterprise Password Manager** | Tier 1 |
| **IT Service Desk** | Tier 3 |
| **Network & Firewall Infrastructure** | Tier 1 |
| **Remote Monitoring & Management (RMM)** | Tier 2 |
| **Secure VPN Gateway** | Tier 2 |
| **Microsoft Azure Cloud Platform** | Tier 1 |
| **Roastery Control Software** | Tier 2 |
| **Automated Packaging Line PLC** | Tier 3 |
| **Physical Access Control & CCTV** | Tier 2 |
| **Vehicle Fleet Tracking System** | Tier 3 |

## 7. Reference
* **Primary Inventory:** `docs/systems-inventory.md` (Master copy for system owners, administrators, data held, classification, and criticality labels).
