---
id: WP3-MATRICES
title: Technology Registers, Mapping Matrices, Zambia Readiness & Gaps (WP3)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 3 — Technology Research
work_package: WP3
industry: cross-industry
topic: Technology intelligence
keywords: [technology, AI, GIS, remote-sensing, drone, IoT, enterprise, cybersecurity, readiness]
summary: Outputs 2-15. Domain registers (views of the catalogue), OSS/commercial split, technology-to-workflow/regulation/stakeholder matrices, Zambia readiness assessment, and technology gaps. Evidence-first; no software/architecture/requirements.
source: SRC-0081;SRC-0108;SRC-0109;SRC-0110;SRC-0111;SRC-0112
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 74
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_GLOBAL_TECHNOLOGY_CATALOGUE.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Technology Registers, Matrices, Readiness & Gaps (Outputs 2–15)

> The **domain registers (Outputs 2–8)** and **OSS/commercial registers (9–10)** are **filtered views of the Global Technology Catalogue** (`01_GLOBAL_TECHNOLOGY_CATALOGUE.csv`) via the `domain` and `licensing` columns — not duplicated here. Counts below.

## Outputs 2–10 — Register summaries (catalogue filters)
| Register | Filter | Count (this pass) |
|----------|--------|-------------------|
| 2. AI Capability Register | domain=AI | 46 (`TECH-001..046`) |
| 3. GIS & Spatial Intelligence Register | domain=GIS | 13 (`TECH-047..059` incl. shared) |
| 4. Remote Sensing Register | domain=RS | 13 (`TECH-055,060..072`) |
| 5. Drone Technology Register | domain=Drone | 11 (`TECH-073..083`) |
| 6. IoT Technology Register | domain=IoT | 21 (`TECH-084..104`) |
| 7. Enterprise Platform Register | domain=Enterprise | 31 (`TECH-105..135,150`) |
| 8. Cybersecurity Register | domain=Cyber | 14 (`TECH-136..149`) |
| 9. Open-Source Technology Register | licensing contains OSS | ~90 |
| 10. Commercial Technology Register | licensing contains Commercial | ~70 |
> **Total catalogued this pass: 150 technologies** (`TECH-001`–`TECH-150`).

## Output 11 — Technology-to-Workflow Matrix (selected)
| Technology | Workflows |
|-----------|-----------|
| YOLO / OpenCV (vision) | WF-013/015/016 (scouting/pest/disease); WF-M/C inspection |
| OCR/IDP (Tesseract/Textract) | WF-007 GIN, WF-C08 delivery notes, permits |
| Time-series forecasting | WF-019 weather, WF-029 price, WF-L demand |
| Vector DB + RAG | knowledge/advisory (WF-038/039) |
| PostGIS/QGIS/ArcGIS | WF-003 field mapping, WF-M03 mine planning, WF-E10 monitoring |
| Sentinel-2/Landsat/NDVI | WF-014/025 crop monitoring/yield, WF-E11 |
| Drone mapping (DroneDeploy/Pix4D/ODM) | WF-024/025 (ag), WF-M survey, WF-C07 progress, WF-E inspection |
| LoRaWAN/NB-IoT + sensors | WF-012 irrigation, WF-019 weather, WF-026/027 storage/cold-chain, WF-E10 monitoring |
| GPS/telematics | WF-L08/L11/L12 fleet/haulage |
| RFID/BLE + WMS | WF-L17..L20 warehouse |
| Offline sync (CouchDB/SQLite/CRDT) | all field workflows (WF-033 records, WF-038 extension) |
| ERP/BPM/workflow engines | WF-006/032 finance, WF-C12 valuations, procurement |
| Search/BI (Metabase/Superset) | WF-035 reporting, dashboards |
| Mobile money + USSD/SMS | WF-007/029/032/037 payments & advisories |
| IAM/MFA/encryption/audit | all data workflows (compliance with DPA) |

## Output 12 — Technology-to-Regulation Matrix (selected)
| Technology | Regulation |
|-----------|-----------|
| IAM/MFA/encryption/audit logging | Data Protection Act 2021 (REG-0024); Cyber Acts 2025 (REG-0025) |
| Cloud platforms | data-residency under DPA (REG-0024) |
| GIS/RS boundaries & land data | admin geography (WP1.1); Lands/EMA |
| IoT emissions/water monitoring | EMA 2011 / EIA (REG-0017/18); WRMA (REG-0019) |
| e-payment / mobile money tech | BoZ / FIC AML (REG-0031); NPS |
| Digital documents / e-signatures | Electronic Transactions / Cyber Acts (REG-0025) |
| Standards conformance (products) | Standards Act 2017 (REG-0016) |
| Public-sector platforms (e-GP) | Public Procurement Act (REG-0029) |

