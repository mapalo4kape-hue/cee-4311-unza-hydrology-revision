---
id: WP2.1-P2-RELC
title: Relationship Catalogue — Zambian Agriculture (WP2.1 Phase 2)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Entity relationships
keywords: [relationships, entities, information-ecosystem]
summary: Evidence-based relationships between agricultural master entities. Information intelligence only — no schema, ERD, or UML.
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

# Relationship Catalogue — Zambian Agriculture

> Each relationship is evidence-based: cited to a source where the mechanism is documented, or marked **[WF]** where it derives from the ACT-008 operational workflows (themselves evidenced). No ERD/UML/schema.

| ID | Relationship | Basis / evidence |
|----|--------------|------------------|
| REL-01 | Farmer **owns/operates** Farm | [WF-001] operational |
| REL-02 | Farm **contains** Fields | [WF-003] operational |
| REL-03 | Field **grows** Crop | [WF-011] operational |
| REL-04 | Farmer **belongs to** Cooperative | FISP requires group/cooperative [SRC-0045] |
| REL-05 | Farmer **registered in** ZIAMIS (has digital ID, NRC link) | [SRC-0058] |
| REL-06 | Farmer **redeems voucher at** Agro-dealer | [SRC-0045] |
| REL-07 | Agro-dealer **accredited in** ZIAMIS | [SRC-0046] |
| REL-08 | Supplier **supplies** Input Product to Agro-dealer | [SRC-0058] |
| REL-09 | Farmer **contributes deposit via** Financial Institution/MMO | [SRC-0045] |
| REL-10 | Farmer **applies inputs to** Field | [WF-015,018] |
| REL-11 | Harvest **produces** Commodity | [WF-024] |
| REL-12 | Commodity **stored in** Warehouse/Storage Facility | [WF-026] |
| REL-13 | Warehouse **issues** Warehouse Receipt for Commodity | [SRC-0061] |
| REL-14 | Warehouse Receipt **secures** Loan (Financial Institution) | Agricultural Credits Act; Collateral Registry [SRC-0062] |
| REL-15 | Buyer/FRA **purchases** Commodity from Farmer | [SRC-0052] |
| REL-16 | Transporter **moves** Commodity/Inputs | [WF-028] |
| REL-17 | Payment **settles** Invoice/Sale | [WF-029] |
| REL-18 | Extension Officer **advises/visits** Farmer (within Camp/Block) | [SRC-0050] |
| REL-19 | Agribusiness **contracts** Farmer (outgrower) via Distributor | [SRC-0055] |
| REL-20 | Agribusiness **provides inputs-on-credit to** Farmer; **buys back** Harvest | [SRC-0054] |
| REL-21 | Cooperative **aggregates** Commodity from members | [SRC-0051] |
| REL-22 | Insurer **covers** Farmer's Crop (via FISP) | [SRC-0059] |
| REL-23 | Laboratory **analyses** Soil/Sample for Field | [WF-004] |
| REL-24 | Camp **part of** Block **part of** District (extension) | [SRC-0050] |
| REL-25 | Farm/Field **located in** Administrative Area (province/district) | [WF-003] + WP1.1 |
| REL-26 | Farmer **insures crop through** ZIAMIS-engaged Insurer | [SRC-0059] |
| REL-27 | Commodity **traded on** ZAMACE (via Warehouse Receipt) | [SRC-0053] |
| REL-28 | Equipment **assigned to/operated on** Field | [WF-021] |
| REL-29 | Weather Observation **applies to** Location/Season | [WF-019] |
| REL-30 | Farmer **linked to buyers/suppliers/finance via** e-Business Directory | [SRC-0063] |

## Note
Relationships are documented as **operational facts**, not as a data model. Instantiation as knowledge-graph edges is done in the Knowledge Graph Expansion output; no schema, foreign keys, or UML are produced.
