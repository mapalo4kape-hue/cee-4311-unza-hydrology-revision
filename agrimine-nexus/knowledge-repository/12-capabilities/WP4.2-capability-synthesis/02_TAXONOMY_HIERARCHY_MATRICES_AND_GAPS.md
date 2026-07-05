---
id: WP4.2-TAXONOMY
title: Capability Taxonomy, Hierarchy, Matrices, Maturity & Gaps (WP4.2)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 4 — Product & Competitor Research
work_package: WP4.2
industry: cross-industry
topic: Enterprise capability synthesis
keywords: [capability, taxonomy, hierarchy, traceability, maturity, cross-industry]
summary: Outputs 2-12. Capability taxonomy/hierarchy, traceability matrices, maturity matrix, gap register, and cross-industry analysis. Synthesis of prior evidence only. No software design, features, prioritisation, requirements, or architecture.
source: F-0053;F-0056;F-0060;F-0067;F-0079;F-0085
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 70
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_MASTER_ENTERPRISE_CAPABILITY_CATALOGUE.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Capability Taxonomy, Hierarchy, Matrices, Maturity & Gaps (Outputs 2–12)

> Synthesis of previously collected evidence into a normalised, hierarchical **Enterprise Capability Model**. Every capability in `01_MASTER_ENTERPRISE_CAPABILITY_CATALOGUE.csv` (`CAP-001`–`CAP-170`) traces to supporting IDs (`WF-/STK-/REG-/TECH-/CMP-/INT-/F-`) — **no orphan capabilities**. This is **not** software design, feature recommendation, prioritisation, requirements, or architecture.

## Output 2 — Capability Taxonomy (controlled classification)
- **L1 Domain** (7): Agriculture, Mining, Construction, Environmental, Logistics, Enterprise (cross-industry).
- **L2 Capability Group** (examples): Farm Operations, Crop Management, Irrigation, Warehousing, Commodity Trading, Marketplace, Finance, Insurance, Livestock/Poultry/Aquaculture, Extension, Cooperatives (Agriculture); Exploration, Survey, Mine Planning, Fleet, Equipment, Asset Management, Safety, Environmental, Contractor Management, Laboratory, Inventory, Procurement (Mining); Project Planning, BOQ, Scheduling, Procurement, Site Operations, Equipment, Workforce, QA/QC, HSE, Document Control (Construction); EIA, Monitoring, Water, Waste, ESG, Carbon, Laboratory, Reporting (Environmental); Transport, Fleet, Warehouse, Route Planning, Cold Chain, Inventory, Dispatch (Logistics); Finance, HR, CRM, Procurement, Inventory, Document Management, Analytics, Reporting, Notifications, Workflow Automation, Audit, Compliance, Identity (Enterprise).
- **L3 Capability** = the catalogue rows (`CAP-*`).

## Output 3 — Capability Hierarchy (L1 → L2 → L3 counts)
| L1 Domain | Capabilities | L2 groups |
|-----------|--------------|-----------|
| Agriculture | 40 (`CAP-001..040`) | 12 groups |
| Mining | 27 (`CAP-041..067`) | 11 groups |
| Construction | 21 (`CAP-068..088`) | 9 groups |
| Environmental | 13 (`CAP-089..101`) | 7 groups |
| Logistics | 19 (`CAP-102..120`) | 7 groups |
| Enterprise (cross-industry) | 50 (`CAP-121..170`) | 13 groups |
| **Total** | **170** | — |

## Output 4 — Workflow-to-Capability Matrix
Every capability lists its `workflows` column (WF IDs). Coverage highlights: agriculture WF-001..041 map to `CAP-001..040`; mining WF-M01..M11 to `CAP-041..067`; construction WF-C01..C14 to `CAP-068..088`; environmental WF-E01..E14 to `CAP-089..101`; logistics WF-L01..L26 to `CAP-102..120`; cross-cutting WF-006/032/033/034/035/037/038 to enterprise `CAP-121..170`. No capability lacks a workflow reference.

## Output 5 — Stakeholder-to-Capability Matrix
Each capability lists `stakeholders` (STK IDs). Dominant links: farmers STK-028 (agri capabilities); mines STK-039 + engineers/geologists STK-047 (mining); contractors STK-048 + QS STK-050 (construction); ZEMA STK-010 (environmental); fleet operators STK-055 (logistics); finance/HR/IT functions STK-029/058/070 and regulators STK-022/023 (enterprise).

## Output 6 — Regulation-to-Capability Matrix
Regulated capabilities carry `regulations` (REG IDs). Key mappings: Data Protection Act REG-0024 → identity/audit/document/consent (`CAP-143/153/156/157/170`); Mines Act REG-0009 → mining planning/licence (`CAP-041/044/046/066`); EMA REG-0017/18 → environmental monitoring/reporting (`CAP-089..099`); OHS REG-0034 → safety/HSE (`CAP-057/059/085`); tax REG-0026/27/28 → finance/tax (`CAP-121/128`); procurement REG-0029 → procurement (`CAP-055/071/131`).

