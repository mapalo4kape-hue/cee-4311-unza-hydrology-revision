# AgriMine Nexus — Research Engine Architecture (Deliverable 1)

> **ACT-003 · Research Engine Implementation Standard (REIS) v1.0**
> Built by the Research Systems Engineer role. Governed by the [ROM](../ROM_Internalisation.md), [MREP](../MREP_Internalisation.md), and [Citation Standard](../CITATION_STANDARD.md). This document defines the *system* that manages every future research activity, artifact, citation, requirement, entity, and deliverable.

---

## 1. Purpose

The Research Engine turns research from a pile of documents into **structured, linked, reusable knowledge**. It guarantees the golden traceability chain:

```
Evidence → Finding → Knowledge → Requirement → Architecture
        → Software Module → Database → API → User Interface → Business Value
```

No artifact may exist in isolation: every node in the chain references the nodes above and below it.

## 2. Layered architecture

| Layer | Responsibility | Backed by (component / deliverable) |
|-------|----------------|-------------------------------------|
| **L0 — Governance** | The rules all research obeys | ROM, MREP, Citation Standard |
| **L1 — Storage** | Where artifacts physically live, versioned in git | Repository Blueprint (D2) |
| **L2 — Classification** | Controlled vocabulary for tagging everything | Master Taxonomy (D3) |
| **L3 — Knowledge model** | Entities, relationships, IDs | Knowledge Graph Spec (D4) + Master Entity Catalogue (D8) |
| **L4 — Metadata** | Mandatory descriptive fields on every artifact | Metadata Standard (D5) |
| **L5 — Evidence** | Every claim's source of truth | Evidence Register (D7) + Citation Standard |
| **L6 — Traceability** | Links evidence → … → business value | Requirement Traceability Framework (D6) |
| **L7 — Production** | How artifacts are authored | Research Template Library (D9) |
| **L8 — Assurance** | Progress, coverage, quality gates | Quality Dashboard Spec (D10) + MREP QA Gates |
| **L9 — Validation** | Proof the engine satisfies governance | Validation Report (D11) |

## 3. Core data objects and their IDs

Every object carries a stable, human-readable ID prefix so it can be referenced anywhere:

| Object | ID prefix | Example | Registered in |
|--------|-----------|---------|---------------|
| Evidence / source | `SRC-` | `SRC-0042` | Evidence Register (D7) |
| Finding | `F-` | `F-0107` | Research report / activity record |
| Knowledge entity | `ENT-` | `ENT-FARM` | Master Entity Catalogue (D8) |
| Business requirement | `BR-` | `BR-015` | Requirement Register |
| Functional requirement | `FR-` | `FR-231` | Requirement Register |
| Non-functional requirement | `NFR-` | `NFR-044` | Requirement Register |
| User story | `US-` | `US-310` | Requirement Register |
| Acceptance criterion | `AC-` | `AC-310.2` | Requirement Register |
| Database entity | `DB-` | `DB-FARM` | Data Model Catalogue |
| API endpoint | `API-` | `API-089` | API Opportunity Register |
| UI screen | `UI-` | `UI-052` | Product folder |
| Workflow | `WF-` | `WF-021` | Process Maps |
| Automation rule | `AR-` | `AR-013` | Requirement Register |
| AI model / use case | `AI-` | `AI-007` | AI Use Case Matrix |
| GIS layer | `GIS-` | `GIS-011` | GIS Layer Catalogue |
| IoT device profile | `IOT-` | `IOT-006` | IoT Device Catalogue |
| Report | `RPT-` | `RPT-018` | Product folder |
| KPI | `KPI-` | `KPI-033` | Analytics & KPI Framework |
| Risk | `RISK-` | `RISK-012` | Risk Register |
| Opportunity | `OPP-` | `OPP-027` | Opportunity Matrix |
| Business objective | `BO-` | `BO-004` | Business folder |
| Work package | `WP` | `WP2.1` | Work Package Tracker |
| Activity | `ACT-` | `ACT-003` | Activity Log |

ID allocation is centralized in [`../knowledge-repository/00-governance/ID_REGISTRY.md`](../knowledge-repository/00-governance/ID_REGISTRY.md) (next-number-per-prefix) so IDs are never reused.

## 4. Information flow (author → knowledge)

1. **Collect** a source → register it in the Evidence Register (get `SRC-NN`).
2. **Author** an artifact from a template (D9) → fill mandatory metadata (D5) → tag with taxonomy nodes (D3).
3. **State findings** with inline citations (Citation Standard) → each finding gets `F-NN`.
4. **Extract knowledge** → create/link entities (`ENT-`) in the graph (D4/D8).
5. **Derive requirements** → `BR-/FR-/NFR-/US-` linked back to findings (D6).
6. **Trace forward** → requirements link to `DB-/API-/UI-/WF-/AI-/RPT-/KPI-/BO-`.
7. **Assure** → QA gates checked; dashboard (D10) recomputed from the registers.

## 5. Physical realization

The engine is implemented as **plain, version-controlled files** (Markdown specs + CSV registers) so it works offline, needs no server, and is fully auditable in git — consistent with the ROM's offline-capable, evidence-first philosophy. The CSV registers (evidence, requirements, entities, IDs) are the machine-readable "database"; any future dashboard or app can ingest them directly.

## 6. How the components fit together

```
                ┌─────────────── L0 Governance (ROM/MREP/Citation) ───────────────┐
                │                                                                  │
  Templates ──▶ Artifacts ──▶ Metadata ──▶ Taxonomy tags                           │
  (D9)          (in repo/D2)   (D5)         (D3)                                    │
                   │                                                               │
                   ▼                                                               │
             Evidence Register (D7) ──▶ Findings ──▶ Knowledge Graph (D4/D8)        │
                   │                                     │                          │
                   ▼                                     ▼                          │
             Requirement Traceability (D6) ──▶ Architecture / Modules / DB / API / UI / KPI / Business Value
                   │
                   ▼
             Quality Dashboard (D10) ◀── QA Gates ◀── Validation (D11)
```

## 7. Non-goals of ACT-003

- No Stage 1–5 research content is produced.
- No application code, database, or API is built.
- The engine is the **scaffolding and standards**; it is populated only when work packages execute.
