# AgriMine Nexus — Research Quality Dashboard Specification (Deliverable 10 / Component 9)

> Specifies a dashboard that reports research progress and quality by reading the engine's registers. It requires no bespoke database: all metrics are computed from the CSV registers and the Work Package Tracker, so it can be rendered by any BI tool, a notebook, or a static site generator.

---

## 1. Data sources (inputs)

| Metric source | File |
|---------------|------|
| Work-package & gate status | `knowledge-repository/WORK_PACKAGE_TRACKER.md` + `21-quality-assurance/QA_GATE_LOG.csv` |
| Evidence | `02-evidence/EVIDENCE_REGISTER.csv` |
| Requirements & traceability | `10-requirements/REQUIREMENT_REGISTER.csv` |
| Knowledge graph | `10-requirements/GRAPH_NODES.csv`, `GRAPH_EDGES.csv` |
| Risks / opportunities | risk & opportunity registers |
| Integrations / APIs | `14-integrations/*.csv` |

## 2. Panels & metrics

| Panel | Metric | Computation |
|-------|--------|-------------|
| **Research Progress** | % work packages complete | complete WPs ÷ 19 |
| **Work Package Completion** | per-WP status + gates passed | from tracker/QA log |
| **Evidence Counts** | total sources; new this period | count rows in Evidence Register |
| **Source Distribution** | by reliability tier (1–4) | group by `reliability_tier` |
| **Confidence Scores** | avg/median confidence; % low-confidence (<50) | over evidence & findings |
| **Coverage by Industry** | evidence/requirements per `TAX-IND.*` | group by `industry` |
| **Coverage by Province** | evidence per Zambian province | group by `LOC-` province |
| **Coverage by Stakeholder** | stakeholders profiled vs taxonomy `STK` nodes | join to taxonomy |
| **Coverage by Technology** | assessments per `AIM/GIS/IOT/DRN/TEC` | group by classification |
| **Open Risks** | count/severity of `open` risks | risk register |
| **Outstanding Questions** | open items flagged `[OPEN QUESTION]` | scan artifacts/registers |
| **Research Gaps** | requirements with broken forward/backward chains | traceability rule check (D6 §3) |
| **Quality Gate Status** | count of artifacts per gate result | QA gate log |

## 2b. Evidence-acquisition preparation panels (added ACT-005)

Computed from the Master Source Register, National Data Inventory, and Research Collection Matrix:

| Panel | Metric | Computation |
|-------|--------|-------------|
| **Sources Identified** | count of catalogued sources | rows in `02-evidence/MASTER_SOURCE_REGISTER.csv` |
| **Datasets Identified** | count of expected datasets | rows in `15-datasets/NATIONAL_DATA_INVENTORY.csv` |
| **Coverage by Theme** | research questions & sources per theme | group Research Collection Matrix by `theme` |
| **Coverage by Province** | data availability per province | join datasets/sources spatial coverage → 10 provinces |
| **Coverage by Institution** | sources per organisation/owner | group source register by `organization` |
| **Coverage by Research Question** | % RQs mapped to ≥1 source | matrix rows with non-empty `potential_source_ids` ÷ total RQs |
| **Coverage by Reliability Tier** | sources per tier (1–4) | group source register by `reliability_tier` |
| **Coverage by Data Format** | datasets per format | group data inventory by `format` |

A point-in-time computation of these panels is stored in `knowledge-repository/21-quality-assurance/DASHBOARD_SNAPSHOT.md`.

## 3. Derived quality indicators

- **Traceability completeness** = requirements with full evidence→value chain ÷ total requirements.
- **Evidence quality index** = weighted avg of tier (1=4pts…4=1pt) × confidence.
- **Verification rate** = verified+corroborated sources ÷ total sources.
- **Contradiction load** = count of `CONTRADICTS` edges unresolved.

## 4. Refresh & thresholds

- Recompute on every commit that touches a register (can be a CI step or a notebook run).
- **Red flags:** any `Must` requirement with a broken chain; any work package attempting Gate 8 with unpassed Gates 1–7; verification rate < 70%; average confidence < 60.

## 5. Reference implementation note

A minimal implementation is a Python/pandas notebook that loads the CSVs and renders tables/charts, or a single static HTML page. The spec deliberately keeps the store as flat files so the dashboard stays offline-capable and version-controlled (ROM philosophy). No dashboard is built in ACT-003 — only specified.
