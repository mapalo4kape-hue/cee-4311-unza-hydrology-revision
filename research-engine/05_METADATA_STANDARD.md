# AgriMine Nexus — Research Metadata Standard (Deliverable 5 / Component 4)

> Mandatory metadata for **every** research artifact. Markdown artifacts carry it as YAML front-matter; registers carry the equivalent columns. Enforced at QA Gate 1 (Scope) and Gate 3 (Evidence quality).

---

## 1. Mandatory front-matter block

Every Markdown artifact begins with:

```yaml
---
id:                 # unique artifact id (e.g. WP1.1-R01)
title:              # descriptive title
author:             # who produced it
research_program:   # MREP stage (e.g. "Stage 1 — Foundation")
work_package:       # e.g. WP1.1
industry:           # TAX-IND.* or "cross-industry"
topic:              # short topic label
keywords: []        # controlled + free tags
summary:            # 1–3 sentence abstract
source:             # primary SRC- id(s) or "derived"
publication_date:   # YYYY-MM-DD (of the artifact)
retrieval_date:     # YYYY-MM-DD (when sources were accessed)
confidence:         # 0–100 net confidence
evidence_level:     # tier 1–4 (best supporting source)
status:             # draft | in-review | reviewed | approved | superseded
version:            # vNN
reviewer:           # who reviewed (QA)
approval_status:    # pending | approved | rejected
related_documents: []     # other artifact ids
related_requirements: []  # BR-/FR-/NFR- ids
related_entities: []      # ENT- ids
related_apis: []          # API- ids
related_modules: []       # MOD ids
related_workflows: []     # WF- ids
---
```

## 2. Field definitions

| Field | Required | Rule |
|-------|----------|------|
| id | ✔ | unique; from ID Registry |
| title | ✔ | ≤ 120 chars |
| author | ✔ | name/role |
| research_program | ✔ | one of the 5 MREP stages |
| work_package | ✔ | valid `WP` id or `governance` |
| industry | ✔ | taxonomy `TAX-IND.*` or `cross-industry` |
| topic | ✔ | short label |
| keywords | ✔ | ≥1; prefer taxonomy nodes |
| summary | ✔ | plain-language abstract |
| source | ✔ | `SRC-` id(s) or `derived` |
| publication_date | ✔ | ISO date |
| retrieval_date | ✔ | ISO date |
| confidence | ✔ | integer 0–100 |
| evidence_level | ✔ | 1–4 |
| status | ✔ | lifecycle value |
| version | ✔ | `vNN` |
| reviewer | ✔ at review | set by QA |
| approval_status | ✔ at approval | set by QA Gate 8 |
| related_* | ✔ (may be empty lists) | cross-links for traceability |

## 3. Lifecycle (status transitions)

```
draft → in-review → reviewed → approved
                 └→ (changes requested) → draft
approved → superseded   (when a new version replaces it; old moves to 22-archives)
```

## 4. Register-column equivalents

For CSV registers (evidence, requirements, graph, integrations), the same descriptive metadata is expressed as columns; the register's own standard (D6/D7) governs the exact schema. Consistency rule: `id`, `confidence`, `evidence_level/source_tier`, `status`, `version`, and the `related_*` links must always be present in some form.

## 5. Compliance

An artifact missing any mandatory field **fails QA Gate 1** and cannot be counted toward work-package completion in the Quality Dashboard (D10).
