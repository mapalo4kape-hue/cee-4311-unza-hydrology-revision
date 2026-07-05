---
id: WP1.1-P1-COVERAGE
title: Coverage Assessment — Zambia (WP1.1 Phase 1)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 1 — Foundation Research
work_package: WP1.1
industry: cross-industry
topic: Coverage assessment
keywords: [coverage, completeness, priorities]
summary: Assessment of how completely the five Priority-1 collection areas have been covered by authoritative evidence in this phase. Measures completeness, not quantity.
source: derived
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 90
evidence_level: 1
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../../02-evidence/EVIDENCE_REGISTER.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Coverage Assessment — WP1.1 Phase 1 (Authoritative Evidence Acquisition)

> Completeness of each priority area. Legend: 🟢 well covered (authoritative, cross-checked) · 🟡 partial (authoritative but gaps remain) · 🔴 minimal (targets identified, evidence pending).

## 1. Coverage by collection priority

| Priority | Area | Status | Authoritative evidence | Main remaining gaps |
|----------|------|--------|-------------------------|---------------------|
| P1 | Administrative geography | 🟢 | ISO codes [SRC-0003]; ZamStats units [SRC-0004]; CRS [SRC-0006/0007] | Official district code list; ward discrepancy; chiefdom count; gazette/SI history; ZamStats spatial formats/licence |
| P2 | National reference systems | 🟢 | Currency [SRC-0008]; timezone [SRC-0010]; languages/independence [SRC-0011]; identifiers [SRC-0009] | Primary ISO/IANA/ITU confirmation; postal-code status; ZWMA basis; full membership list |
| P3 | Government structure | 🟡 | Branches [SRC-0014/0020]; agencies; EIZ [SRC-0021]; ZABS [SRC-0016] | Definitive ministry list/count; legal basis for several agencies; judiciary detail |
| P4 | Legal & standards framework | 🟡 | DPA [SRC-0012]; Constitution [SRC-0014]; 8NDP [SRC-0015]; Standards Act [SRC-0016] | Primary text for several sector Acts; cyber Acts 2025 primary; SI/Gazette access |
| P5 | National spatial data infrastructure | 🟡 | Mining Cadastre [SRC-0017]; open geospatial (MSR-035..041) | Official ZNSDI/Survey Dept portal; sector portal data access & licences |

## 2. Geographic coverage
- **National:** 🟢 covered (identifiers, structure, law, CRS).
- **Provincial (all 10):** 🟢 enumerated with ISO codes and capitals [SRC-0003][SRC-0004].
- **District:** 🟡 count established (116 at 2022) [SRC-0004]; official per-district code list and post-2022 changes pending.
- **Constituency / Ward:** 🟡 counts established (156 / 1,858) [SRC-0004]; geometries/codes pending; ward-count discrepancy noted.
- **Chiefdom / sub-district:** 🔴 no authoritative count/boundaries yet.

## 3. Source-quality profile (this phase)
- Evidence items added: **20** (`SRC-0003`–`SRC-0022`).
- Tier distribution: Tier 1 ≈ 13; Tier 2 ≈ 5; Tier 3 ≈ 1; Tier 4 ≈ 1 (encyclopedia, corroborated).
- Verification: majority `verified`/`corroborated`; **integrity/checksum pending** (files not yet downloaded).
- Priority followed government/primary sources over volume, per the quality standard.

## 4. Completeness verdict
Priority 1 (administrative geography) and Priority 2 (reference systems) are **substantially complete** for a national baseline. Priorities 3–5 have an **authoritative core** with clearly enumerated gaps (see Gap Register). No economic/demographic/infrastructure/sector intelligence was collected (correctly out of scope for this phase).
