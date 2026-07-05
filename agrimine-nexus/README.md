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
| [ACT-006](activity-log/2026-07-05_ACT-006_wp1.1-phase1-authoritative-evidence-acquisition.md) | 2026-07-05 | WP1.1 Phase 1 authoritative evidence acquisition (Zambia national baseline) | Stage 1 · collection | Complete (awaiting review) |

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

**WP1.1 Phase 1 (Authoritative Evidence Acquisition) is complete** (ACT-006): the Zambia national baseline — administrative geography, reference systems, government structure, legal/standards framework, and spatial data infrastructure — is collected with **20 cited authoritative sources** and full traceability. Outputs: [`knowledge-repository/01-research/WP1.1-phase1-national-baseline/`](knowledge-repository/01-research/WP1.1-phase1-national-baseline/). No interpretation, recommendations, or design — pure evidence acquisition. **Awaiting review before economic/demographic/infrastructure/sector intelligence.** Repository migration to `agrimine-nexus-research` remains prepared/validated; the final create-repo/rename/push step needs GitHub write access (see [`MIGRATION_REPORT.md`](MIGRATION_REPORT.md)). Status: [`knowledge-repository/WORK_PACKAGE_TRACKER.md`](knowledge-repository/WORK_PACKAGE_TRACKER.md).

## How to add a new activity record

1. Copy [`templates/ACTIVITY_RECORD_TEMPLATE.md`](templates/ACTIVITY_RECORD_TEMPLATE.md) into `activity-log/` as `YYYY-MM-DD_ACT-NNN_short-slug.md`.
2. Fill in every field; score all evidence per ROM §11.
3. Add a row to the table above.
4. Commit and push.

## Guardrail

Per ROM §1, **no** software architecture, UI/UX, database, API, AI-model, or infrastructure work may begin until the relevant industry research program is complete according to the manual.
