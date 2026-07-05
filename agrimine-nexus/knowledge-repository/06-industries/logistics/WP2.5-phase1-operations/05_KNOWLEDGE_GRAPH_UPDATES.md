---
id: WP2.5-P1-KG
title: Knowledge Graph Updates — WP2.5 Logistics
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research (logistics layer)
work_package: WP2.5
industry: TAX-IND.5 (Logistics & Supply Chains)
topic: Knowledge extraction
keywords: [knowledge-graph, logistics, entities, cross-industry-links]
summary: Output 14. Logistics entities, findings, and cross-industry links added to the knowledge graph. No software design.
source: derived
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 80
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
related_workflows: [WF-L01..WF-L26]
---

# Knowledge Graph Updates — WP2.5 Logistics (Output 14)

## Added to the graph
- **Logistics entities (11+ requested classes):** `ENT-CORRIDOR`, `ENT-BORDERPOST`, `ENT-VEHICLE-FLEET`, `ENT-ROUTE-L`, `ENT-WAREHOUSE-L`, `ENT-SHIPMENT`, `ENT-DELIVERY`, `ENT-CFAGENT`, `ENT-SEZ`, `ENT-CUSTOMS-DECL` (+ reuse `ENT-COMMODITY`, `ENT-WRECEIPT`, `ENT-BUYER-FRA`) — covering logistics, fleet, warehouse, vehicle, route, border, supplier, distribution, storage, shipment, delivery.
- **Findings:** `F-0067`–`F-0072` (corridors/rail, SEZ/dry-port/fuel, customs, cross-border, trucking operators, FRA/fertilizer distribution) with `DERIVED_FROM` edges.
- **Workflows:** `WF-L01`–`WF-L26` (documented in the Workflow Library), each linked upstream/downstream to industry workflows.

## Cross-industry links (edges `E-0122`–`E-0131`)
- Shipment `PART_OF` Corridor / crosses Border Post; carries Commodity.
- Vehicle `PART_OF` Route; Delivery `PART_OF` Warehouse.
- Warehouse `PRODUCES` Warehouse Receipt (links WF-026 agriculture).
- Corridor `CONSUMES` (carries) Mine exports (WF-M13) and Construction materials (WF-C08).
- Shipment (hazmat/waste) `GOVERNED_BY` ZEMA/EIA (WF-E09 / WF-L23).
- Customs Declaration `OWNED_BY` Clearing & Forwarding Agent.

## Effect
The knowledge graph now contains a **logistics layer that connects Agriculture, Mining, Construction, and Environmental workflows** through shared corridors, borders, fleet, warehouses, shipments, and customs — completing the operational model across all target industries.

## Constraint respected
Entities/edges are knowledge modelling only — **no database schema, ERD, UML, API, or software requirements**.
