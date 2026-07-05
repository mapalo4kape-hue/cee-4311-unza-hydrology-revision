---
id: WP5-DOMRISK
title: Domain Risk & Constraint Registers (WP5)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 5 — Enterprise Business Architecture
work_package: WP5
industry: cross-industry
topic: Domain risk and constraint registers
keywords: [domain, risk, constraint, business-architecture]
summary: Outputs 11-12. Domain Risk Register and Domain Constraint Register. Business architecture only.
source: F-0058;F-0073;F-0077;F-0078;F-0086;F-0087
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 68
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_ENTERPRISE_DOMAIN_CATALOGUE.csv, 04_BUSINESS_ARCHITECTURE_AND_MATRICES.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Domain Risk & Constraint Registers (Outputs 11–12)

## Output 11 — Domain Risk Register
| Risk ID | Domain(s) | Risk | Severity | Linked (REQ/CON) | Confidence |
|---------|-----------|------|----------|------------------|------------|
| DRK-01 | ALL cores | Field operations unusable under intermittent connectivity | High | REQ-N-001;CON-001 | 68 |
| DRK-02 | DOM-IAM;DOM-FIN;DOM-CMP | Security/privacy breach; DPA non-compliance | High | REQ-N-008..013;CON-005 | 64 |
| DRK-03 | DOM-FIN;DOM-TRADE | No accessible payment rail; financial integrity failure | High | REQ-F-079;BR-016 | 62 |
| DRK-04 | DOM-MINE;DOM-ENV;DOM-CMP | Statutory/regulatory breach; penalties | High | REQ-F-045;REQ-F-063;CON-006 | 60 |
| DRK-05 | DOM-MINE;DOM-CONS | Safety incidents; legal exposure | High | REQ-F-040;REQ-F-057 | 58 |
| DRK-06 | DOM-MSG;DOM-CMP | Government portal-first (few APIs) blocks automated integration | Medium | CON-007;GAP-I01 | 60 |
| DRK-07 | DOM-ANALYTICS;DOM-CFG | Poor data quality undermines insight/compliance | Medium | REQ-N-027;CON-012 | 54 |
| DRK-08 | DOM-NOTIF;DOM-EXT | Low adoption if channels/languages unsuitable | Medium | REQ-N-015;CON-002;CON-011 | 54 |
| DRK-09 | ALL | Domain-boundary erosion / duplicated responsibility over time | Medium | governance | 52 |
| DRK-10 | DOM-GEO | Imagery/data licensing or skills gaps limit spatial capability | Medium | GAP-T06;CON-004 | 50 |
| DRK-11 | DOM-FILE;DOM-AUDIT | Data loss without DR/backup and audit | Medium | REQ-N-016;REQ-N-017;REQ-N-019 | 50 |
| DRK-12 | DOM-HR;DOM-FIN | Payroll/tax miscompliance across jurisdictions | Medium | BR-007;REQ-F-081 | 52 |

## Output 12 — Domain Constraint Register
| Constraint ID | Domain(s) | Constraint | Source | Confidence |
|---------------|-----------|-----------|--------|------------|
| DCON-01 | ALL cores;DOM-NOTIF | Offline-first + feature-phone/USSD required | CON-001;CON-002;F-0078 | 68 |
| DCON-02 | DOM-IAM;DOM-CMP | Data Protection Act governs personal data (and possibly residency) | CON-005;REG-0024 | 62 |
| DCON-03 | DOM-CMP;DOM-ENV;DOM-MINE | Regulator-defined reporting formats/timelines | CON-006;F-0073 | 60 |
| DCON-04 | DOM-MSG;DOM-FIN | Gov portal-first APIs; bank/switch rails restricted; mobile money is accessible rail | CON-007;CON-008;F-0086 | 62 |
| DCON-05 | ALL | Limited digital literacy & in-house IT capacity | CON-010 | 56 |
| DCON-06 | ALL cores | Users distributed across provinces with variable coverage | CON-009 | 56 |
| DCON-07 | DOM-NOTIF;DOM-EXT | Multiple local languages | CON-011 | 54 |
| DCON-08 | ALL | Affordability/FX constraints favour OSS and low-cost SaaS | CON-004;F-0084 | 58 |
| DCON-09 | DOM-INV;DOM-MINE;DOM-CONS | Power/infrastructure reliability variable at sites | CON-003 | 54 |
| DCON-10 | DOM-ANALYTICS;DOM-CFG | Fragmented baseline data of variable quality | CON-012 | 54 |

## Discipline & uncertainties
Domains, contexts, events, and objects are **business-level** abstractions traced to evidence and requirements. No databases, APIs, events-for-implementation, microservices, cloud infrastructure, deployment diagrams, UI, UML class diagrams, or software modules are produced. Business objects list **business attributes only** (no data types, keys, or schema). Where evidence is thin (e.g., livestock/carbon), confidence is lowered and prior gaps (`GAP-C*`, `GAP-I*`, `GAP-RQ*`) are referenced rather than resolved by assumption.
