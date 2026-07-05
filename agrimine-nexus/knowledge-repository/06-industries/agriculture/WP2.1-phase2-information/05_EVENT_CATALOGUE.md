---
id: WP2.1-P2-EVC
title: Event Catalogue — Zambian Agriculture (WP2.1 Phase 2)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Operational events
keywords: [events, state-change, operations]
summary: Catalogue of events that change operational state across agricultural workflows. Information intelligence only.
source: SRC-0045;SRC-0051;SRC-0052;SRC-0059
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 80
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [02_TRANSACTION_CATALOGUE.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Event Catalogue — Zambian Agriculture

> Events change operational state and typically produce a transaction/record. Columns: **Triggered by** · **State change** · **Data produced** · **Workflow**.

| ID | Event | Triggered by | State change | Data produced | Workflow |
|----|-------|--------------|--------------|---------------|----------|
| EV-01 | Farmer registered | Enrolment | non-registered → registered | farmer record (ZIAMIS) [SRC-0058] | WF-007 |
| EV-02 | Deposit confirmed | Farmer contribution | pending → funded | deposit confirmation [SRC-0045] | WF-007 |
| EV-03 | Voucher issued | Deposit captured | funded → entitled | e-voucher code [SRC-0045] | WF-007 |
| EV-04 | Input redeemed | Redemption at dealer | entitled → supplied | GIN [SRC-0045] | WF-007,008 |
| EV-05 | Planting | Reliable rains | field prepared → planted | planting record | WF-011 |
| EV-06 | Fertilizer/chemical applied | Growth stage/threshold | untreated → treated | application record | WF-015,018 |
| EV-07 | Disease/pest detected | Scouting | healthy → infested | pest/disease report | WF-013,015,016 |
| EV-08 | Weather alert | Forecast/warning | normal → alert | advisory/alert [SRC-0059] | WF-019 |
| EV-09 | Harvest | Crop maturity | standing crop → harvested | harvest record | WF-024 |
| EV-10 | Yield estimated | Forecast/PHS | unknown → estimated | yield estimate | WF-025 |
| EV-11 | Warehouse entry | Deposit at store | in-field → stored | deposit note / WR issue [SRC-0061] | WF-026 |
| EV-12 | Warehouse receipt issued | Certified deposit | stored → titled (collateralisable) | warehouse receipt [SRC-0061] | WF-026 |
| EV-13 | Warehouse exit | Withdrawal/sale | stored → released | release note | WF-026,029 |
| EV-14 | Transport departure | Dispatch | at origin → in transit | waybill | WF-028 |
| EV-15 | Transport arrival | Delivery | in transit → delivered | delivery note | WF-028 |
| EV-16 | Sale / purchase | Market transaction | owned → sold | sale record [SRC-0052] | WF-029 |
| EV-17 | Delivery to buyer | Consignment received | dispatched → received | delivery confirmation | WF-029 |
| EV-18 | Invoice raised | Billing | delivered → billed | invoice | WF-029 |
| EV-19 | Payment made | Settlement | billed → paid | payment/MMoney receipt | WF-029,032 |
| EV-20 | Contract approved | Outgrower agreement | prospect → contracted | contract record [SRC-0055] | WF-030 |
| EV-21 | Inspection | Audit/quality check | unverified → inspected | inspection report | WF-034 |
| EV-22 | Approval (credit/claim) | Decision | applied → approved/rejected | decision record | WF-036,037 |
| EV-23 | Maintenance | Service due/breakdown | operational → serviced | service log | WF-021 |
| EV-24 | Market price update | Market movement | old price → new price | price record [SRC-0053] | WF-029 |
| EV-25 | Aggregation completed | Bulking | lots → consolidated graded lot | aggregation record [SRC-0051] | WF-031 |
| EV-26 | Emergency declared | Shock (drought/flood) | normal → emergency | disaster assessment | WF-040 |
| EV-27 | Extension visit | Advisory | pre-advice → advised | ADEO diary entry [SRC-0050] | WF-038 |

## Note
The events with **digital state-capture today** are those on the **ZIAMIS/e-voucher rail (EV-01..04)**, **warehouse-receipt (EV-11/12)**, **mobile-money payment (EV-19)**, and **weather alerts (EV-08)**. Field/agronomic events (EV-05..07, EV-09) are largely captured on paper or not at all.
