---
id: WP2.1-P2-TXC
title: Transaction Catalogue — Zambian Agriculture (WP2.1 Phase 2)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Transaction data
keywords: [transactions, records, operations]
summary: Catalogue of operational transactions across agricultural workflows. Information intelligence only.
source: SRC-0045;SRC-0051;SRC-0052;SRC-0055;SRC-0058
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 80
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_MASTER_DATA_CATALOGUE.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Transaction Catalogue — Zambian Agriculture

> Each transaction = an operational record created/updated during a workflow. Columns: **Trigger** · **Actors** · **Master data referenced** · **Source document** · **Recorded (current)** · **Workflow**.

| ID | Transaction | Trigger | Actors | Master data referenced | Source document | Recorded (current) | Workflow |
|----|-------------|---------|--------|------------------------|-----------------|--------------------|----------|
| TX-01 | Farmer registration | FISP/registry enrol | Farmer, DACO | Farmer, Cooperative, Camp | Registration form | ZIAMIS + paper [SRC-0058] | WF-007 |
| TX-02 | Farm registration | New farm | Farmer, extension | Farm, Location | — | paper/verbal | WF-001 |
| TX-03 | Field registration | Field mapping | Farmer, extension | Field, Farm | field sketch | paper (Field Area app GPS) | WF-003 |
| TX-04 | Input purchase | Buy inputs | Farmer, agro-dealer | Input Product, Agro-dealer | receipt | paper/POS | WF-007,008,009 |
| TX-05 | FISP redemption | e-voucher redeem | Farmer, agro-dealer | Voucher, Input Product | GIN | ZIAMIS + signed GIN [SRC-0045] | WF-007,008 |
| TX-06 | Inventory receipt | Stock in | Farmer/cooperative | Input Product, Storage | stock card | paper | WF-010 |
| TX-07 | Inventory issue | Stock out | Farmer/cooperative | Input Product | issue note | paper | WF-010 |
| TX-08 | Planting record | Sowing | Farmer | Field, Seed Variety | planting record | paper diary | WF-011 |
| TX-09 | Fertilizer application | Top-dress/basal | Farmer | Field, Fertilizer | field book | paper | WF-018 |
| TX-10 | Chemical application | Spray | Farmer | Field, Chemical | spray record | paper | WF-015,016,017 |
| TX-11 | Irrigation event | Watering | Farmer | Field, Equipment | irrigation log | paper | WF-012 |
| TX-12 | Scouting observation | Field walk | Farmer/agronomist | Field | scouting form | paper | WF-013 |
| TX-13 | Pest report | Pest detected | Farmer/extension | Field | pest note | paper/verbal | WF-015 |
| TX-14 | Disease report | Disease detected | Farmer/extension/lab | Field | diagnosis note | paper/verbal | WF-016 |
| TX-15 | Harvest record | Harvesting | Farmer | Field, Commodity | harvest record | paper | WF-024 |
| TX-16 | Yield estimate | Forecast/PHS | Farmer/ZamStats | Field, Commodity | crop forecast form | survey [SRC-0056] | WF-025 |
| TX-17 | Storage entry | Store produce | Farmer/warehouse | Commodity, Storage | stock/deposit note | paper/WRS | WF-026 |
| TX-18 | Warehouse receipt issue | Certified deposit | Warehouse operator | Warehouse, Commodity | warehouse receipt | WRS + paper [SRC-0061] | WF-026 |
| TX-19 | Transport dispatch | Move goods | Transporter | Commodity, Transporter | waybill | paper | WF-028 |
| TX-20 | Produce sale | Sell | Farmer, buyer/FRA | Commodity, Buyer | sale contract | depot system/paper [SRC-0052] | WF-029 |
| TX-21 | Commodity delivery | Deliver to buyer | Farmer/transporter | Commodity, Buyer | delivery note | paper | WF-028,029 |
| TX-22 | Invoice | Bill | Buyer/dealer | Commodity/Input | invoice/GIN | paper/ZIAMIS | WF-007,029 |
| TX-23 | Payment | Settle | Buyer/farmer/bank | Financial Institution | receipt/MMoney | mobile money/bank | WF-029,032 |
| TX-24 | Loan application | Seek finance | Farmer, bank/MFI | Financial Institution, WR | loan forms | forms/branch [SRC-0051] | WF-037 |
| TX-25 | Insurance claim | Loss event | Farmer, insurer/FISP | Farmer, Field | claim form | forms/ZIAMIS [SRC-0059] | WF-036 |
| TX-26 | Inspection | Audit/quality | Regulator/buyer | Farm/Commodity | inspection report | paper | WF-034 |
| TX-27 | Extension visit | Advisory | CEO | Farmer, Field | ADEO diary | paper [SRC-0050] | WF-038 |
| TX-28 | Training attendance | FFS/training | Extension/farmers | Farmer | attendance register | paper | WF-038 |
| TX-29 | Asset maintenance | Service | Owner/provider | Equipment | service log | paper | WF-021 |
| TX-30 | Fuel consumption | Refuel/use | Farmer | Equipment | fuel log | paper | WF-022 |
| TX-31 | Equipment assignment | Allocate machine | Manager/provider | Equipment, Employee | booking record | paper | WF-021 |
| TX-32 | Weather observation | Reading/forecast | ZMD/farmer | Location, Season | advisory/log | SMS/paper [SRC-0059] | WF-019 |
| TX-33 | Deposit (FISP) | Farmer contribution | Farmer, bank/MMO | Farmer, Voucher | deposit confirmation | bank/MMoney→ZIAMIS [SRC-0045] | WF-007 |
| TX-34 | Aggregation / grading | Bulk lots | Cooperative/aggregator | Commodity | aggregation record | scales/moisture meter [SRC-0051] | WF-031 |

## Note
Most transactions are **paper today**; the digitally-captured ones are **FISP registration, deposit, redemption (GIN), weather advisory, warehouse receipt, and mobile-money payment**.
