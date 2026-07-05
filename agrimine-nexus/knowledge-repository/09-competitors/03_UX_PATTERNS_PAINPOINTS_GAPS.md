---
id: WP4.1-UX-PAIN-GAP
title: UX Pattern Catalogue, Customer Pain Point Register & Feature Gap Analysis (D6-D8)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 4 — Product & Competitor Research
work_package: WP4.1
industry: cross-industry
topic: UX / pain points / gaps
keywords: [ux, pain-points, feature-gaps, reviews]
summary: Deliverables 6-8. UX patterns observed across competitor products, customer pain points from reviews, and evidence-backed feature gaps. Landscape/gap identification only — no solutions.
source: SRC-0078;SRC-0079;SRC-0080;SRC-0081;SRC-0084
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 74
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_GLOBAL_COMPETITOR_CATALOGUE.csv, 02_COMPARISON_MATRICES.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# UX Patterns, Customer Pain Points & Feature Gaps (D6–D8)

## D6 — UX Pattern Catalogue (observed patterns)
| Pattern | Where seen | Notes |
|---------|-----------|-------|
| **USSD / feature-phone menus** | Lima Links, AgriPredict, mobile money | reaches offline/low-literacy rural users |
| **Mobile-app + agent-assisted** | Apollo, DigiFarm, Copia | agent bridges digital gap |
| **SMS advisories/alerts** | Esoko, Ignitia, AgriPredict | push info to feature phones |
| **Cloud dashboards + role views** | Procore, ArcGIS, Cority | office/enterprise users |
| **Map-centric UI** | ArcGIS, DroneDeploy, Hexagon | spatial-first workflows |
| **Field-first task/checklist** | Fieldwire, MaintainX, Procore field | on-site simplicity |
| **Gantt/scheduling canvas** | Deswik, Primavera P6 | planning-heavy |
| **Wizard-based onboarding/registration** | ZIAMIS (gov), Apollo | guided data capture |
| **Wallet/transaction ledger** | M-Pesa, Airtel Money | simple balance + history |
| **Photo-diagnosis capture** | AgriPredict, Aerobotics, Taranis | image → AI result |
| **Offline sync + later upload** | John Deere, AGRIVI, Fieldwire | intermittent connectivity |
| **Marketplace listing + matching** | eMsika, Twiga, Khula, AFEX | buyer-seller connection |

## D7 — Customer Pain Point Register (from reviews/reports)
> Sourced from review platforms/reports (Capterra/G2/PeerSpot-class) and analyst commentary; treated as **user-reported signal** (Tier 3-4), corroborated where possible.

| ID | Pain point | Products commonly cited | Type |
|----|-----------|-------------------------|------|
| CP-01 | High cost / per-user pricing escalates with field teams | Autodesk ACC, enterprise EHS | Cost [SRC-0079][SRC-0080] |
| CP-02 | Long, costly implementation (6–18 months) | Enablon, Intelex, Sphera, ERP | Onboarding [SRC-0080] |
| CP-03 | Complexity / steep learning curve | ArcGIS, Primavera, mining suites | Usability [SRC-0081] |
| CP-04 | Poor offline / low-bandwidth performance | many global SaaS | Connectivity |
| CP-05 | Weak interoperability / data silos | FMS vs planning; ERP vs field | Integration [SRC-0076] |
| CP-06 | Limited localisation (language, currency, tax) | global suites in Africa | Localisation |
| CP-07 | Mobile app instability / limited functionality vs web | various (app-store reviews) | Mobile |
| CP-08 | Expensive add-on modules / hidden costs | construction & EHS suites | Pricing |
| CP-09 | Data lock-in / hard export | several SaaS | Portability |
| CP-10 | Smallholder tools shallow beyond advisory (no full ops) | African agri apps | Depth |
| CP-11 | Fragmented point solutions (many apps, no single view) | agri + logistics + finance | Fragmentation |
| CP-12 | Support/latency for non-Western time zones | global vendors | Support |

## D8 — Feature Gap Analysis (evidence-backed)
> Gaps = capabilities weakly served **for the Zambian/African productive-industry context**, inferred from the catalogue + WP2.x operations. Gaps, not solutions.

| Gap ID | Gap | Evidence basis |
|--------|-----|----------------|
| GAP-X01 | **Cross-industry** platform spanning agriculture+mining+construction+environmental (all are domain-siloed) | catalogue: no multi-industry product (D2) |
| GAP-X02 | **Offline-first + USSD** at enterprise depth (African tools offline but shallow; enterprise tools deep but online-only) | D2/D4 contrast |
| GAP-X03 | **Local integration fabric** (Airtel/MTN/Zamtel MoMo + ZIAMIS + Mining Cadastre + ZPPA + My-WARMA/ZEMA + ZAMACE/Collateral Registry) unified | D5; WP2.x |
| GAP-X04 | **Affordable enterprise-grade** tooling for Zambian mid-market (gap between $5 apps and $100k suites) | D3 pricing bimodality |
| GAP-X05 | **Compliance automation** for Zambian regulators (ZEMA EIA/audits, mine safety, NCC, WARMA) | WP2.x compliance burden |
| GAP-X06 | **Warehouse-receipt / commodity finance** integrated with field operations & registry | ZAMACE + FISP siloed |
| GAP-X07 | **Localised GIS baselayers + smallholder-scale precision** (global GIS complex; African tools thin on GIS) | D2 GIS column |
| GAP-X08 | **Shared master data** (farmer/asset/location/permit) across programs & sectors | WP2.x data duplication |
| GAP-X09 | **Multi-language / low-literacy UX** at operational depth | CP-06/CP-10 |
| GAP-X10 | **Field-to-finance traceability** (operations → payment → credit → insurance) end-to-end | CP-11 fragmentation |

**Note:** gaps are **evidence-backed observations of the market**, not recommendations. Translating any gap into AgriMine Nexus features/design is explicitly **out of scope** for ACT-011.
