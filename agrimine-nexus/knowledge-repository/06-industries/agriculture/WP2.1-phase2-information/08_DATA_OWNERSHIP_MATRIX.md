---
id: WP2.1-P2-OWN
title: Data Ownership Matrix — Zambian Agriculture (WP2.1 Phase 2)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Data ownership
keywords: [ownership, custody, access, retention]
summary: Who owns, may modify, consumes, and retains each agricultural information domain. Information intelligence only.
source: SRC-0045;SRC-0058;SRC-0061;SRC-0062
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 78
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [07_DATA_LIFECYCLE_REGISTER.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Data Ownership Matrix — Zambian Agriculture

| Data domain | Owner | May modify | Consumes | Retention basis |
|-------------|-------|-----------|----------|-----------------|
| Farmer registry | MoA / ZIAMIS | MoA officers | MoA, agro-dealers, suppliers, banks, insurers | persistent registry [SRC-0058] |
| FISP voucher / GIN | MoA / ZIAMIS | SZI/MoA; dealer (redeem) | MoA, farmer, dealer, bank | per season (reconciliation) [SRC-0045] |
| Field / agronomic records | Farmer | Farmer | Farmer, extension | none standardised (paper) |
| Harvest / yield (own) | Farmer | Farmer | Farmer, buyer | none standardised |
| Yield / production (aggregate) | ZamStats | ZamStats | Govt, planners, FRA | statistical archive [SRC-0056] |
| Warehouse receipt / stored grain | Warehouse operator (issuer); title→holder | Operator | Farmer, bank, buyer, Authority | statutory (Agricultural Credits Act; Collateral Registry) [SRC-0061][SRC-0062] |
| Sale / payment | Transacting parties | Buyer / bank | Farmer, buyer | transaction/programme |
| Outgrower contract / credit | Agribusiness | Company / distributor | Company, farmer | contract term [SRC-0055] |
| Loan / credit | Financial institution | FI | FI, farmer | loan term |
| Insurance policy / claim | Insurer (via FISP) | Insurer | Farmer, MoA | policy term [SRC-0059] |
| Extension records (ADEO) | MoA | Extension officer | MoA | programme [SRC-0050] |
| Weather / advisory | ZMD / provider | Provider | Farmer, extension, insurer | provider archive [SRC-0059] |
| Cooperative membership/aggregation | Cooperative | Cooperative officers | Members, buyers | cooperative governance |
| Administrative geography | GRZ (ZamStats/MLGRD) | GRZ | all | national (WP1.1) |

## Observations (descriptive)
- **State/programme-held data** (farmer registry, vouchers, warehouse receipts, statistics) has **clear ownership and modification control**.
- **Farmer-held operational data** (fields, applications, harvest, records) is **owned by the farmer but not systematically retained or shared**, limiting downstream use.
- **Third-party-held data** (outgrower ledgers, buyer records, insurer/bank data) is **siloed** in each organisation's system.
- Data-protection obligations (Data Protection Act No.3 of 2021, WP1.1) apply to personal data across these domains — noted as context, not designed here.