## Output 7 — Technology-to-Capability Matrix
Each capability lists `technologies` (TECH IDs). Examples: computer vision TECH-015 → scouting/QA (`CAP-007/082`); GIS TECH-047 → mapping/planning (`CAP-002/046/162`); RS TECH-060 → yield/biodiversity (`CAP-013/095`); IoT TECH-084/098 → irrigation/monitoring (`CAP-009/060/092`); LLM/RAG TECH-001/033 → advisory (`CAP-023/168`); IAM TECH-136..139 → identity (`CAP-156..158`); offline-sync TECH-127/129 → offline capture/sync (`CAP-160/161`).

## Output 8 — Competitor Coverage Matrix
Each capability lists `competitors` (CMP IDs) that demonstrably support it in the market — evidence that the capability **exists** (not an endorsement). Coverage is dense for enterprise/agri/logistics/construction and (desktop-bound) for mining/environmental. Thinly-covered capabilities are flagged in the gap register.

## Output 9 — Integration Dependency Matrix
Each capability lists `integrations` (INT IDs) it depends on. Examples: payments (`CAP-124/125/039`) → INT-003/004/006; government submissions (`CAP-066/098`) → INT-030/035; comms (`CAP-149/169`) → INT-091/092/102; identity (`CAP-156..159`) → INT-105/108/115; spatial (`CAP-162`) → INT-057/058.

## Output 10 — Capability Maturity Matrix (market maturity)
| Maturity | Meaning | Example capabilities |
|----------|---------|----------------------|
| Commodity | Ubiquitous, well-served across vendors | GL/AP/AR (`CAP-121-123`), payroll (`CAP-129`), identity (`CAP-156`), notifications (`CAP-149`) |
| Established | Mature, multiple proven products | mine planning (`CAP-046`), BOQ (`CAP-069`), fleet mgmt (`CAP-106`), ECM (`CAP-143`) |
| Growing | Rising adoption, less standardised | AI advisory (`CAP-023`), progress-tracking from drone (`CAP-075`), cold-chain (`CAP-115`), data sync (`CAP-161`) |
| Emerging | Early, sparse evidence | irrigation automation (`CAP-010`), index insurance (`CAP-029`), carbon accounting (`CAP-097`) |

## Output 11 — Capability Gap Register (`GAP-C01`–`GAP-C08`)
| Gap ID | Gap | Notes |
|--------|-----|-------|
| GAP-C01 | Quantity floor not met: 170 normalised capabilities vs. ≥500 target (and per-industry targets) | after merging duplicates/normalising terminology, 170 distinct capabilities at a consistent L3 grain; further decomposition risks artificial inflation |
| GAP-C02 | Livestock/poultry/aquaculture capabilities under-evidenced (thin workflow/product evidence) | `CAP-030..036` low confidence |
| GAP-C03 | Emerging capabilities (irrigation automation, index insurance, carbon) have sparse market/Zambia evidence | `CAP-010/029/097` |
| GAP-C04 | Per-capability KPIs, inputs/outputs, and documents/assets captured at description level only (not itemised) | full attribute set deferred |
| GAP-C05 | Competitor coverage is category/product-level, not verified per capability per product | ties to `GAP-M08` |
| GAP-C06 | Some capabilities depend on integrations flagged uncertain (gov/bank APIs) | ties to `GAP-I01..I04` |
| GAP-C07 | Remaining-pain-point mapping per capability is qualitative | see cross-industry analysis |
| GAP-C08 | Environmental laboratory & waste capabilities thinly evidenced locally | `CAP-094/100` |

## Output 12 — Cross-Industry Capability Analysis
- **~30% of capabilities are cross-industry (enterprise) commons** (`CAP-121..170`) reused by all sectors: finance, HR, procurement, inventory, document management, analytics, notifications, workflow, audit, compliance, identity, offline capture/sync, geospatial mapping.
- **Shared operational patterns** recur across industries: asset/equipment management (mining `CAP-052/053` ≈ construction `CAP-080` ≈ logistics `CAP-106`); safety/HSE (mining `CAP-057-059` ≈ construction `CAP-085`); monitoring (mining env `CAP-060/061` ≈ environmental `CAP-091/092`); inventory/warehousing (agri `CAP-015` ≈ logistics `CAP-112/113` ≈ mining `CAP-054`).
- **Offline-first, mobile/USSD, mobile-money, and geospatial** are the cross-cutting Zambia-relevant enablers (`CAP-125/149/160/161/162/169`) — consistent with WP3 (`F-0078`) and WP4.3 (`F-0086`) findings.
- **Highest market maturity** is in enterprise commons; **lowest** in emerging agri-fintech/insurance and environmental carbon — signalling where the market (not AgriMine) is least served (documented, not prioritised).

## Recorded uncertainties
Capabilities describe **what exists in the market**, traced to evidence. No capability was invented; where evidence is thin, confidence is lowered and the gap is registered. No prioritisation, feature design, or requirements are expressed.
