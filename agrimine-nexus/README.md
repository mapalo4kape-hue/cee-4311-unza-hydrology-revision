# AgriMine Nexus — Research Repository

> **Single source of truth** for the AgriMine Nexus research programme. This directory is the **root of the dedicated `agrimine-nexus-research` repository** — see [`MIGRATION_REPORT.md`](MIGRATION_REPORT.md) for the migration out of the hydrology repository (history-preserving).

The working rule (from the project directive): **read and internalise the governing documents, and each time an activity is carried out, produce a record of *how* it was done and save it to GitHub.**

The project follows a strict order: **Governance → Research Engine → Research Execution.** It is now in **Research Execution** (Stage 1 · WP1.1), operating in research-consultant mode.

## Governance documents (all binding)

| Path | What it is |
|------|-----------|
| [`ROM_Internalisation.md`](ROM_Internalisation.md) | The **ROM** — *how* research must be done (method, quality, evidence, deliverables). |
| [`MREP_Internalisation.md`](MREP_Internalisation.md) | The **MREP** — *what* gets researched, *in what order*, and *what each work package produces* (5 stages, 19 work packages, 8 QA gates, 28 deliverables). |
| [`CITATION_STANDARD.md`](CITATION_STANDARD.md) | Mandatory **Citation & Evidence-Traceability Standard** — every factual claim is cited (org, publication date, confidence, retrieval date) and every recommendation traces back to evidence. |

## The Research Engine (ACT-003)

| Path | What it is |
|------|-----------|
| [`research-engine/`](research-engine/) | The internal research system (REIS v1.0): architecture, repository blueprint, master taxonomy, knowledge-graph spec, metadata standard, requirement-traceability framework, evidence-register standard, master entity catalogue, template library, quality-dashboard spec, and validation report. Guarantees traceability from **Evidence → Finding → Knowledge → Requirement → Architecture → Module → Database → API → UI → Business Value**. |

## Working materials

| Path | What it is |
|------|-----------|
| [`knowledge-repository/`](knowledge-repository/) | Version-controlled knowledge base (23-folder REIS hierarchy) + live registers (evidence, requirements/RTM, knowledge graph, integrations, QA gates) + work-package/QA-gate tracker. |
| [`templates/`](templates/) | Reusable authoring templates (19 types) — all enforce the Citation Standard. |
| [`activity-log/`](activity-log/) | Dated records of every research activity performed. |
| [`source/`](source/) | Primary source documents, kept in-repo for traceability (Evidence First). |

## Activity log

| ID | Date | Activity | ROM phase | Status |
|----|------|----------|-----------|--------|
| [ACT-001](activity-log/2026-07-05_ACT-001_read-and-internalise-rom.md) | 2026-07-05 | Read & internalise the ROM | Planning (governance intake) | Complete |
| [ACT-002](activity-log/2026-07-05_ACT-002_internalise-mrep-and-add-citation-standard.md) | 2026-07-05 | Internalise the MREP, scaffold knowledge repo, add Citation Standard | Planning (governance intake) | Complete |
| [ACT-003](activity-log/2026-07-05_ACT-003_build-research-engine.md) | 2026-07-05 | Build the Research Engine (REIS v1.0) — 10 components, 12 deliverables | Engine build (pre-Stage 1) | Complete |
| [ACT-004](activity-log/2026-07-05_ACT-004_wp1.1-project-initiation-package.md) | 2026-07-05 | Open WP1.1 & produce the Project Initiation Package (PIP) | Stage 1 · initiation | Complete |
| [ACT-005](activity-log/2026-07-05_ACT-005_repository-migration-and-evidence-acquisition-prep.md) | 2026-07-05 | Repository migration prep + WP1.1 evidence-acquisition system | Stage 1 · execution prep | Complete |
| [ACT-006](activity-log/2026-07-05_ACT-006_wp1.1-phase1-authoritative-evidence-acquisition.md) | 2026-07-05 | WP1.1 Phase 1 authoritative evidence acquisition (Zambia national baseline) | Stage 1 · collection | Complete |
| [ACT-007](activity-log/2026-07-05_ACT-007_wp1.1-phase2-economic-digital-infrastructure-baseline.md) | 2026-07-05 | WP1.1 Phase 2 economic/population/infrastructure/financial/digital/logistics/climate baseline | Stage 1 · collection | Complete |
| [ACT-008](activity-log/2026-07-05_ACT-008_wp2.1-phase1-agricultural-operations-intelligence.md) | 2026-07-05 | WP2.1 Phase 1 agricultural operations intelligence (41 workflows, 20 stakeholders) | Stage 2 · operations | Complete |
| [ACT-009](activity-log/2026-07-05_ACT-009_wp2.1-phase2-agricultural-information-intelligence.md) | 2026-07-05 | WP2.1 Phase 2 agricultural information/data/document intelligence | Stage 2 · information | Complete |
| [ACT-010](activity-log/2026-07-05_ACT-010_cross-industry-research-sprint.md) | 2026-07-05 | Cross-industry breadth-first sprint: Mining, Construction, Environmental + Comparative Analysis | Stage 2 · breadth-first | Complete |
| [ACT-011](activity-log/2026-07-05_ACT-011_global-product-competitor-intelligence.md) | 2026-07-05 | Global product & competitor intelligence (153 products, 12 deliverables) | Stage 4 · competitors | Complete |
| [ACT-011.1](activity-log/2026-07-05_ACT-011.1_wp2.5-logistics-supply-chain-intelligence.md) | 2026-07-05 | WP2.5 Logistics & Supply Chain operations intelligence (26 workflows linking all industries) | Stage 2 · logistics | Complete |
| [ACT-012](activity-log/2026-07-05_ACT-012_wp1.2-policy-regulatory-landscape.md) | 2026-07-05 | WP1.2 Policy & Regulatory Landscape (~37 instruments, ~21 authorities) | Stage 1 · regulatory | Complete |
| [ACT-013](activity-log/2026-07-05_ACT-013_wp1.3-stakeholder-mapping-ecosystem-intelligence.md) | 2026-07-05 | WP1.3 Stakeholder Mapping & Ecosystem Intelligence (75 stakeholders) | Stage 1 · stakeholders | Complete (awaiting review) |

