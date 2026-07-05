# WP5 — Enterprise Requirements Engineering & Traceability (ACT-018)

Transforms the evidence repository into a fully-traceable **Enterprise Requirements Repository**. Requirements engineering only — **not** architecture, database, API, UI/UX, or implementation phasing. No requirement invented.

## Files
| File | Contents |
|------|----------|
| `01_FUNCTIONAL_REQUIREMENTS.csv` | 106 functional requirements (`REQ-F-001`–`REQ-F-106`), each traced to `CAP-/WF-/STK-/REG-/TECH-/INT-/F-` with verification/acceptance/priority/risk/confidence (Output 1) |
| `02_NON_FUNCTIONAL_REQUIREMENTS.csv` | 32 NFRs (`REQ-N-001`–`REQ-N-032`) with measurable acceptance criteria (Output 2) |
| `03_RULES_CONSTRAINTS_ASSUMPTIONS_USERGOALS.md` | Business Rules (`BR-001..020`), Constraints (`CON-001..012`), Assumptions (`ASM-001..010`), User Goals (Outputs 3–6) |
| `04_TRACEABILITY_DEPENDENCY_RISK_GAP_VV.md` | Traceability matrix, dependency matrix, risk register (`RSK-R01..R10`), gap register (`GAP-RQ-01..08`), V&V plan (Outputs 7–12) |
| `05_EXECUTIVE_SUMMARY.md` | Executive summary (Output 16) |

Activity record: `activity-log/2026-07-05_ACT-018_*` (Output 17).
KG (Output 13): `../GRAPH_*.csv` (`F-0090`–`F-0091`; `E-0199`–`E-0204`).
Evidence (Output 14): synthesis reuses `SRC-0001`–`SRC-0121` (no new sources).

## Totals
138 requirements (106 FR + 32 NFR) · 20 business rules · 12 constraints · 10 assumptions · 10 risks · 8 requirement gaps.

## Traceability rule
Evidence → F- → WF- → STK- → REG- → TECH- → CMP- → INT- → CAP- → REQ-. Every requirement is atomic, unique, testable, and evidence-traced. **No orphan requirements; none invented.**

## Honest limitation
Some NFR targets (availability %, RPO/RTO) are placeholders pending stakeholder confirmation (`GAP-RQ-01`); consolidated set of 138 requirements, not exhaustive (`GAP-RQ-07`). Handover baseline for ACT-019 (Enterprise Architecture) — **not** started.
