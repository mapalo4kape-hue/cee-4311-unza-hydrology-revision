---
id: WP5-TRACE
title: Requirement Traceability, Dependency, Risk, Gap & V&V (WP5)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 5 (transition) — Requirements Engineering
work_package: WP5
industry: cross-industry
topic: Traceability, dependency, risk, gap, verification & validation
keywords: [traceability, dependency, risk, gap, verification, validation, requirements]
summary: Outputs 8-12. Requirement Traceability Matrix, Dependency Matrix, Risk Register, Gap Register, and Verification & Validation Plan. Requirements engineering only.
source: F-0053;F-0073;F-0077;F-0078;F-0079;F-0086;F-0088
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 68
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_FUNCTIONAL_REQUIREMENTS.csv, 02_NON_FUNCTIONAL_REQUIREMENTS.csv, 03_RULES_CONSTRAINTS_ASSUMPTIONS_USERGOALS.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Requirement Traceability, Dependency, Risk, Gap & V&V (Outputs 8–12)

## Output 8 — Requirement Traceability Matrix
> The traceability chain **Evidence → F- → WF- → STK- → REG- → TECH- → CMP- → INT- → CAP- → REQ-** is carried **inline per requirement** in the requirement CSVs (each `REQ-F-*`/`REQ-N-*` row lists its capability, workflows, stakeholders, regulations, technologies, integrations, and findings). This section summarises coverage.

| Upstream layer | Linked to requirements? | Notes |
|----------------|------------------------|-------|
| Findings (F-) | Yes | every REQ references >=1 finding |
| Workflows (WF-) | Yes (functional) | all FRs cite workflows; NFRs cite capabilities/findings |
| Stakeholders (STK-) | Yes (functional) | all FRs cite stakeholders |
| Regulations (REG-) | Where applicable | compliance/finance/safety/env FRs + NFR-013/019/023 |
| Technologies (TECH-) | Yes | FRs/NFRs cite enabling technologies |
| Competitors (CMP-) | Via capability | CMP support carried at capability layer (`CAP-*`) |
| Integrations (INT-) | Where applicable | payment/comms/gov/identity/spatial FRs |
| Capabilities (CAP-) | Yes | every REQ maps to >=1 capability; no orphan requirement |

**Coverage:** 106 functional requirements (`REQ-F-001..106`) + 32 non-functional (`REQ-N-001..032`) = **138 requirements**, all traceable. Capability→requirement coverage: all 6 capability domains represented; some capabilities merged into shared requirements (e.g., `CAP-089+090 → REQ-F-059`).

## Output 9 — Requirement Dependency Matrix (representative)
| Requirement | Depends on (supporting) | Blocking (must precede) | External systems | Regulations | Stakeholders |
|-------------|-------------------------|-------------------------|------------------|-------------|--------------|
| REQ-F-001 farmer profile | REQ-F-096 identity;REQ-F-099 user/org | advisory/finance FRs | INT-032 | REG-0024 | STK-028 |
| REQ-F-013 warehouse receipt | REQ-F-012 storage;REQ-F-076 GL | REQ-F-027 produce finance | INT-034 | REG-0012 | STK-031;STK-060 |
| REQ-F-022 farmer payment | REQ-F-079 mobile money;REQ-F-078 payments | subsidy/credit payout | INT-003;INT-006 | REG-0031 | STK-028;STK-062 |
| REQ-F-045 statutory mining report | REQ-F-043 monitoring;REQ-F-033 production | — | INT-030;INT-016 | REG-0009;REG-0010 | STK-009;STK-039 |
| REQ-F-063 env compliance report | REQ-F-043 monitoring;REQ-F-044 LIMS | — | INT-035;INT-036 | REG-0017;REG-0019 | STK-010 |
| REQ-F-092 notifications | REQ-F-096 identity | advisory/price FRs | INT-091;INT-102 | — | STK-028;STK-030 |
| REQ-F-100 offline capture | REQ-F-101 sync | most field FRs | — | — | STK-028;STK-048 |
| REQ-F-101 offline sync | REQ-F-096 identity;REQ-N-002 | field data integrity | INT-133 | REG-0024 | STK-070 |
| REQ-N-013 privacy/DPA | REQ-F-096;REQ-F-097;REQ-F-105 | all personal-data FRs | INT-105 | REG-0024 | STK-022 |
| REQ-N-024 interoperability | REQ-F-091 import/export | integration-dependent FRs | INT-126;INT-134 | — | STK-070 |
> Foundational dependencies: identity/access (`REQ-F-096..099`), offline capture+sync (`REQ-F-100/101`), audit (`REQ-F-094`), and notifications (`REQ-F-092`) underpin most domain requirements.

