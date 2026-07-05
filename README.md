# AgriMine Nexus — Research Governance Workspace

This folder holds the research-governance materials for the **AgriMine Nexus** project, following the *Master Research Operating Manual (ROM), Version 1.0*.

The working rule (from the project directive): **read and internalise the ROM, and each time an activity is carried out, produce a record of *how* it was done and save it to GitHub.**

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
| [ACT-004](activity-log/2026-07-05_ACT-004_wp1.1-project-initiation-package.md) | 2026-07-05 | Open WP1.1 & produce the Project Initiation Package (PIP) | Stage 1 · initiation | Complete (PIP in Gate 1 review) |

## Current position

Now operating in **research-consultant mode**. WP1.1 is **open**: the [Project Initiation Package](knowledge-repository/01-research/WP1.1_project-initiation-package_v01.md) (objectives, scope, ~250 research questions, deliverables, sources, stakeholders, outputs, risks, acceptance criteria, activity plan) is submitted for **QA Gate 1**. **No data collection begins until the PIP is approved.** Next: ACT-005 (planning refinement). Status tracked in [`knowledge-repository/WORK_PACKAGE_TRACKER.md`](knowledge-repository/WORK_PACKAGE_TRACKER.md).

## How to add a new activity record

1. Copy [`templates/ACTIVITY_RECORD_TEMPLATE.md`](templates/ACTIVITY_RECORD_TEMPLATE.md) into `activity-log/` as `YYYY-MM-DD_ACT-NNN_short-slug.md`.
2. Fill in every field; score all evidence per ROM §11.
3. Add a row to the table above.
4. Commit and push.

## Guardrail

Per ROM §1, **no** software architecture, UI/UX, database, API, AI-model, or infrastructure work may begin until the relevant industry research program is complete according to the manual.
