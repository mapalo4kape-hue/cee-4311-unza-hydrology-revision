---
id: WP2.1-P2-KG
title: Knowledge Graph Expansion — WP2.1 Phase 2
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Knowledge extraction
keywords: [knowledge-graph, entities, relationships, master-data]
summary: Expands the knowledge graph with agricultural master-data entities and evidence-based relationships from the information ecosystem. No schema, ERD, or UML.
source: derived
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 82
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../../../10-requirements/GRAPH_NODES.csv, ../../../10-requirements/GRAPH_EDGES.csv, 06_RELATIONSHIP_CATALOGUE.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Knowledge Graph Expansion — WP2.1 Phase 2

> Registers the agricultural information ecosystem into the knowledge graph as **entities and evidence-based relationships**. This is knowledge modelling, **not** a database schema, ERD, or UML.

## 1. Added to the graph
- **Entity instances (16):** `ENT-FARMER`, `ENT-FARM`, `ENT-FIELD`, `ENT-COOPERATIVE`, `ENT-AGRODEALER`, `ENT-WAREHOUSE`, `ENT-VOUCHER`, `ENT-WRECEIPT`, `ENT-COMMODITY`, `ENT-CONTRACT-OG`, `ENT-EXTOFFICER`, `ENT-INPUTPRODUCT`, `ENT-BUYER-FRA`, `ENT-COOP-AGG` (+ Phase-1 `LOC-*`). Each classified to a taxonomy node and evidence-linked.
- **Findings (3):** `F-0053` (ZIAMIS farmer registry), `F-0054` (warehouse-receipt content & legal basis), `F-0055` (weather-index insurance via ZIAMIS).
- **Relationship edges (`E-0072`–`E-0090`):** ownership, composition (`PART_OF`), redemption, issuance (`PRODUCES`), purchase (`CONSUMES`), advisory (`MONITORED_BY`), and contract (`GOVERNED_BY`) — each tied to the Relationship Catalogue (REL-xx) and its evidence.

## 2. Information objects registered (not schematised)
Master data (`MD-01`–`MD-31`), transactions (`TX-01`–`TX-34`), documents (`DC-01`–`DC-28`), measurements (`MS-01`–`MS-22`), and events (`EV-01`–`EV-27`) are catalogued in their respective outputs and cross-referenced to workflows (`WF-001`–`WF-041`) and entities. They are recorded as **information items**, not tables/columns/keys.

## 3. Coverage
Every ACT-008 workflow now has its information footprint identified (created/received/updated/stored/exchanged/reported), with ownership, modification rights, consumers, retention, and current recording medium captured in the Lifecycle and Ownership outputs.

## 4. Constraint respected
No software tables, database schemas, APIs, or UML were produced. Requirement/feature/AI extraction remains deferred. The graph now supports future traceability from these information objects to eventual requirements in later work packages.
