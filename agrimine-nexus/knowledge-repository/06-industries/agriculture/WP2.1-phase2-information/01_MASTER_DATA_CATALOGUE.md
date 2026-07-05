---
id: WP2.1-P2-MDC
title: Master Data Catalogue — Zambian Agriculture (WP2.1 Phase 2)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Master data
keywords: [master-data, records, farmer-registry, information-ecosystem]
summary: Catalogue of master records used across Zambian agricultural workflows and the information each carries. Information intelligence only — no database schemas, tables, types, or keys.
source: SRC-0045;SRC-0046;SRC-0058;SRC-0059;SRC-0060;SRC-0061;SRC-0063
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 82
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../WP2.1-phase1-operations/01_AGRICULTURAL_WORKFLOW_LIBRARY.md]
related_requirements: []
related_entities: [ENT-FARMER, ENT-FARM]
related_apis: []
related_modules: []
related_workflows: []
---

# Master Data Catalogue — Zambian Agriculture

> Master records and the **business information** each holds (not schemas/tables/keys). Where a record's content is evidenced (e.g., FISP/ZIAMIS farmer registry, warehouse receipt), it is cited; otherwise the information elements are consultant synthesis of the ACT-008 workflows.

## 1. Records grounded in evidence

- **Farmer** (`MD-01`): the farmer master record in the **ZIAMIS universal farmer register** — holds **biographical data, contact details, farming activities, and NRC linkage**, with a **unique digital ID** per farmer [SRC-0058] (AfJARE, pub. 2023; confidence 80/100; retrieved 2026-07-05); register covers ~**4.3M** verified/traceable farmers [SRC-0063] (agribusinesszambia/FAO, pub. 2024; confidence 70/100; retrieved 2026-07-05). Geodata (farm maps/location) recommended but not yet standard [SRC-0060] (FAO, pub. 2022; confidence 80/100; retrieved 2026-07-05). Owner: **Ministry of Agriculture / ZIAMIS**.
- **Agro-dealer** (`MD-10`): accredited-dealer record in ZIAMIS (product list, recommended prices, accreditation, location); ~779 accredited, unique vendor digital ID [SRC-0046][SRC-0063]. Owner: MoA/ZIAMIS.
- **Input Product** (`MD-15`): product record submitted by suppliers/dealers to ZIAMIS (product, recommended price) [SRC-0058]. Owner: supplier/MoA.
- **Warehouse Receipt master terms** (`MD-27` linked): a certified **warehouse** issues receipts carrying operator name, location, issue date, serial number, delivery terms, commodity description, storage/handling rate, signature, net weight + grading, negotiable/non-negotiable [SRC-0061] (Agricultural Credits Act No.35/2010; confidence 88/100; retrieved 2026-07-05). Owner: warehouse operator; registry via Collateral Registry [SRC-0062].
- **Cooperative** (`MD-06`): group record (membership, digital ID) — FISP requires group/cooperative membership [SRC-0045]; unique digital ID [SRC-0063]. Owner: cooperative / MoA.

## 2. Master record catalogue (all)

| ID | Master record | Definition | Key information held (business) | Owner | Source workflow(s) |
|----|---------------|-----------|--------------------------------|-------|--------------------|
| MD-01 | Farmer | Individual producer | bio, contact, NRC link, activities, digital ID [SRC-0058] | MoA/ZIAMIS | WF-007,038 |
| MD-02 | Farm | Production holding | name, tenure, location, size | Farmer | WF-001,003 |
| MD-03 | Field | Cultivated unit within farm | area, location, crop history | Farmer | WF-003,011 |
| MD-04 | Block | Extension administrative unit | block name, camps, officer | MoA | WF-038 |
| MD-05 | Camp | Sub-block extension unit | camp name, zones, CEO | MoA | WF-038 |
| MD-06 | Cooperative | Farmer group | members, digital ID, office-bearers [SRC-0063] | Cooperative | WF-007,031 |
| MD-07 | Household | Family unit | members, head, residence | Farmer/ZamStats | WF-020,032 |
| MD-08 | Employee/Worker | Farm labour | name, role, terms | Farmer/manager | WF-020 |
| MD-09 | Supplier | Input manufacturer/importer | name, products, prices | Supplier/MoA | WF-007,008 |
| MD-10 | Agro-dealer | Accredited input retailer | accreditation, products, prices, location [SRC-0046] | MoA/ZIAMIS | WF-007,008 |
| MD-11 | Buyer | Produce purchaser (incl. FRA) | name, type, terms | Buyer | WF-029 |
| MD-12 | Transporter | Haulage provider | name, vehicles, routes | Transporter | WF-028 |
| MD-13 | Warehouse | Storage facility (certified) | operator, location, capacity, certification [SRC-0061] | Operator | WF-026 |
| MD-14 | Equipment | Machinery/implement | type, model, hours | Owner/provider | WF-021 |
| MD-15 | Input Product | Seed/fertilizer/chemical item | product, price, spec [SRC-0058] | Supplier | WF-007,008,009 |
| MD-16 | Seed Variety | Crop variety | variety, traits, source | Supplier/researcher | WF-007 |
| MD-17 | Fertilizer | Fertilizer type | grade (e.g. D/Urea), rate | Supplier | WF-008 |
| MD-18 | Chemical | Agrochemical | active ingredient, dosage, safety | Supplier | WF-009 |
| MD-19 | Livestock | Animals | species, count, health | Farmer | WF-— (livestock context) |
| MD-20 | Customer | Downstream purchaser | name, terms | Farmer/agribusiness | WF-029 |
| MD-21 | Financial Institution | Bank/MFI/MMO | name, products | FI/BoZ | WF-032,037 |
| MD-22 | Government Agency | MoA/FRA/ZamStats etc. | name, mandate | GRZ | WF-034,035,040 |
| MD-23 | Extension Officer | CEO/BEO | name, camp/block, specialisation | MoA | WF-038 |
| MD-24 | Laboratory | Soil/quality lab | name, tests, accreditation | Lab | WF-004 |
| MD-25 | Location | Geographic point/place | name, coordinates | multiple | WF-003 |
| MD-26 | Administrative Area | Province/district/ward | code, name, parent | GRZ (WP1.1) | all |
| MD-27 | Growing Season | Season reference | season year, dates | MoA | all (season anchor) |
| MD-28 | Commodity | Traded produce | commodity, grade | Farmer/ZAMACE | WF-029,031 |
| MD-29 | Storage Facility | On-farm/community/warehouse store | type, capacity, location | Farmer/operator | WF-026 |
| MD-30 | Contract (outgrower) | Farmer-agribusiness agreement | parties, terms, input credit, buyback [SRC-0055] | Agribusiness | WF-030 |
| MD-31 | FISP e-Voucher | Farmer input entitlement | code, allocation, validity, redemption [SRC-0045] | MoA/ZIAMIS | WF-007,008 |

## 3. Notes
- The **farmer, agro-dealer, cooperative, and voucher** master records already exist in a **live digital registry (ZIAMIS)**; most other records (farm, field, equipment, contract) are held on **paper/verbally** at operator level (ACT-008).
- No schema, table, key, or type is defined — this is an information inventory only (per phase scope).
