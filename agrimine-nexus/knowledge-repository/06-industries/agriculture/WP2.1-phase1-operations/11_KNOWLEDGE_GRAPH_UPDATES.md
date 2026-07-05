---
id: WP2.1-P1-KG
title: Knowledge Graph Updates — WP2.1 Phase 1
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Knowledge extraction
keywords: [knowledge-graph, workflows, entities, stakeholders]
summary: Registers agricultural workflows, entities, relationships, and stakeholders into the knowledge graph. Traceable knowledge only — no software requirements.
source: derived
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 84
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../../../10-requirements/GRAPH_NODES.csv, ../../../10-requirements/GRAPH_EDGES.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: [WF-001..WF-041]
---

# Knowledge Graph Updates — WP2.1 Phase 1

> Traceable knowledge registration (ROM Phase 4). **No software requirements** created.

## 1. Added to the graph
- **Workflow nodes `WF-001`–`WF-041`** (41 agricultural operational workflows) in `GRAPH_NODES.csv`, classified `TAX-PRC`.
- **Findings `F-0047`–`F-0052`** (Zambia-specific operational mechanisms) with `DERIVED_FROM` edges to evidence.
- **Edges `E-0059`–`E-0071`** linking key workflows to their evidencing findings (`EVIDENCED_BY`) and findings to sources (`DERIVED_FROM`).

## 2. Entities identified (domain objects — to be instantiated as WP2.1 deepens)
ENT-FARMER, ENT-FARM, ENT-FIELD, ENT-CROP, ENT-INPUT, ENT-HARVEST, ENT-COOPERATIVE, ENT-AGRODEALER, ENT-WAREHOUSE, ENT-CONTRACT, ENT-VOUCHER (FISP e-voucher), ENT-WAREHOUSE-RECEIPT, ENT-EXTENSION-OFFICER, ENT-TRANSACTION, ENT-EQUIPMENT, ENT-DOCUMENT (GIN, contract, WRS). *(IDs will be minted when the domain model is populated in a later phase to avoid premature over-modelling.)*

## 3. Relationships (operational)
- Farmer `PARTICIPATES_IN` FISP; `REDEEMS_AT` agro-dealer; `MEMBER_OF` cooperative.
- Agro-dealer `ACCREDITED_IN` ZIAMIS; `ISSUES` GIN.
- Farmer `DELIVERS_TO` FRA/warehouse; warehouse `ISSUES` warehouse receipt; receipt `SECURES` bank loan.
- Agribusiness `CONTRACTS` farmer via distributor; `PROVIDES` inputs-on-credit; `BUYS_BACK` harvest.
- Extension (CEO) `ADVISES` farmer within block/camp hierarchy.

## 4. Stakeholders registered
The 20 stakeholder types (Stakeholder Operations Handbook) are catalogued with roles, tools, information flows, and the workflows they drive.

## 5. Business processes supported (for future WP mapping — not requirements)
Input supply (FISP), extension advisory, production management, harvest & post-harvest, aggregation, warehouse-receipt finance, marketing (FRA/ZAMACE), contract farming, and reporting.

## 6. Future work packages impacted
WP2.1 later phases (crop-specific), WP2.5 (logistics), WP3.1–3.4 (AI/GIS/IoT/drone — later), WP4.x (product/competitor — later), WP5.x (business — later). **No requirements, features, or AI opportunities defined here.**
