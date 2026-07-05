# WP5 — Enterprise Business Architecture & Domain Model (ACT-019)

Converts the Requirements Repository into a **Domain-Driven Design business architecture**. **Not** software/microservices/database/API/cloud architecture, deployment, UML, or UI. Every element traces to `CAP-/REQ-/WF-/STK-/REG-/F-`.

## Files
| File | Contents |
|------|----------|
| `01_ENTERPRISE_DOMAIN_CATALOGUE.csv` | 24 domains (`DOM-*`; 6 core/11 supporting/7 generic) with full attributes + traceability (Output 2) |
| `02_BUSINESS_OBJECT_CATALOGUE.csv` | 30 business objects (`BO-001`–`BO-030`), business attributes only (Output 7) |
| `03_BUSINESS_EVENT_CATALOGUE.csv` | 35 business events (`EVT-001`–`EVT-035`) with trigger/actor/result (Output 6) |
| `04_BUSINESS_ARCHITECTURE_AND_MATRICES.md` | Architecture narrative, taxonomy, bounded contexts, interaction/dependency/cross-domain matrices (Outputs 1,3,4,5,8,9,10) |
| `05_DOMAIN_RISK_AND_CONSTRAINT_REGISTERS.md` | Domain risk (`DRK-01..12`) + constraint (`DCON-01..10`) registers (Outputs 11–12) |
| `06_EXECUTIVE_SUMMARY.md` | Executive summary (Output 16) |

Activity record: `activity-log/2026-07-05_ACT-019_*` (Output 17).
KG (Output 13): `../../10-requirements/GRAPH_*.csv` (`F-0092`–`F-0093`; `E-0205`–`E-0212`).
Evidence (Output 14): synthesis reuses `SRC-0001`–`SRC-0121` (no new sources).

## Domain taxonomy
**Core (6):** Agriculture · Mining · Construction · Environmental · Logistics · Commodity Trading.
**Supporting (11):** Finance · Procurement · Inventory/Asset · HR · CRM · Compliance · Document · Analytics · Notifications · Extension · Geospatial.
**Generic (7):** Identity · Audit · Configuration · Monitoring · File · Messaging · Scheduling.

## Quality rule
Every domain maps to >=1 capability, requirement, workflow, stakeholder (and regulations where applicable), has defined boundaries, and avoids duplicated ownership.

## Handover
Business Object Catalogue anchors ACT-020 (Enterprise Information & Data Architecture) — **not** started.