## Output 13 — Technology-to-Stakeholder Matrix (selected)
| Technology | Stakeholders |
|-----------|--------------|
| ZIAMIS-class registries / OCR / RAG | MoA (STK-001), agro-dealers (STK-032), farmers (STK-028) |
| GIS/RS/drone | MRC/mines (STK-009/039), consultants (STK-047/050), ZEMA (STK-010) |
| IoT sensors/telematics | farmers (STK-028), mines (STK-039), fleet operators (STK-055) |
| ERP/BI/workflow | commercial farmers/mines/contractors (STK-029/039/048) |
| Mobile money / payment APIs | MMO (STK-062), banks (STK-060), fintech (STK-069) |
| IAM/cyber | DP Commissioner (STK-022), ZICTA (STK-023), all data holders |
| Cloud/connectivity | telecoms (STK-068), cloud providers (STK-070) |

## Output 14 — Zambia Technology Readiness Assessment
| Technology class | Readiness in Zambia | Basis |
|------------------|---------------------|-------|
| Mobile money / USSD / SMS | **High** — pervasive rails (Airtel/MTN/Zamtel) | WP1.1/WP2.x |
| Feature-phone + offline-first patterns | **High** — connectivity/literacy constraints favour offline/USSD | WP1.1 digital divide |
| GIS/RS (open data: Sentinel/Landsat/SRTM/QGIS/PostGIS) | **Medium-High** — free data + OSS tools usable now | SRC-0081 |
| On-device/edge AI (Gemma/Phi/Whisper/YOLO/TFLite) | **Medium** — works offline but needs skills/devices | SRC-0108/0109 |
| Cloud LLM / large-scale AI | **Low-Medium** — bandwidth/cost/data-residency constraints | SRC-0108; DPA |
| IoT LPWAN (LoRaWAN/NB-IoT) | **Medium** — viable; coverage/power/skills gaps | SRC-0110/0111 |
| Satellite IoT | **Medium** — closes rural dead zones; cost | SRC-0110 |
| Drones | **Medium** — regulated (ZCAA/RATSA) + skills/cost | SRC-0081 |
| Enterprise ERP/BI (OSS: Odoo/ERPNext/Metabase) | **Medium** — affordable OSS viable; commercial suites costly | SRC-0079 |
| Cybersecurity (Keycloak/MFA/TLS/audit) | **Medium** — OSS available; capacity gap; DPA driver | SRC-0112 |
| Connectivity dependence | **Constraint** — intermittent rural connectivity is the key limiter | WP1.1 |

## Output 15 — Technology Gap Register
| Gap ID | Gap | Priority | Resolution |
|--------|-----|----------|------------|
| GAP-T01 | Offline-first + edge-AI depth for rural low-connectivity ops | H | evaluate on-device stacks (later stage) |
| GAP-T02 | Local-language ASR/TTS/NLP (Bemba/Nyanja/Tonga/Lozi…) coverage | H | assess Whisper/Vosk fine-tuning feasibility |
| GAP-T03 | Affordable enterprise tooling for Zambian mid-market | M | OSS ERP/BI evaluation |
| GAP-T04 | IoT power/coverage/skills for LPWAN at scale | M | field feasibility |
| GAP-T05 | Data-residency-compliant cloud/edge options (DPA) | M | hosting options review |
| GAP-T06 | Zambia adoption/case-study evidence per technology (mostly global) | H | local pilots / vendor references |
| GAP-T07 | Per-technology cost/training/SLA specifics | M | vendor documentation |
| GAP-T08 | Quantity floor (≥500 tech / ≥200 commercial / ≥150 OSS / ≥100 APIs) not met (150 catalogued this pass) | M | follow-on catalogue expansion |
| GAP-T09 | APIs/SDKs not separately enumerated to 100 (embedded in entries) | M | dedicated API/SDK register |

## Recorded uncertainties
Technology attributes are largely **global/vendor-reported**; Zambia-specific adoption is inferred from WP1.1/WP2.x context and marked accordingly. Drone airspace rules (ZCAA/RATSA) to confirm as a regulatory item.
