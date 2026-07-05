# AgriMine Nexus — Research Governance Workspace

This folder holds the research-governance materials for the **AgriMine Nexus** project, following the *Master Research Operating Manual (ROM), Version 1.0*.

The working rule (from the project directive): **read and internalise the ROM, and each time an activity is carried out, produce a record of *how* it was done and save it to GitHub.**

## Contents

| Path | What it is |
|------|-----------|
| [`ROM_Internalisation.md`](ROM_Internalisation.md) | Faithful working restatement of the ROM — evidence it has been read and internalised. |
| [`templates/ACTIVITY_RECORD_TEMPLATE.md`](templates/ACTIVITY_RECORD_TEMPLATE.md) | Reusable template for documenting how each research activity was carried out (built from the ROM's quality, evidence-scoring, and requirement-extraction standards). |
| [`activity-log/`](activity-log/) | Dated records of every research activity performed. |
| [`source/`](source/) | Primary source documents, kept in-repo for traceability (Evidence First). |

## Activity log

| ID | Date | Activity | ROM phase | Status |
|----|------|----------|-----------|--------|
| [ACT-001](activity-log/2026-07-05_ACT-001_read-and-internalise-rom.md) | 2026-07-05 | Read & internalise the ROM | Planning (governance intake) | Complete |

## How to add a new activity record

1. Copy [`templates/ACTIVITY_RECORD_TEMPLATE.md`](templates/ACTIVITY_RECORD_TEMPLATE.md) into `activity-log/` as `YYYY-MM-DD_ACT-NNN_short-slug.md`.
2. Fill in every field; score all evidence per ROM §11.
3. Add a row to the table above.
4. Commit and push.

## Guardrail

Per ROM §1, **no** software architecture, UI/UX, database, API, AI-model, or infrastructure work may begin until the relevant industry research program is complete according to the manual.
