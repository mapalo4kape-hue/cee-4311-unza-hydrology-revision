---
id: WP2.1-P2-EXCH
title: Information Exchange Matrix — Zambian Agriculture (WP2.1 Phase 2)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Information exchange
keywords: [exchange, actors, channels, interfaces]
summary: Who exchanges what information with whom, and through which channel, across Zambian agriculture. Information intelligence only.
source: SRC-0045;SRC-0051;SRC-0058;SRC-0059;SRC-0063
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 80
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../WP2.1-phase1-operations/05_INFORMATION_FLOW_CATALOGUE.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Information Exchange Matrix — Zambian Agriculture

> From → To, the information exchanged, and the current channel. Extends the ACT-008 Information Flow Catalogue.

| ID | From | To | Information | Channel (current) |
|----|------|----|-------------|-------------------|
| EX-01 | Farmer | MoA/ZIAMIS | Registration (bio, NRC, farmland, cooperative) | District office → ZIAMIS [SRC-0058] |
| EX-02 | ZIAMIS/SZI | Farmer | Voucher code, confirmations | SMS [SRC-0045] |
| EX-03 | Farmer | Bank/MMO | Deposit (contribution) | mobile money / bank |
| EX-04 | Bank/MMO | ZIAMIS | Deposit confirmation | integration [SRC-0058] |
| EX-05 | Farmer | Agro-dealer | NRC + voucher code | in person [SRC-0045] |
| EX-06 | Agro-dealer | ZIAMIS/MoA | Redemption (GIN), stock, prices | ZIAMIS |
| EX-07 | Supplier | Agro-dealer/ZIAMIS | Product list, prices | ZIAMIS [SRC-0058] |
| EX-08 | ZMD/provider | Farmer/extension | Weather forecast, alerts | SMS, radio [SRC-0059] |
| EX-09 | Extension officer | Farmer | Advice, demos, training | verbal, FFS, meetings [SRC-0050] |
| EX-10 | Farmer | Extension | Field problems, queries | verbal |
| EX-11 | Farmer | ZamStats | Crop forecast / PHS responses | survey [SRC-0056] |
| EX-12 | Farmer/cooperative | Warehouse operator | Deposit (commodity, quality) | in person [SRC-0051] |
| EX-13 | Warehouse operator | Farmer/bank | Warehouse receipt | WRS + paper [SRC-0061] |
| EX-14 | Bank | Farmer | Loan decision / disbursement | branch/mobile |
| EX-15 | Farmer | Buyer/FRA | Produce offer, delivery | in person / depot [SRC-0052] |
| EX-16 | Buyer/FRA | Farmer | Purchase, payment | depot / mobile money |
| EX-17 | Transporter | Farmer/buyer | Waybill, delivery status | paper |
| EX-18 | Agribusiness | Farmer (via distributor) | Contract, inputs-on-credit, buyback terms | distributor, paper [SRC-0055] |
| EX-19 | Farmer | Agribusiness | Harvest delivery, debt settlement | in person |
| EX-20 | Insurer/FISP | Farmer | Policy, payout | ZIAMIS/SMS [SRC-0059] |
| EX-21 | Cooperative | Members | Input allocation, aggregation, prices | meetings, verbal |
| EX-22 | Extension/cooperative | MoA/donor | Programme reports | forms/ZIAMIS |
| EX-23 | ZIAMIS e-Business Directory | Farmer | Links to buyers/suppliers/finance/mechanisation | ZIAMIS [SRC-0063] |
| EX-24 | ZAMACE | Traders/farmers | Prices, trades, receipts | ZAMACE platform [SRC-0053] |
| EX-25 | Regulator/buyer | Farmer/exporter | Inspection results, certification | paper |

## Observations (descriptive)
- **Digital exchange rails today:** ZIAMIS (registration/redemption/e-extension/e-Business Directory), mobile money (deposits/payments), SMS (codes/advisories), WRS, ZAMACE.
- **Analogue exchange:** most farmer↔extension, farmer↔buyer, cooperative↔member, and transport exchanges remain **verbal/paper/in-person**.
- Exchanges are **point-to-point and fragmented**; no single interoperable flow — recorded as an information-ecosystem characteristic (not a design proposal).