## Evidence-acquisition system (ACT-005, WP1.1)

| Artifact | Location |
|----------|----------|
| Master Source Register (44 sources) | [`knowledge-repository/02-evidence/MASTER_SOURCE_REGISTER.csv`](knowledge-repository/02-evidence/MASTER_SOURCE_REGISTER.csv) |
| Research Collection Matrix (174 RQs) | [`knowledge-repository/02-evidence/RESEARCH_COLLECTION_MATRIX.csv`](knowledge-repository/02-evidence/RESEARCH_COLLECTION_MATRIX.csv) |
| National Data Inventory (32 datasets) | [`knowledge-repository/15-datasets/NATIONAL_DATA_INVENTORY.csv`](knowledge-repository/15-datasets/NATIONAL_DATA_INVENTORY.csv) |
| Source Validation Plan | [`knowledge-repository/02-evidence/SOURCE_VALIDATION_PLAN.md`](knowledge-repository/02-evidence/SOURCE_VALIDATION_PLAN.md) |
| Data Collection Strategy | [`knowledge-repository/02-evidence/DATA_COLLECTION_STRATEGY.md`](knowledge-repository/02-evidence/DATA_COLLECTION_STRATEGY.md) |
| Dashboard Snapshot | [`knowledge-repository/21-quality-assurance/DASHBOARD_SNAPSHOT.md`](knowledge-repository/21-quality-assurance/DASHBOARD_SNAPSHOT.md) |

## Current position

Operational model for all target industries (WP2.1–2.5 + comparative), the **global competitor landscape** (WP4.1), the **regulatory landscape** (WP1.2 — ~37 instruments, ~21 authorities: [`knowledge-repository/08-regulations/WP1.2-regulatory-landscape/`](knowledge-repository/08-regulations/WP1.2-regulatory-landscape/)), and the **stakeholder ecosystem** (WP1.3 — 75 stakeholders across 10 categories: [`knowledge-repository/01-research/WP1.3-stakeholder-mapping/`](knowledge-repository/01-research/WP1.3-stakeholder-mapping/)). **107 evidence sources** total. Every workflow now maps to regulations and stakeholders — the operational + regulatory + actor model is complete. Evidence-first — **no software, schemas, APIs, UML, features, requirements, business strategy, or AI**. **STOP condition active: awaiting review before Stage 3 (Technology Research).** Repository migration to `agrimine-nexus-research` remains prepared/validated ([`MIGRATION_REPORT.md`](MIGRATION_REPORT.md)). Status: [`knowledge-repository/WORK_PACKAGE_TRACKER.md`](knowledge-repository/WORK_PACKAGE_TRACKER.md).

> Note: this work lives on branch `cursor/agrimine-rom-internalisation-9a65` and is under review in **PR #5** (PR #4 was merged early with only ACT-001).

## How to add a new activity record

1. Copy [`templates/ACTIVITY_RECORD_TEMPLATE.md`](templates/ACTIVITY_RECORD_TEMPLATE.md) into `activity-log/` as `YYYY-MM-DD_ACT-NNN_short-slug.md`.
2. Fill in every field; score all evidence per ROM §11.
3. Add a row to the table above.
4. Commit and push.

## Guardrail

Per ROM §1, **no** software architecture, UI/UX, database, API, AI-model, or infrastructure work may begin until the relevant industry research program is complete according to the manual.
