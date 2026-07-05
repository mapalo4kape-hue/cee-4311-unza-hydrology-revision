---
id: WP1.1-SVP
title: Source Validation Plan — WP1.1
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 1 — Foundation Research
work_package: WP1.1
industry: cross-industry
topic: Source validation
keywords: [validation, sources, bias, confidence, cross-reference]
summary: Defines how every WP1.1 source will be validated before its data is trusted — strategy, cross-reference sources, known limitations, bias assessment, confidence rules, and fallback sources.
source: derived
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 100
evidence_level: 1
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [MASTER_SOURCE_REGISTER.csv, RESEARCH_COLLECTION_MATRIX.csv, ../../CITATION_STANDARD.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Source Validation Plan — WP1.1

> No source's data is treated as a finding until it passes this plan. Applies the ROM source hierarchy and Phase-3 validation, and the Citation Standard.

## 1. Universal validation strategy (every source)

1. **Provenance check** — confirm the source organisation, official URL, and that the document/dataset is the authentic latest version.
2. **Currency check** — record publication date; flag if older than the theme's acceptable staleness (macro: ≤2y preferred; structural/geographic: ≤5y; boundaries: latest).
3. **Cross-reference** — corroborate each material figure against ≥1 independent source (ideally a different tier). Prefer **Tier 1** for official statistics, **Tier 2** for validation.
4. **Contradiction handling** — if sources disagree, record all values, create a `CONTRADICTS` link, keep the higher-tier/most-recent as primary, and **lower confidence**.
5. **Confidence scoring** — assign 0–100 per the Citation Standard confidence bands; never exceed the minimum confidence of supporting evidence.
6. **Metadata capture** — every accepted figure becomes an Evidence Register (`SRC-`) row with org, publication date, retrieval date, tier, confidence.

## 2. Per-tier rules

| Tier | Validation posture | Cross-reference requirement |
|------|--------------------|-----------------------------|
| 1 (Govt/official) | Trust as primary; still date-stamp | Corroborate headline figures with WB/IMF/UN where they exist |
| 2 (Multilateral/academic) | Strong; good for cross-checking Tier 1 | Compare with Tier 1 national figures; note methodology differences |
| 3 (Industry/vendor) | Treat as claims | Must corroborate with Tier 1/2 before use |
| 4 (Media/forums) | Signal only | Never used as authoritative; must verify upstream |

## 3. Per-source validation (Master Source Register)

> Fallbacks are alternative sources if the primary is inaccessible/outdated. Bias flags guide confidence adjustment.

| Source | Cross-reference sources | Known limitations | Bias risk | Confidence rule | Fallback |
|--------|------------------------|-------------------|-----------|-----------------|----------|
| MSR-001 ZamStats | MSR-022, MSR-024, MSR-037 | Inter-census gaps; district re-demarcation | Possible optimistic framing (govt) | 90+ if census-based & <3y | MSR-022 WB (rebased) |
| MSR-002 Bank of Zambia | MSR-023 IMF, MSR-022 WB | Monetary focus; less subnational | Low | 90+ for monetary/FX | MSR-023 IMF |
| MSR-003 MoFNP | MSR-023, MSR-028 | Budget optimism | Political | 70–85; corroborate | MSR-023, MSR-022 |
| MSR-004 ZICTA | MSR-029 ITU, MSR-030 GSMA | Operator self-report inputs | Commercial (via operators) | 70–85; xref ITU | MSR-029, MSR-030 |
| MSR-005/006/007 Energy | MSR-028 AfDB, MSR-022 | Utility reporting cadence | Commercial/institutional | 70–85 | MSR-028 |
| MSR-008/009 Transport | MSR-035 OSM, MSR-036 HDX | GIS access limited; OSM rural gaps | Coverage bias (urban) | 70–85; geo-consistency | MSR-035/036 |
| MSR-010/011 Water | MSR-025 FAO-AQUASTAT, MSR-027 | Subnational sparsity | Institutional | 70–85 | MSR-025 |
| MSR-012 ZEMA | MSR-040/041 satellite | Monitoring coverage gaps | Institutional | 70–85 | Satellite (MSR-040/041) |
| MSR-013 ZMD | MSR-042 CHIRPS, MSR-044 ERA5 | Station sparsity | Low | 80+ with satellite xref | MSR-042/043/044 |
| MSR-014 ZDA | MSR-022, MSR-028 | Promotional framing | Commercial (investment) | 65–80 | MSR-022 |
| MSR-016 ZRA | MSR-022 WB trade, MSR-025 | Classification harmonisation | Institutional | 75–85 | MSR-022 |
| MSR-017 MLGRD | MSR-038/039 boundaries | Boundary version drift | Low | 85+ for admin structure | MSR-038 geoBoundaries |
| MSR-022 World Bank | MSR-001, MSR-023 | Modelled/estimated cells | Low | 85+; note "modelled" | MSR-023 |
| MSR-023 IMF | MSR-002, MSR-022 | Forecast uncertainty | Low | 85+ for macro | MSR-022 |
| MSR-024 UNDP | MSR-001, MSR-027 | Composite indices lag | Low | 80+ | MSR-022 |
| MSR-025 FAO | MSR-018, MSR-033 | National aggregation | Low | 80+ | MSR-018 |
| MSR-029 ITU | MSR-004, MSR-030 | Annual lag | Low | 80+ | MSR-004 |
| MSR-030 GSMA | MSR-004, MSR-029 | Industry-funded | Commercial | 65–80; corroborate | MSR-029 |
| MSR-031 FSD/FinScope | MSR-002, MSR-022 | Survey-year gaps | Low–med | 80+ in survey years | MSR-002 |
| MSR-035 OSM | MSR-036, MSR-008 | Crowd-sourced completeness | Coverage (urban) | 70–85; geo-consistency | MSR-036 HDX |
| MSR-036 HDX | MSR-038, MSR-037 | Dataset-dependent quality | Varies | Per-dataset | MSR-038/037 |
| MSR-037 WorldPop | MSR-001 | Modelled, not census | Low | 80+ (label modelled) | MSR-001 |
| MSR-038 geoBoundaries / MSR-039 GADM | MSR-017 | Version/vintage differences | Low | 85+ (record vintage) | each other |
| MSR-040 Copernicus / MSR-041 NASA | MSR-042/044 | Cloud cover; processing needs | Low | 80+ (document processing) | each other |
| MSR-042 CHIRPS / MSR-043 POWER / MSR-044 ERA5 | MSR-013 ZMD | Model/reanalysis vs station | Low | 80+ (note method) | ZMD (MSR-013) |

## 4. Escalation
If neither a primary nor any fallback yields acceptable data for a research question, mark the question `[OPEN QUESTION]`, log a **data gap** in the National Data Inventory and dashboard, and consider deferring to a primary-collection activity (interview/survey/field) in a later work package.
