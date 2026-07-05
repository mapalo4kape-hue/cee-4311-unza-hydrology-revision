---
id: WP1.1-P2-KG
title: Knowledge Graph Updates — WP1.1 Phase 2
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 1 — Foundation Research
work_package: WP1.1
industry: cross-industry
topic: Knowledge extraction
keywords: [knowledge-graph, entities, relationships, stakeholders]
summary: Registers the entities, relationships, stakeholders, business processes supported, and future work packages impacted by the Phase 2 evidence. Traceable knowledge only — no software requirements.
source: derived
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 88
evidence_level: 1
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../../10-requirements/GRAPH_NODES.csv, ../../10-requirements/GRAPH_EDGES.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Knowledge Graph Updates — WP1.1 Phase 2

> Per the knowledge-extraction requirement: for each theme, the entities, relationships, stakeholders, business processes supported, and future work packages impacted. **No software requirements** — traceable knowledge registration only. Findings `F-0022`–`F-0046` and edges `E-0032`–`E-0058` added to `GRAPH_NODES.csv` / `GRAPH_EDGES.csv`.

## 1. Extraction by theme

| Theme | Key entities (types) | Relationships | Stakeholders | Business processes supported | Future WP impacted |
|-------|----------------------|---------------|--------------|------------------------------|--------------------|
| Economy | ENT-ORG (ZamStats, BoZ, MoFNP), ENT-TRANSACTION, ENT-LOCATION | GDP `MEASURED_BY` KPI; sectors `PART_OF` economy | Government, investors, enterprises | Financial reporting, budgeting, market sizing | WP2.1-2.5 (industry sizing), WP5.1 (business model) |
| Population | ENT-LOCATION (provinces/districts), ENT-STAKEHOLDER | province `PART_OF` Zambia; households `LOCATED_AT` | ZamStats, planners | Market segmentation, service planning | WP1.3 (stakeholders), all WP2 |
| Infrastructure | ENT-ASSET (power plants, grid), ENT-ROUTE (roads/rail), ENT-ORG (ZESCO, RDA) | grid `MONITORED_BY` sensors; roads `LOCATED_AT` provinces | ZESCO, ERB, RDA, ZICTA | Operations, logistics, energy planning | WP2.2-2.5, WP3.3 (IoT), WP3.5 (architecture/offline) |
| Digital | ENT-ORG (ZICTA, MNOs), ENT-STAKEHOLDER | connectivity `GOVERNED_BY` ZICTA | ZICTA, operators, users | Digital service delivery, connectivity | WP3.1 (AI), WP3.5, WP4.3 (integration) |
| Financial | ENT-ORG (BoZ, banks, MNOs, insurers), ENT-TRANSACTION | payments `GOVERNED_BY` BoZ | BoZ, PIA, banks, MNOs | Payments, credit, insurance | WP4.3 (mobile-money integration), WP5.1 |
| Logistics | ENT-ROUTE (corridors), ENT-LOCATION (border posts) | corridors `PART_OF` regional network | Min. Transport, ZRA, RECs | Cross-border trade, freight | WP2.5 (logistics), WP4.3 |
| Climate | ENT-WEATHER, ENT-LOCATION (AER zones, basins) | zones `PART_OF` Zambia; basins transboundary | ZMD, WARMA, ZEMA | Agri planning, water/hydropower, risk | WP2.1 (agriculture), WP3.2 (GIS), WP3.3 (IoT) |

## 2. New graph content (this phase)
- **Findings:** `F-0022`–`F-0046` (25 findings), each `DERIVED_FROM` its evidence source.
- **Contradiction edges:** internet penetration (`F-0038`: DataReportal 31.2% `CONTRADICTS` ZICTA 64.1%); population (`F-0026`: de facto 19,610,769 `CONTRADICTS` de jure 19,693,423).
- **Entities:** reuses Phase-1 `LOC-ZM` / provinces; new domain-entity instances (ZESCO, BoZ, ZICTA, corridors, basins) are noted here and will be instantiated with IDs as WP2+ deepens each domain (to avoid premature over-modelling).

## 3. Constraint respected
No software/database/API requirements created. Only traceable knowledge registered (ROM Phase 4). Requirement extraction (RTM) deferred to later work packages.
