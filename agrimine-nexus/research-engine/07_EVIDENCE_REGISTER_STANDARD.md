# AgriMine Nexus — Evidence Register Standard (Deliverable 7 / Component 6)

> Defines the master evidence register — the single source of truth for every source used anywhere in the project. Implements the Citation Standard at data-model level. Physical register: `knowledge-repository/02-evidence/EVIDENCE_REGISTER.csv`.

---

## 1. Rules

- **Every** source cited anywhere must have exactly one row here with a unique `SRC-` id.
- A citation `[SRC-NN]` in any document is invalid unless `SRC-NN` exists in the register (enforced at QA Gate 2).
- Rows are **append-only**; corrections add a new version note, never overwrite. Retrieval facts are immutable history.
- Where possible, store the actual source file in `03-sources/` named `SRC-NNNN_<slug>.<ext>` (Tier-1/2 documents especially).

## 2. Register schema (CSV columns)

| Column | Required | Description |
|--------|----------|-------------|
| `evidence_id` | ✔ | `SRC-NNNN`, unique, never reused |
| `title` | ✔ | title of the source |
| `source` | ✔ | publication / document / URL locator |
| `organization` | ✔ | authoring organization (Citation Standard Rule A) |
| `publication` | ✔ | publication venue/series (or "self") |
| `publication_date` | ✔ | `YYYY-MM-DD` or `YYYY` |
| `retrieved_date` | ✔ | `YYYY-MM-DD` |
| `industry` | ✔ | `TAX-IND.*` or `cross-industry` |
| `research_program` | ✔ | MREP stage / `governance` |
| `topic` | ✔ | short topic |
| `reliability_tier` | ✔ | 1–4 (ROM source hierarchy) |
| `confidence` | ✔ | 0–100 |
| `verification_status` | ✔ | unverified / corroborated / verified / disputed |
| `related_findings` | ✔* | `F-` ids (may be empty at intake) |
| `related_requirements` | ✔* | `BR-/FR-` ids |
| `related_risks` | ✔* | `RISK-` ids |
| `related_opportunities` | ✔* | `OPP-` ids |
| `stored_file` | – | path in `03-sources/` if archived |
| `notes` | – | free notes, contradictions (`CONTRADICTS SRC-xx`) |

\* list columns may be empty when a source is first registered; they are filled as findings/requirements are derived.

## 3. Reliability tiers (from ROM §2)

| Tier | Sources |
|------|---------|
| 1 | Government publications, Acts, regulations, national/international standards, official statistics/databases |
| 2 | Peer-reviewed journals, universities, research institutions, UN/World Bank/FAO/IFAD/ILO/UNEP/WHO/AfDB |
| 3 | Industry associations, consulting firms, annual reports, technical manuals, vendor docs, conference papers |
| 4 | Public discussions, forums, blogs, social media — pain-point signal only, never authoritative without verification |

## 4. Verification workflow

`unverified` → (found in a second independent source) → `corroborated` → (checked against a Tier-1/2 authority) → `verified`. Conflicting sources are linked with `CONTRADICTS` and both kept; confidence is lowered and the contradiction recorded (ROM Phase 3).

## 5. Seed

The register is seeded with the two governance sources already used (`SRC-0001` ROM, `SRC-0002` MREP). Real evidence accumulates as work packages run.
