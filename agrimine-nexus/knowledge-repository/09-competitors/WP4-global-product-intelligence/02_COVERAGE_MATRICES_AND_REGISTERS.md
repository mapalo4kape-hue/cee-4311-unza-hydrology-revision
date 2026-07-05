---
id: WP4-MATRICES
title: Product Coverage Matrices & Registers (WP4)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 4 — Product & Competitor Research
work_package: WP4.1
industry: cross-industry
topic: Product coverage matrices & registers
keywords: [feature matrix, workflow coverage, stakeholder coverage, technology adoption, integration, pricing, deployment, gaps]
summary: Outputs 3-11. Category-level coverage matrices and registers mapped to documented WF-/STK-/REG-/TECH- IDs. Evidence-first; no recommendations, no requirements, no subjective ranking.
source: SRC-0071;SRC-0075;SRC-0076;SRC-0079;SRC-0080;SRC-0084;SRC-0086;SRC-0114;SRC-0115;SRC-0116;SRC-0117
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 70
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_GLOBAL_COMPETITOR_CATALOGUE.csv, 01_MARKET_ANALYSIS_ZAMBIA_SOUTHERN_AFRICA.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Product Coverage Matrices & Registers (Outputs 3–11)

> The **Global Product Catalogue** (`01_GLOBAL_COMPETITOR_CATALOGUE.csv`, `CMP-0001`–`CMP-0248`) is the per-product record with ~19 captured attributes. Matrices below are **category-level views** (per-product cells are in the CSV's `mobile/offline/gis/ai/iot/drone/api` columns). Mappings use IDs from prior WPs.

## Output 3 — Product Feature Matrix (category-level capability summary)
| Category | Mobile | Offline | GIS | AI | IoT | API | Representative products |
|----------|--------|---------|-----|----|----|-----|-------------------------|
| African agri advisory/marketplace | ●●● | ●● | ● | ●● | ○ | ●● | CMP-0001/0002/0009/0010/0012 |
| Farm mgmt / precision ag (global) | ●● | ● | ●●● | ●●● | ●● | ●●● | CMP-0013/0134/0135/0143 |
| Mine planning/geology | ○ | ●●● | ●●● | ● | ○ | ●● | CMP-0154..0162 |
| Mine fleet/telemetry | ●●● | ● | ●● | ●● | ●●● | ●●● | CMP-0163..0166 |
| CMMS/EAM | ●●● | ● | ○ | ● | ●● | ●●● | CMP-0167..0171 |
| EHS/ESG/carbon | ●● | ○ | ● | ●● | ● | ●●● | CMP-0172..0187 |
| LIMS/environmental data | ●● | ● | ●● | ● | ●● | ●●● | CMP-0177..0183 |
| Construction PM/BIM | ●●● | ●● | ●● | ● | ○ | ●●● | CMP-0188..0203 |
| Logistics WMS/TMS/visibility | ●●● | ● | ●● | ●● | ●● | ●●● | CMP-0204..0221 |
| Fleet telematics | ●●● | ● | ●●● | ●● | ●●● | ●●● | CMP-0211..0216 |
| Enterprise ERP/CRM/HR/low-code | ●●● | ● | ○ | ●● | ● | ●●● | CMP-0222..0240 |
> ●●● strong / ●● common / ● partial / ○ rare (category-level, from catalogue evidence).

## Output 4 — Workflow Coverage Matrix (product category → documented workflows)
| Product category | Workflows covered |
|------------------|-------------------|
| Agri advisory/marketplace | WF-013/019/029/038 (scouting/weather/sales/extension) |
| Farm ERP / precision | WF-003/012/014/024/025/033 (mapping/irrigation/monitoring/records) |
| Mine planning/geology | WF-M03 mine planning, exploration/survey workflows |
| Mine fleet/telemetry | WF-M haulage/production; equipment telemetry |
| CMMS/EAM | maintenance workflows (mining/ag/logistics assets) |
| EHS/ESG/LIMS | WF-E10/E11 monitoring, safety, EIA/lab workflows |
| Construction PM/BIM/QS | WF-C03/C07/C08/C12 (BOQ/progress/delivery/valuation) |
| Logistics WMS/TMS | WF-L08/L11/L12/L17-L20 (fleet/haulage/warehouse) |
| Enterprise ERP/finance | WF-006/032 finance, procurement, reporting WF-035 |

## Output 5 — Stakeholder Coverage Matrix (category → stakeholder groups served)
| Product category | Stakeholders (STK) |
|------------------|--------------------|
| Agri advisory/marketplace | farmers (STK-028), agro-dealers (STK-032), cooperatives (STK-031) |
| Farm ERP/precision | commercial farmers (STK-029), agronomists (STK-034) |
| Mine planning/fleet/EAM | mines (STK-039), mine engineers/geologists, contractors (STK-041) |
| Construction PM/BIM/QS | contractors (STK-048), consultants/QS (STK-050), engineers |
| Logistics WMS/TMS/telematics | fleet operators (STK-055), transporters, warehouse operators |
| EHS/ESG/LIMS | ZEMA (STK-010), labs, HSE managers |
| Enterprise ERP/CRM/HR | enterprises across all industries, finance/HR functions |

## Output 6 — Technology Adoption Matrix (category → WP3 technologies)
| Product category | Technologies (TECH) |
|------------------|---------------------|
| Agri advisory | LLM/chatbot (TECH-001..007), USSD/SMS (TECH-150), mobile money |
| Precision ag / drone | GIS (TECH-047..059), RS/NDVI (TECH-060..071), drone mapping (TECH-073..082), IoT (TECH-084..104) |
| Mine planning | GIS/3D (TECH-047..059), optimisation (TECH-029/030) |
| Mine fleet / telematics | GPS/telematics (TECH-101/104), IoT connectivity (TECH-084..088) |
| Logistics | routing (TECH-058), GPS (TECH-101), RFID/BLE (TECH-102) |
| EHS/ESG/LIMS | analytics (TECH-024..028), search/BI (TECH-121..124) |
| Enterprise | databases (TECH-130..132), BI (TECH-123/124), workflow (TECH-113..116), IAM (TECH-136..149) |

## Output 7 — Integration Capability Matrix (category-level)
| Category | Typical integrations |
|----------|----------------------|
| Enterprise ERP | banking/payments, tax (ZRA), payroll, BI, e-commerce |
| Logistics WMS/TMS | ERP, carriers, customs (ASYCUDA), telematics, e-commerce |
| Mining suites | LIMS/assay, fleet, survey instruments, ERP/EAM |
| Construction | BIM (IFC), accounting/cost, document control, scheduling |
| Agri platforms | mobile money, weather/satellite APIs, market-price feeds |
> API presence per product in CSV `api` column; open standards noted where evidenced (IFC for BIM, OGC for GIS).

## Output 8 — Pricing Model Register
| Model | Typical categories | Examples |
|-------|--------------------|----------|
| Subscription/SaaS | most cloud enterprise/agri/logistics | Procore, Odoo, Samsara |
| Perpetual licence | mining/BIM desktop suites | Vulcan, Datamine, Revit |
| Freemium | African agri, inspections | AgriPredict, SafetyCulture, MaintainX |
| Transaction/commission | fintech, marketplaces, logistics | Zoona, Musanga, Kobo360 |
| PAYGO | rural distribution | VITALITE |
| Credit/margin | agri-fintech | Apollo, ThriveAgric, Lupiya |
| Government-funded | e-gov systems | ZIAMIS, Smart Zambia |
| Open-source (free/support) | OSS | ERPNext, SENAITE, OpenBoxes, Budibase, OpenProject |

## Output 9 — Deployment Model Register
| Model | Count tendency | Notes |
|-------|----------------|-------|
| Cloud / SaaS | majority | dominant for new products; connectivity-dependent |
| On-prem / desktop | mining/BIM/large ERP | Vulcan, Datamine, SAP on-prem |
| Mobile / USSD | African smallholder/fintech | offline-relevant |
| IoT/edge + cloud | telematics/precision ag | Samsara, Solinftec, Semios |
| Self-host (OSS) | OSS stack | ERPNext, SENAITE, OpenBoxes |

## Output 10 — Strength–Weakness Register (category-level, evidence-based)
| Category | Documented strengths | Documented weaknesses/limitations |
|----------|----------------------|-----------------------------------|
| Global Tier-1 (SAP/Oracle/Manhattan) | depth, integration, compliance | cost, complexity, connectivity/skills barriers in Zambia |
| Mining suites | mature 3D/scheduling | require multiple vendors; desktop; costly; limited mobile/offline-field |
| African agri-tech | mobile/USSD reach, local fit | narrow scope, funding-dependent, thin GIS/offline |
| OSS enterprise | affordable, self-host, offline | need in-house skills; support burden |
| Fintech | payment rails, reach | narrow (payments), regulatory dependence |
| Construction PM/BIM | collaboration, field docs | connectivity/device needs; licence cost |

## Output 11 — Market Gap Register (`GAP-M01`–`GAP-M08`)
| Gap ID | Gap | Notes |
|--------|-----|-------|
| GAP-M01 | Several African/Zambian product entries known-but-unverified (verification=K) | confirm founding/status/capabilities |
| GAP-M02 | Quantity floors not fully met: 248 products (vs 300), ~150 commercial, ~15 OSS (vs 50), ~50 African, ~20 Zambian | expansion follow-on |
| GAP-M03 | Government product identities beyond ZIAMIS/Smart Zambia unconfirmed | verify TaxOnline/ASYCUDA/cadastre as products |
| GAP-M04 | NGO/donor platform identities under-evidenced | verify |
| GAP-M05 | University-developed systems (UNZA/CBU) not evidenced | research |
| GAP-M06 | Exact pricing points not captured (model-level only) | vendor pricing pages |
| GAP-M07 | Per-product customer feedback/awards/certifications sparsely captured | analyst reports/case studies |
| GAP-M08 | Unsolved-pain-point mapping is category-level, not per-product | deeper reverse-engineering |

## Cross-cutting note (special analysis)
For each **category** we have mapped supported workflows, stakeholders served, technologies used, and (from ACT-011 `03_UX_PATTERNS_PAINPOINTS_GAPS.md`) pain points addressed vs. left unsolved. Per-product depth for all 248 items is **not** complete this pass (`GAP-M08`). No capability asserted without a catalogue evidence source; unverified items marked `K`.
