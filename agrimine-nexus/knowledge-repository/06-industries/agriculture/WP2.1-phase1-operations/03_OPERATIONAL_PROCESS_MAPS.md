---
id: WP2.1-P1-MAPS
title: Operational Process Maps — Zambian Agriculture (WP2.1 Phase 1)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Process maps
keywords: [process-maps, BPMN, season, FISP, marketing, outgrower]
summary: End-to-end process maps for the core agricultural operational flows in Zambia. Operational intelligence only.
source: SRC-0045;SRC-0051;SRC-0052;SRC-0054;SRC-0056
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 82
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

# Operational Process Maps — Zambian Agriculture

> Representative end-to-end maps (BPMN-style, Mermaid). These describe *how work flows*, not software.

## 1. Smallholder season lifecycle
```mermaid
flowchart LR
    A([Season start Sep]) --> B[Land prep WF-002]
    B --> C[Input plan & FISP registration WF-005/007/008]
    C --> D{Reliable rains?}
    D -- No --> D
    D -- Yes --> E[Planting WF-011 Nov-Dec]
    E --> F[Crop mgmt: weeding/pest/nutrient WF-015..018]
    F --> G[Scouting & monitoring WF-013/014]
    G --> H[Harvest WF-024 May-Aug]
    H --> I[Storage / WRS WF-026]
    I --> J[Market sales FRA/ZAMACE/buyer WF-029]
    J --> K[Season close-out WF-041]
    K --> A
```

## 2. FISP e-voucher input supply
```mermaid
flowchart TD
    A([FISP opens]) --> B[Farmer registers at District Ag Office - NRC, mobile, farmland proof]
    B --> C[e-KYC in ZIAMIS]
    C --> D{Verified?}
    D -- No --> B
    D -- Yes --> E[Farmer deposits K400 - govt adds K8000]
    E --> F[SMS confirmation]
    F --> G[Redeem code created within 24h]
    G --> H[Farmer to accredited agro-dealer with NRC + code]
    H --> I[Select inputs; sign GIN]
    I --> J[Transaction SMS; inputs collected]
```
*(Source: [SRC-0045] MoA; [SRC-0048] PDU.)*

## 3. Harvest-to-market with warehouse receipts
```mermaid
flowchart LR
    A[Harvest WF-024] --> B[Dry & grade]
    B --> C{Sell now or store?}
    C -- Sell --> D[Aggregate WF-031 / sell to FRA depot WF-029]
    C -- Store --> E[Deposit at certified warehouse]
    E --> F[Warehouse receipt issued WRS]
    F --> G{Need cash?}
    G -- Yes --> H[Use receipt as loan security - bank]
    G -- No --> I[Hold for better price]
    F --> J[Trade on ZAMACE platform]
```
*(Source: [SRC-0051] PARM; [SRC-0052] FRA; [SRC-0053] ZAMACE.)*

## 4. Contract farming / outgrower cycle
```mermaid
flowchart TD
    A([Agribusiness recruits via distributor]) --> B[Contract signed; central registry]
    B --> C[Inputs on credit Oct-Dec]
    C --> D[Distributor monitors crop 15-20 farmers]
    D --> E[Harvest]
    E --> F[Company buys back from June]
    F --> G[Input debt deducted from payment]
    G --> H{Side-selling risk}
    H -- managed --> I[Repeat next season]
```
*(Source: [SRC-0054] J-PAL; [SRC-0055] World Bank.)*

## 5. Extension advisory flow
```mermaid
flowchart LR
    A[Farmer query/need] --> B[Camp Extension Officer]
    B --> C{Complex?}
    C -- No --> D[Advice / demo / FFS]
    C -- Yes --> E[Block Extension Officer / SMS specialist]
    E --> F[District DACO / research]
    D --> G[Farmer applies practice]
    F --> D
```
*(Structure per [SRC-0050] MEAS; [SRC-0049] NAESP.)*

## Note
Maps are operational (current-state) descriptions. No future/target software design is implied.
