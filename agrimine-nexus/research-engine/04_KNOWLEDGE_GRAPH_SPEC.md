# AgriMine Nexus — Knowledge Graph Specification (Deliverable 4 / Component 3)

> The enterprise knowledge graph is the model that links every entity, its evidence, and its downstream requirements/modules. This spec defines entity types, relationship types, attributes, identifiers, and traceability rules. It is implemented as CSV node/edge registers so it is versionable and tool-agnostic.

---

## 1. Graph model

- **Nodes** = entities (people, things, concepts, artifacts) — each an instance of a **node type**.
- **Edges** = typed, directed relationships between nodes.
- **Every node and edge is evidence-backed**: it must reference at least one `SRC-` id (Citation Standard) or be explicitly `[ASSUMPTION]`.

## 2. Node types

| Node type | ID prefix | Classified by taxonomy facet |
|-----------|-----------|------------------------------|
| Entity (domain object) | `ENT-` | any (IND/STK/AST/…) |
| Evidence/Source | `SRC-` | DOC/RPT |
| Finding | `F-` | — |
| Requirement (BR/FR/NFR) | `BR-/FR-/NFR-` | DOM/MOD |
| User Story / Acceptance | `US-/AC-` | MOD |
| Database Entity | `DB-` | — |
| API | `API-` | MOD |
| UI Screen | `UI-` | MOD |
| Workflow | `WF-` | PRC |
| Automation Rule | `AR-` | PRC |
| AI Model | `AI-` | AIM |
| GIS Layer | `GIS-` | GIS |
| IoT Device | `IOT-` | IOT/SEN |
| Report | `RPT-` | RPT |
| KPI | `KPI-` | KPI |
| Risk | `RISK-` | — |
| Opportunity | `OPP-` | — |
| Regulation | `REG-` | REG |
| Business Objective | `BO-` | — |
| Stakeholder | `STK-` | STK |
| Organization | `ORG-` | ORG |
| Location | `LOC-` | LOC |

## 3. Relationship (edge) types

| Edge | From → To | Meaning |
|------|-----------|---------|
| `EVIDENCED_BY` | any → `SRC-` | node is supported by evidence |
| `DERIVED_FROM` | `F-` → `SRC-`; `BR-` → `F-` | knowledge derived from lower layer |
| `REFINES` | `FR-` → `BR-`; `AC-` → `US-` | requirement refinement |
| `SATISFIES` | `US-` → `FR-`; `MOD` → `BR-` | fulfilment |
| `IMPLEMENTED_BY` | `FR-` → `API-`/`UI-`/`DB-`/`WF-` | forward traceability |
| `MEASURED_BY` | `BO-` → `KPI-` | objective measured by KPI |
| `GOVERNED_BY` | any → `REG-` | subject to regulation |
| `PART_OF` | `ENT-` → `ENT-` | composition/hierarchy |
| `LOCATED_AT` | `ENT-` → `LOC-` | spatial placement |
| `OWNED_BY` / `OPERATED_BY` | `ENT-` → `STK-`/`ORG-` | ownership/operation |
| `PRODUCES` / `CONSUMES` | `PRC`/`ENT-` → `ENT-` | input/output flows |
| `MONITORED_BY` | `ENT-`/`ENV` → `IOT-`/`SEN` | sensing relationship |
| `MITIGATES` | `MOD`/`FR-` → `RISK-` | risk mitigation |
| `ADDRESSES` | `OPP-`/`FR-` → pain point/`F-` | opportunity linkage |
| `CONTRADICTS` | `SRC-` → `SRC-` | conflicting evidence |
| `SUPERSEDES` | any → any | version replacement |

## 4. Mandatory node attributes

Every node record carries:

| Attribute | Notes |
|-----------|-------|
| `id` | unique, prefixed (see §2) |
| `label` | human name |
| `type` | node type |
| `classification` | ≥1 taxonomy node id (`TAX-…`) |
| `description` | definition |
| `evidence_refs` | list of `SRC-` ids (or `[ASSUMPTION]`) |
| `confidence` | 0–100 (net, per Citation Standard) |
| `source_tier` | best supporting tier (1–4) |
| `industry` | `TAX-IND.*` where applicable |
| `work_package` | originating `WP` |
| `status` | draft / reviewed / approved / superseded |
| `version` | vNN |
| `created_by`, `created_at`, `updated_at` | provenance |
| `related_requirements` | list of `BR-/FR-/NFR-` |
| `related_workflows` | list of `WF-` |
| `related_modules` | list of `MOD` |
| `related_integrations` | list of `API-`/integration ids |

Multiplicity requirement (Component 3): every entity **supports many** — multiple evidence sources, requirements, workflows, regulations, software modules, and integrations. All of these are list-valued attributes/edges, so the model is inherently many-to-many.

## 5. Physical representation

Two CSVs under `10-requirements/` (nodes) and a shared edges file:

- `knowledge-repository/10-requirements/GRAPH_NODES.csv` — columns = the mandatory attributes above.
- `knowledge-repository/10-requirements/GRAPH_EDGES.csv` — columns: `edge_id, from_id, to_id, edge_type, evidence_refs, confidence, note`.

Any graph database (e.g. property-graph) or BI tool can import these directly; git tracks version history (Component 3: Version History + Traceability Rules).

## 6. Traceability rules (enforced at QA Gates 4 & 5)

1. **No orphans:** every `F-` must have ≥1 `DERIVED_FROM SRC-`; every `BR-` ≥1 `DERIVED_FROM F-`.
2. **Forward reachability:** every `BR-` should reach at least one downstream implementation node (`DB-/API-/UI-/WF-`) before design begins, or be flagged as a gap.
3. **Backward reachability:** every implementation node must trace back to a `BR-` and ultimately to `SRC-`.
4. **Objective coverage:** every `BO-` is `MEASURED_BY` ≥1 `KPI-`.
5. **Regulatory coverage:** every regulated entity is `GOVERNED_BY` the relevant `REG-`.
6. **Confidence propagation:** a derived node's confidence may not exceed the minimum confidence of its supporting evidence.
