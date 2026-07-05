# AgriMine Nexus — Requirement Traceability Framework (Deliverable 6 / Component 5)

> Defines the end-to-end chain that links raw evidence all the way to business value, and the register that makes every link queryable. This is the spine of the Research Engine. Enforced at QA Gate 5 (Requirement extraction) and Gate 6 (Architecture relevance).

---

## 1. The traceability chain

```
Evidence (SRC-)
  ↓ DERIVED_FROM
Finding (F-)
  ↓ DERIVED_FROM
Knowledge Entity (ENT-)
  ↓ informs
Business Requirement (BR-)
  ↓ REFINES
Functional Requirement (FR-)  ── and ──  Non-Functional Requirement (NFR-)
  ↓ REFINES
User Story (US-)
  ↓ REFINES
Acceptance Criteria (AC-)
  ↓ IMPLEMENTED_BY
Database Entity (DB-)
  ↓
API (API-)
  ↓
UI Screen (UI-)
  ↓
Workflow (WF-)
  ↓
Automation Rule (AR-)
  ↓
AI Model (AI-)
  ↓
Report (RPT-)
  ↓
KPI (KPI-)
  ↓ MEASURED_BY (inverse)
Business Objective (BO-)  →  Business Value
```

Every arrow is a typed edge in the knowledge graph (D4). Traceability is bidirectional: you can walk **forward** (evidence → value) or **backward** (value → evidence).

## 2. The Requirement Traceability Matrix (RTM)

Implemented as `knowledge-repository/10-requirements/REQUIREMENT_REGISTER.csv`. One row per requirement, with columns capturing both directions of the chain:

| Column | Meaning |
|--------|---------|
| `req_id` | `BR-/FR-/NFR-/US-/AC-` |
| `type` | requirement type |
| `title` | short statement |
| `statement` | full requirement text |
| `parent_ids` | upstream req(s) it refines (e.g. FR → BR) |
| `finding_ids` | `F-` this requirement derives from |
| `evidence_ids` | `SRC-` backing those findings |
| `entity_ids` | `ENT-`/`DB-` involved |
| `api_ids` | `API-` that implement it |
| `ui_ids` | `UI-` screens |
| `workflow_ids` | `WF-` |
| `automation_ids` | `AR-` |
| `ai_ids` | `AI-` |
| `report_ids` | `RPT-` |
| `kpi_ids` | `KPI-` |
| `business_objective_ids` | `BO-` |
| `module` | owning `MOD` |
| `industry` | `TAX-IND.*` |
| `priority` | MoSCoW (Must/Should/Could/Won't) |
| `confidence` | 0–100 |
| `status` | proposed / accepted / designed / deferred |
| `work_package` | origin `WP` |

## 3. Traceability rules

1. **Upward completeness:** no `BR-` without ≥1 `finding_id`; no finding without ≥1 `evidence_id`. A requirement lacking evidence is downgraded to `[ASSUMPTION]` (Citation Standard, Rule B).
2. **Downward completeness (design-readiness):** before architecture starts, each `Must` requirement must reach at least a `DB-`/`API-`/`UI-` candidate, or be flagged as a **gap** in the dashboard.
3. **Objective linkage:** every `BR-` maps to ≥1 `BO-`; every `BO-` is measured by ≥1 `KPI-`.
4. **Regulatory linkage:** requirements arising from a regulation carry the `REG-` id in `parent_ids`.
5. **No dangling edges:** every id referenced in any column must exist in a register.

## 4. Worked (illustrative) example

```
SRC-0007 (ZEMA EIA guideline, 2023) 
  → F-0042 "EIA approval is mandatory before mine construction"
  → ENT-PERMIT (EIA approval)
  → BR-006 "Platform must track environmental permits and their validity"
  → FR-131 "System shall alert 60 days before permit expiry"
  → US-210 / AC-210.1
  → DB-PERMIT, API-045 (GET/POST permits), UI-030 (Permit dashboard), WF-012 (renewal workflow), AR-004 (expiry alert)
  → KPI-018 (permit-compliance rate) → BO-002 (Zero compliance breaches)
```
*(Illustrative only — no Stage 1 research has been conducted; real rows are populated by work packages.)*

## 5. Reporting

The Quality Dashboard (D10) reads the RTM to report requirement counts by type, coverage (requirements with full forward+backward chains), and gaps (broken chains).
