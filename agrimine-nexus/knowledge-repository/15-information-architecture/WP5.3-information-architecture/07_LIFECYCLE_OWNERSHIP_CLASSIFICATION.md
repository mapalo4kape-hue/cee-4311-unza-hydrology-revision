---
id: WP5.3-LIFECYCLE
title: Information Lifecycle, Ownership & Classification Registers (WP5.3)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 5 — Enterprise Information & Data Architecture
work_package: WP5.3
industry: cross-industry
topic: Information lifecycle, ownership, classification
keywords: [lifecycle, ownership, stewardship, classification, information-architecture]
summary: Outputs 5-7. Information Lifecycle Catalogue, Master Data Ownership Register, and Data Classification Register. Business information level only.
source: F-0053;F-0073;F-0077;F-0079;F-0086
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 68
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_ENTERPRISE_INFORMATION_CATALOGUE.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Information Lifecycle, Ownership & Classification (Outputs 5–7)

## Output 5 — Information Lifecycle Catalogue
Lifecycle stages applied to information objects: **Creation → Validation → Approval → Use → Sharing → Archive → Retention → Deletion.**
| Information group | Creation | Validation | Approval | Use | Sharing | Archive/Retention | Deletion |
|-------------------|----------|-----------|----------|-----|---------|-------------------|----------|
| Farmer/identity (INFO-001/040) | At registration | Identity checks | Steward | Advisory/finance | Consent-based | Per-DPA | On lawful request/expiry |
| Land/crop/harvest (INFO-002/003/006) | Field capture | Agronomy review | — | Planning/yield | With cooperative/buyer | Season+3–7y | After retention |
| Financial (INFO-014/016/042) | Transaction | Reconciliation | Finance approver | Accounting/tax | Regulator/auditor | 7y-statutory | After statutory period |
| Warehouse receipt (INFO-010) | On deposit | Stock verification | WRS operator | Trade/finance | Financier/buyer | Statutory+7y | After redemption+retention |
| Mining (INFO-018/020/021) | Survey/production | Geology/QA | Mine engineer | Planning/reporting | Regulator | Life-of-mine | Post-closure per law |
| Environmental (INFO-024/025) | Monitoring/lab | Validation vs limits | Env steward | Compliance | ZEMA | Statutory | After statutory period |
| Permit/compliance (INFO-027/028) | Application/period | Completeness check | Regulator/officer | Right-to-operate/report | Regulator | Life-of-licence+7y | After retention |
| Construction (INFO-031/033/034) | Project/site | QS/QA | PM/QS | Delivery/payment | Client/consultant | Life-of-project+7y | After retention |
| Logistics (INFO-035/036/037) | Order/dispatch | Delivery confirm | — | Fulfilment | Customer/customs | 7y | After retention |
| Audit/consent (INFO-043/044) | On action/consent | — | — | Accountability | Auditor/regulator | Per-policy/DPA | Append-only; per policy |

## Output 6 — Master Data Ownership Register
| Information object | Business Owner (domain) | Custodian | Steward | Producer | Consumer | Regulator | Auditor |
|--------------------|-------------------------|-----------|---------|----------|----------|-----------|---------|
| Farmer Profile (INFO-001) | DOM-AGRI | DOM-IAM | Extension lead | Farmer/officer | Advisory/finance | DPC (STK-022) | Internal audit |
| Payment (INFO-014) | DOM-FIN | DOM-FIN | Finance steward | Payer/system | Payee/finance | BoZ/FIC (STK-060) | Internal/external audit |
| Warehouse Receipt (INFO-010) | DOM-TRADE | DOM-TRADE | WRS steward | Warehouse operator | Financier/buyer | ZAMACE/regulator | Auditor |
| Permit/Licence (INFO-027) | DOM-CMP | DOM-CMP | Compliance steward | Regulator | Operator | MMMD/ZEMA (STK-009/010) | Auditor |
| Env Monitoring (INFO-024) | DOM-ENV | DOM-ENV | Env steward | Operator/sensor | ZEMA/mgmt | ZEMA (STK-010) | Env auditor |
| Person Identity (INFO-040) | DOM-IAM | DOM-IAM | Identity steward | Registrant | All domains | DPC (STK-022) | Security audit |
| Financial Ledger (INFO-042) | DOM-FIN | DOM-FIN | Finance steward | Finance ops | Management/tax | ZRA (STK-002) | External audit |
| Reference/Master (INFO-045) | DOM-CFG | DOM-CFG | MDM steward | MDM team | All domains | — | Data governance |
> Every information object in `01_ENTERPRISE_INFORMATION_CATALOGUE.csv` carries `domain_owner`, `steward`, `source_stakeholder`, and `consuming_stakeholders` — this register summarises the accountable roles across the enterprise.

## Output 7 — Data Classification Register
Levels: **Public · Internal · Confidential · Restricted · Highly Restricted.**
| Level | Definition | Example information | Rationale |
|-------|-----------|---------------------|-----------|
| Public | Freely shareable | Advisory content (INFO-007); market prices (INFO-012); reference data (REF public) | Intended for wide dissemination |
| Internal | Business-only, low harm | Crop/plot records (INFO-002/003); progress reports (INFO-033) | Operational data, limited sensitivity |
| Confidential | Business-sensitive | Invoices (INFO-016); warehouse receipts (INFO-010); mine plans (INFO-020); permits (INFO-027); monitoring (INFO-024) | Commercial/regulatory sensitivity |
| Restricted | Personal/financial | Payments (INFO-014); loans (INFO-015); person identity (INFO-040); audit log (INFO-043); consent (INFO-044) | Personal data (DPA) / financial integrity |
| Highly Restricted | Credentials/secrets | Credential references (ATR-048); secrets | Direct security/breach impact |
> Classification drives NFR controls (`REQ-N-008..013/019`) and business rules (`BR-001/002/020`); personal data classified Restricted per Data Protection Act (`REG-0024`). Classifications recorded per object in the information catalogue `confidentiality` column.
