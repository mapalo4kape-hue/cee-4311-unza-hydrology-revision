---
id: WP2.1-P1-INFO
title: Information Flow Catalogue — Zambian Agriculture (WP2.1 Phase 1)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Information flows
keywords: [information-flow, data, channels, ZIAMIS, SMS]
summary: Catalogue of information produced and consumed across agricultural operations and the channels used. Operational intelligence only.
source: SRC-0045;SRC-0046;SRC-0051;SRC-0055
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 80
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_AGRICULTURAL_WORKFLOW_LIBRARY.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Information Flow Catalogue — Zambian Agriculture

| ID | Information item | Produced by | Consumed by | Channel (current) | Frequency | Notes |
|----|------------------|-------------|-------------|-------------------|-----------|-------|
| INF-01 | Farmer registration / profile | Farmer → District Ag Office | MoA, agro-dealer | ZIAMIS + paper | seasonal | e-KYC via NRC+mobile [SRC-0046] |
| INF-02 | e-Voucher / redeem code | ZIAMIS/SZI | Farmer, agro-dealer | SMS | seasonal | 24h issue; 30-day window [SRC-0045] |
| INF-03 | Input transaction (GIN) | Agro-dealer | MoA/ZIAMIS, farmer | ZIAMIS + signed paper | per redemption | reconciliation to subsidy [SRC-0045] |
| INF-04 | Weather forecast / advisory | ZMD, providers | Farmer, extension | SMS, radio, verbal | daily/seasonal | patchy reach |
| INF-05 | Extension advice | CEO/BEO | Farmer | verbal, meetings, FFS, ADEO diary | season | ratio 1:1,200+ [SRC-0049] |
| INF-06 | Scouting / crop status | Farmer, agronomist | Farmer, extension | paper/notebook, verbal | weekly | rarely digitised |
| INF-07 | Field / activity records | Farmer, manager | Farmer, bank, buyer | paper diary, memory | ongoing | completeness low |
| INF-08 | Prices (input & output) | Markets, FRA, ZAMACE | Farmer, cooperative | verbal, radio, SMS, ZAMACE | frequent | price discovery gaps |
| INF-09 | Warehouse receipt | Warehouse operator | Farmer, bank | WRS system + paper | at deposit | loan collateral [SRC-0051] |
| INF-10 | Sales / purchase record | Buyer/FRA/cooperative | Farmer, buyer | depot systems, paper | at sale | payment delays common |
| INF-11 | Contract & credit ledger | Agribusiness/distributor | Farmer, company | company registry, paper | season | debt reconciliation [SRC-0055] |
| INF-12 | Loan application & status | Farmer/cooperative | Bank/MFI | forms, branch, phone | pre-season | slow turnaround |
| INF-13 | Insurance policy & claim | Insurer/FISP | Farmer | forms, SMS | seasonal/post-loss | basis-risk on index |
| INF-14 | Crop forecast / yield estimate | ZamStats/MoA/NRSC | Govt, planners, FRA | surveys, remote sensing | annual | PHS/CFS + RS [SRC-0056] |
| INF-15 | Aggregation / grade data | Cooperative/aggregator | Buyer, warehouse | scales, moisture meters, paper | harvest | quality gating [SRC-0051] |
| INF-16 | Compliance / permits | Regulator/buyer | Farmer/exporter | certificates, paper | as required | awareness gaps |
| INF-17 | Program reports | Extension/cooperative | MoA/donors | forms, ZIAMIS | periodic | duplication |
| INF-18 | Emergency assessment | DMMU/govt/NGO | Govt, relief | assessment forms | event | slow flow |

## Observations (operational, not recommendations)
- **Dominant channels today:** verbal/paper at field level; **SMS + mobile money + ZIAMIS** as the digital backbone; **ZAMACE/WRS** for structured trade.
- **Weakest links (information):** field records (INF-06/07), local prices (INF-08), and extension reach (INF-05) — high-volume, low-digitisation, high-latency.
