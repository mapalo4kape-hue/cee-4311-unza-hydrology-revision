# Activity Record — ACT-018

- **Activity ID:** ACT-018
- **Date:** 2026-07-05
- **Work Package:** WP5 — Enterprise Requirements Engineering & Requirement Traceability
- **Stage:** Stage 5 (transition)
- **Consultant:** Cursor AI (research consultant)
- **Status:** Complete (pending review)

## Objective
Transform the evidence repository into a complete **Enterprise Requirements Engineering Repository** with full traceability. Requirements engineering only — **not** architecture, database, API, UI/UX, or implementation phasing. No requirement invented.

## Traceability principle honoured
Every requirement maintains the chain: Evidence → Finding (F-) → Workflow (WF-) → Stakeholder (STK-) → Regulation (REG-) → Technology (TECH-) → Competitor (CMP-, via capability) → Integration (INT-) → Capability (CAP-) → Requirement (REQ-). Each `REQ-*` references applicable upstream IDs. **No orphan requirements.**

## What I did (synthesis; no new external research)
1. Derived atomic, testable **functional requirements** from the 170-capability model (WP4.2), each carrying capability/workflow/stakeholder/regulation/technology/integration/finding references.
2. Derived **non-functional requirements** with measurable acceptance criteria from technology/infrastructure/regulatory findings (WP3/WP1.1/WP1.2).
3. Extracted **business rules** from regulations, **constraints** from national/infrastructure findings, and **assumptions** (separated from evidence, each with rationale/confidence/verification plan).
4. Compiled the **user goal catalogue**, **traceability/dependency matrices**, **risk register**, **gap register**, and **V&V plan**.
5. Updated the knowledge graph (`F-0090`–`F-0091`, requirement-set nodes, edges `E-0199`–`E-0204`).

## Outputs (17 required)
| # | Output | Location |
|---|--------|----------|
| 1 | Functional Requirements Specification | `01_FUNCTIONAL_REQUIREMENTS.csv` (106 FRs) |
| 2 | Non-Functional Requirements Specification | `02_NON_FUNCTIONAL_REQUIREMENTS.csv` (32 NFRs) |
| 3 | Business Rules Catalogue (`BR-001..020`) | `03_RULES_CONSTRAINTS_ASSUMPTIONS_USERGOALS.md` |
| 4 | Constraints Register (`CON-001..012`) | doc 03 |
| 5 | Assumptions Register (`ASM-001..010`) | doc 03 |
| 6 | User Goal Catalogue | doc 03 |
| 7 | Acceptance Criteria Catalogue | inline per requirement (CSVs) + doc 04 |
| 8 | Requirement Traceability Matrix | `04_TRACEABILITY_DEPENDENCY_RISK_GAP_VV.md` (+ CSV columns) |
| 9 | Requirement Dependency Matrix | doc 04 |
| 10 | Requirement Risk Register (`RSK-R01..R10`) | doc 04 |
| 11 | Requirement Gap Register (`GAP-RQ-01..08`) | doc 04 |
| 12 | Verification & Validation Plan | doc 04 |
| 13 | Knowledge Graph Updates | `GRAPH_NODES.csv` / `GRAPH_EDGES.csv` |
| 14 | Evidence Register Updates | no new sources (synthesis reuses `SRC-0001`–`SRC-0121`) |
| 15 | Metadata Updates | doc front-matter |
| 16 | Executive Summary | `05_EXECUTIVE_SUMMARY.md` |
| 17 | Activity Record | this file |

## Totals
**138 requirements** = 106 functional (`REQ-F-001..106`) + 32 non-functional (`REQ-N-001..032`); plus 20 business rules, 12 constraints, 10 assumptions, 10 risks, 8 requirement gaps.

## Key findings
- Foundational cross-cutting requirements (identity/access, offline capture+sync, audit, notifications) underpin most domain requirements.
- Offline-first and mobile-money are Must-priority given connectivity/device/affordability constraints.
- Regulatory compliance (DPA, sector reporting, finance/tax) is a first-class requirement driver.

## Discipline honoured
Requirements state required behaviour/quality, not implementation. No modules/services/APIs/databases/microservices/screens/UML/phasing. Every requirement atomic, unique, testable, evidence-traced; duplicates merged; assumptions separated; unsupported/placeholder items flagged.

## Honest limitations
- Some NFR targets (availability %, RPO/RTO) are placeholders pending stakeholder confirmation (`GAP-RQ-01`).
- Integration-dependent requirements rest on assumptions about gov/MNO API access (`GAP-RQ-02`).
- Consolidated set of 138 requirements (not exhaustive); per-requirement inputs/outputs at summary level (`GAP-RQ-03/07`).

## Evidence
No new sources; synthesis of `SRC-0001`–`SRC-0121` via findings `F-0053`–`F-0088`.

## Stop condition honoured
STOP. Did not begin Enterprise Architecture (ACT-019). Awaiting review.
