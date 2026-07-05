---
id: WP4.1-MATRICES
title: Competitor Comparison Matrices — Feature / Pricing / Technology / Integration (D2-D5)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 4 — Product & Competitor Research
work_package: WP4.1
industry: cross-industry
topic: Competitor comparison
keywords: [feature-matrix, pricing, technology, integration, competitors]
summary: Deliverables 2-5. Detailed attribute capture for representative category leaders. Evidence-first; no solution/product design or AgriMine Nexus design.
source: SRC-0074;SRC-0078;SRC-0079;SRC-0080;SRC-0081;SRC-0086
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 76
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_GLOBAL_COMPETITOR_CATALOGUE.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Competitor Comparison Matrices (D2–D5)

> Representative leaders per domain, with the ACT-011 attribute set. Values are vendor-reported/review-sourced and marked by confidence; `?` = unverified. **No solution design; landscape only.**

## D2 — Feature Comparison Matrix (workflow coverage & capabilities)
Legend: Y yes · P partial · N no · ? unknown.

| Product | Domain | Core modules | Mobile | Offline | GIS | AI | IoT | Drone | Reporting | Dashboards |
|---------|--------|--------------|--------|---------|-----|----|----|-------|-----------|------------|
| Apollo Agriculture | Agri-fintech | inputs, credit, insurance, advisory | Y | P | P | Y | N | N | P | P |
| Cropin | Farm mgmt | crop mgmt, monitoring, supply chain, analytics | Y | Y | Y | Y | P | N | Y | Y |
| John Deere Ops Center | Precision ag | machine data, agronomy, work planning | Y | Y | Y | Y | Y | N | Y | Y |
| AGRIVI | Farm mgmt | planning, tasks, agronomy, analytics | Y | Y | Y | Y | P | N | Y | Y |
| Maptek Vulcan | Mine planning | geology, block model, design, scheduling | N | Y | Y | P | N | N | Y | P |
| Hexagon Mining | Mining suite | planning, FMS, safety, survey | Y | Y | Y | Y | Y | N | Y | Y |
| Procore | Construction PM | project, quality, safety, financials, field | Y | Y | P | Y | N | N | Y | Y |
| Autodesk ACC/Forma | Construction+BIM | design, docs, build, cost, model coord | Y | Y | P | Y | N | Y | Y | Y |
| Cority | EHS | health, safety, IH, environment, analytics | Y | P | P | Y | P | N | Y | Y |
| Esri ArcGIS | GIS | mapping, imagery, spatial analysis, IoT (Velocity) | Y | Y | Y | Y | Y | Y | Y | Y |
| DroneDeploy | Drone | flight, mapping, 3D, site AI, robotics | Y | P | Y | Y | Y | Y | Y | Y |
| IBM Maximo | EAM | assets, maintenance, work orders, IoT | Y | Y | P | Y | Y | N | Y | Y |
| SAP S/4HANA | ERP | finance, SCM, procurement, manufacturing | Y | N | P | Y | Y | N | Y | Y |
| ZAMACE | Commodity | trading, WRS, clearing, market data | Y | N | N | N | N | N | Y | P |
| M-Pesa/Airtel Money | Mobile money | wallet, P2P, merchant, bill pay | Y | Y | N | N | N | N | P | N |

**Observation:** No single product spans agriculture + mining + construction + environmental with shared GIS/IoT/offline; coverage is **domain-siloed**.

## D3 — Pricing Comparison Matrix
| Product | Model | Indicative level | Notes |
|---------|-------|------------------|-------|
| Procore | Volume-based, unlimited users | ~0.1–0.2% of construction volume | predictable annual [SRC-0078][SRC-0079] |
| Autodesk ACC/Forma | Per-user / bundle | ~$50–140/user/mo range | ecosystem bundles [SRC-0079] |
| Buildertrend | Flat-rate per company | ~$199–1,099/mo tiers | residential [SRC-0079] |
| Cority/Enablon/Intelex/Sphera | Enterprise custom quote | ~$30k–$100k+/yr; 6–18 mo impl. | EHS enterprise [SRC-0080] |
| Apollo Agriculture | Margin on inputs + credit | farmer pays via credit/cash | bundled [SRC-0074] |
| eMsika FarmHouse | Subscription | ~ZMW149 (~$5.64) tier | Zambia SME [SRC-0072] |
| Esri ArcGIS | License / named-user + enterprise | tiered; enterprise agreements | [SRC-0081] |
| Mine-planning (Maptek/Deswik/Datamine) | Perpetual/subscription license | high (enterprise) | [SRC-0077] |
| Mobile money | Per-transaction fee | small % / tiered | [SRC-0084] |
| Flutterwave | Per-transaction | % + fixed | 35+ countries [SRC-0085] |

**Observation:** enterprise domain software (mining, EHS, construction ERP) is **high-cost, long-implementation**; African smallholder tools are **freemium/USSD/low-cost** — a large affordability gap.

## D4 — Technology Comparison Matrix
| Product | Deployment | Architecture signal | Offline | Mobile-first | Open API |
|---------|-----------|---------------------|---------|--------------|----------|
| ArcGIS | Cloud + on-prem (Enterprise) | platform + extensions | Y | P | Y |
| QGIS | Desktop (OSS) | open-source, plugin-based | Y | P | Y |
| Procore | Cloud (SaaS) | cloud platform + 400+ integrations | Y | Y | Y |
| Autodesk ACC | Cloud (SaaS) | design-to-field, 400+ integrations | Y | Y | Y |
| SAP S/4HANA | Cloud + on-prem | enterprise suite | N | P | Y |
| Odoo | Cloud + on-prem | modular open-core | P | P | Y |
| ThingsBoard | Cloud/on-prem (OSS) | IoT rules engine | P | Y | Y |
| Apollo/African agri | Cloud + USSD/SMS | mobile/USSD-first, low-bandwidth | P | Y | P |
| M-Pesa/Airtel | USSD + app + API | telco-grade, offline USSD | Y | Y | Y |
| ZIAMIS (Zambia gov, ref) | Cloud + mobile + SMS | national registry rail | P | Y | P |

**Observation:** **offline-first + USSD/low-bandwidth** is common in African tools but rare in global enterprise suites; **open APIs** are widespread among leaders (integration-ready).

## D5 — Integration Comparison Matrix
| Product | Integrates with | Integration style |
|---------|-----------------|-------------------|
| Procore | ERP (Sage, Viewpoint, CMiC), Primavera, 400+ marketplace | prebuilt connectors + API |
| Autodesk ACC | Revit/AutoCAD/Navisworks, ERP/CRM, 400+ | ecosystem + API |
| Esri ArcGIS | IoT platforms, SAP, imagery providers, Velocity feeds | connectors + REST + extensions |
| Hexagon Mining | mixed OEM fleets, SCADA/PLC, ERP | interoperability focus |
| IBM Maximo | ERP, SCADA, IoT, GIS | enterprise integration |
| Flutterwave/aggregators | Airtel/MTN/Zamtel MoMo, cards, banks | unified payments API [SRC-0085] |
| ZAMACE | banking settlement, FIX market data, CSD, Collateral Registry | exchange integrations [SRC-0082] |
| Apollo/DigiFarm | agro-dealers, M-Pesa/mobile money, insurers | platform partnerships |

**Observation:** Zambian rails to integrate with recur across the landscape — **mobile money (Airtel/MTN/Zamtel), ZIAMIS, Mining Cadastre, ZPPA e-GP, My-WARMA/ZEMA, ZAMACE/Collateral Registry** (from WP2.x) — none unified today.
