---
id: WP4.3-REGISTERS
title: Integration Registers, Capability Matrix & Gaps (WP4.3)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 4 — Product & Competitor Research
work_package: WP4.3
industry: cross-industry
topic: Integration & digital ecosystem intelligence
keywords: [integration, API, government, financial, GIS, weather, IoT, communication, identity, ERP, standards]
summary: Outputs 2-15. Domain registers (catalogue views), API register, integration capability matrix, and integration gap register. Evidence collection only — no integration/architecture/API design, no vendor recommendations, no requirements.
source: SRC-0079;SRC-0081;SRC-0084;SRC-0110;SRC-0112;SRC-0118;SRC-0119;SRC-0120;SRC-0121
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 70
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_MASTER_INTEGRATION_CATALOGUE.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Integration Registers, Capability Matrix & Gaps (Outputs 2–15)

> The **Master Integration Catalogue** (`01_MASTER_INTEGRATION_CATALOGUE.csv`, `INT-001`–`INT-150`) is the per-entry record. Each row carries the required evidence fields: owner org, purpose, API availability, protocol style, auth method, licensing, geographic availability, Zambia applicability, documentation URL, evidence, confidence (publication/retrieval dates are in the Evidence Register). Registers below are **catalogue views by `domain`** — not duplicated.

## Register summaries (Outputs 2–13)
| Output | Register | Catalogue filter | Count |
|--------|----------|------------------|-------|
| 2 | API Register | api_available = Yes | ~95 entries expose APIs |
| 3 | Government Systems Register | domain = Government | 21 (`INT-025..045`) |
| 4 | Financial Integration Register | domain = Financial | 24 (`INT-001..024`) |
| 5 | GIS Integration Register | domain = GIS | 10 (`INT-056..065`) |
| 6 | Weather Integration Register | domain = Weather | 10 (`INT-046..055`) |
| 7 | Remote Sensing Register | domain = RemoteSensing | 8 (`INT-066..073`) |
| 8 | Drone Integration Register | domain = Drone | 6 (`INT-074..079`) |
| 9 | IoT Integration Register | domain = IoT | 11 (`INT-080..090`) |
| 10 | Communication Register | domain = Communication | 14 (`INT-091..104`) |
| 11 | Identity Register | domain = Identity | 11 (`INT-105..115`) |
| 12 | ERP Integration Register | domain = ERP | 10 (`INT-116..125`) |
| 13 | Data Exchange Standards Register | domain = Standards | 25 (`INT-126..150`) |
> **Total this pass: 150 integration entries.**

## Output 14 — Integration Capability Matrix (domain → dominant protocols/auth/licensing/Zambia)
| Domain | Dominant protocol style | Common auth | Licensing tendency | Zambia applicability |
|--------|------------------------|-------------|--------------------|----------------------|
| Financial | REST + ISO 8583/20022 (banks) | OAuth2 / API key / PKI | Commercial + regulated | **High** (mobile money); bank rails restricted |
| Government | Web/portal + GSB (ESB) | **ZamPass** | Government | **High** but mostly portal, few open APIs |
| Weather | REST | API key / open | Freemium + open | **High** (NASA POWER/OpenWeather free-tier) |
| GIS | REST + OGC (WMS/WFS) | API key / none | OSS + Commercial | **High** (OSS: QGIS/GeoServer/PostGIS) |
| Remote Sensing | REST / STAC / OGC | OAuth2 / token / open | Open + Commercial | **High** (Copernicus/USGS/DE Africa free) |
| Drone | SDK / REST | API key / OAuth2 | Commercial + OSS | Medium (OSS: OpenDroneMap) |
| IoT | MQTT / REST / gRPC / LoRaWAN | X.509 / token / keys | OSS + Commercial | **High** (LoRaWAN/ChirpStack/MQTT) |
| Communication | REST + callbacks | API key / token | Commercial | **High** (Africa's Talking SMS/USSD/Voice) |
| Identity | OIDC / OAuth2 / SAML | tokens / public-key | Open std + OSS + Commercial | **High** (Keycloak OSS; ZamPass national) |
| ERP | REST / OData / XML-RPC | OAuth2 / API key | Commercial + OSS | Medium–High (Odoo/ERPNext OSS APIs) |
| Standards | HTTP + file formats | varies | Open standards | **High** (JSON/CSV/GeoJSON/OGC/ISO) |

## Output 15 — Integration Gap Register (`GAP-I01`–`GAP-I10`)
| Gap ID | Gap | Notes |
|--------|-----|-------|
| GAP-I01 | Government platforms are portal-first with **few public/open APIs**; GSB is inter-agency and restricted | ZamPortal/ZRA/PACRA/cadastre confirmed as portals; programmatic access unconfirmed |
| GAP-I02 | Bank of Zambia RTGS/ZIPSS & National Financial Switch access is regulated/restricted | membership-gated; no public docs |
| GAP-I03 | MNO mobile-money API access (MTN/Airtel/Zamtel) requires commercial agreements; endpoint specifics unverified | confirm sandbox/production terms |
| GAP-I04 | ZamPass/ZamPay/GSB technical interface specs not publicly documented | request specs from Smart Zambia |
| GAP-I05 | ZMD (national met) API availability limited/unconfirmed | verify data-sharing terms |
| GAP-I06 | Weather/RS API licensing varies (attribution/commercial/rate limits) — captured qualitatively | confirm per-provider terms & costs |
| GAP-I07 | Exact API rate limits, SLAs, and pricing not captured (model-level only) | vendor pricing/docs |
| GAP-I08 | Quantity floors not met this pass: 150 entries (targets: ≥250 APIs, ≥150 endpoints, ≥100 gov services, ≥100 enterprise, ≥100 comms/payment, ≥100 GIS/IoT/weather/drone) | expansion follow-on |
| GAP-I09 | Several Zambian government agency URLs/services to confirm as live discrete interfaces | verification |
| GAP-I10 | Settlement/currency details for financial rails partially captured | confirm supported currencies/settlement windows |

## Recorded uncertainties (per evidence rules)
- **No integration, architecture, API, or implementation designed.** This is an ecosystem inventory only.
- Government entries reflect confirmed **portals/e-services**; presence of a portal does **not** imply a public API — flagged (`GAP-I01/I04`).
- Confidence scores reflect evidence strength; regulated/restricted rails scored lower due to absent public documentation.
- Publication and retrieval dates for each source are recorded in `EVIDENCE_REGISTER.csv` per the Citation Standard.