## Output 10 — Requirement Risk Register (risk if omitted)
| Risk ID | Requirement(s) | Risk if omitted | Severity | Confidence |
|---------|----------------|-----------------|----------|------------|
| RSK-R01 | REQ-N-001/002;REQ-F-100/101 | Field unusable in rural areas; data loss | High | 68 |
| RSK-R02 | REQ-N-008..013;REQ-F-096..098;REQ-F-105 | Security/privacy breach; DPA non-compliance | High | 64 |
| RSK-R03 | REQ-F-079;REQ-F-022;REQ-F-078 | No accessible payment rail; exclusion of users | High | 62 |
| RSK-R04 | REQ-F-045;REQ-F-063;REQ-N-023 | Statutory/regulatory breach; penalties | High | 60 |
| RSK-R05 | REQ-F-094;REQ-N-019 | No accountability/audit; disputes | Medium | 58 |
| RSK-R06 | REQ-F-013;REQ-F-076/077 | Financial integrity failures | Medium | 56 |
| RSK-R07 | REQ-F-040;REQ-F-057 | Safety/legal exposure | High | 58 |
| RSK-R08 | REQ-N-024/025;REQ-F-091 | Data silos; integration failure | Medium | 54 |
| RSK-R09 | REQ-N-015;REQ-F-092/106 | Low adoption among target users | Medium | 54 |
| RSK-R10 | REQ-N-016/017 | Data loss on disaster; no recovery | Medium | 50 |

## Output 11 — Requirement Gap Register (`GAP-RQ-01`–`GAP-RQ-08`)
| Gap ID | Gap | Notes |
|--------|-----|-------|
| GAP-RQ-01 | Some NFR acceptance targets are placeholders pending stakeholder confirmation (e.g., availability %, RPO/RTO) | confirm with owners; currently documented as "to be set" |
| GAP-RQ-02 | Integration-dependent requirements rest on assumptions ASM-001/002 (gov/MNO API access) | verify per `GAP-I03/I04` |
| GAP-RQ-03 | Per-requirement inputs/outputs and detailed acceptance scenarios captured at summary level | expand in detailed spec |
| GAP-RQ-04 | Livestock/aquaculture and carbon requirements low-confidence (thin evidence) | tie to `GAP-C02/C08` |
| GAP-RQ-05 | Regulatory rate/threshold specifics (tax/royalty/permit fees) not fully itemised | maintain reference config; verify with regulators |
| GAP-RQ-06 | Competitor traceability held at capability layer, not per requirement | acceptable per scope; note for detailed RTM |
| GAP-RQ-07 | Requirement volume is a consolidated set (138) not an exhaustive enumeration | further decomposition possible without inventing scope |
| GAP-RQ-08 | Priorities are criticality ratings (Must/Should/Could), not implementation phasing (out of scope) | phasing deferred to later stages |

## Output 12 — Verification & Validation Plan
| Aspect | Approach |
|--------|----------|
| Verification methods | Each requirement carries a method: **Test** (functional behaviour), **Analysis** (computation/scalability), **Inspection** (config/security), **Audit** (regulatory/privacy). |
| Traceability verification | Confirm every REQ references >=1 CAP and >=1 finding; no orphans (automable check on the CSVs). |
| Acceptance criteria | Stated per requirement (functional) and measurable per NFR where evidence supports; placeholders flagged `GAP-RQ-01`. |
| Business-rule validation | Validate BR-001..020 against source regulations with the relevant authority/stakeholder. |
| Assumption validation | Execute ASM-001..010 verification plans before dependent requirements are baselined. |
| Regulatory validation | Confirm reporting formats/timelines with ZEMA/WARMA/Mines/ZRA (CON-006). |
| Field validation | Validate offline/mobile-money/local-language requirements via field trials in target segments. |
| Review & sign-off | Stakeholder review of user goals and priorities; requirements baselined only after review (status currently in-review). |

## Discipline & uncertainties
Requirements state **required behaviour/quality**, not implementation. No modules, services, APIs, databases, microservices, screens, UML, or implementation phasing are produced. Every requirement is atomic, uniquely identified, testable, and evidence-traced; unsupported or placeholder items are flagged rather than invented.
