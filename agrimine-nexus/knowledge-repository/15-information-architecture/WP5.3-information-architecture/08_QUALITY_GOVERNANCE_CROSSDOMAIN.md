---
id: WP5.3-QUALITY-GOV
title: Information Quality, Governance & Cross-Domain Registers (WP5.3)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 5 — Enterprise Information & Data Architecture
work_package: WP5.3
industry: cross-industry
topic: Information quality, governance, cross-domain sharing
keywords: [data-quality, data-governance, stewardship, cross-domain, information-architecture]
summary: Outputs 12-14. Information Quality Register, Information Governance Register, and Cross-domain Information Matrix. Business information level only.
source: F-0077;F-0079;F-0086;F-0088;F-0092
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 68
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_ENTERPRISE_INFORMATION_CATALOGUE.csv, 06_MASTER_TRANSACTION_METADATA.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Information Quality, Governance & Cross-Domain (Outputs 12–14)

## Output 12 — Information Quality Register
| Dimension | Definition | Priority information | Business expectation | Linked requirement |
|-----------|-----------|----------------------|----------------------|--------------------|
| Accuracy | Correctly reflects reality | Payments; monitoring; production | Verified at capture | REQ-N-027;BR-019 |
| Completeness | Required data present | Farmer profile; permit; invoice | Mandatory fields enforced | REQ-N-027 |
| Consistency | Coherent across domains | Reference/master data | Single source of truth | REQ-N-021 |
| Timeliness | Available when needed | Weather; monitoring; transit | Within operational window | REQ-N-004;REQ-N-030 |
| Uniqueness | No duplicate records | Person; organisation; asset | De-duplicated identities | REQ-F-099 |
| Validity | Conforms to rules/reference | Coded fields; classifications | Validated vs reference data | REQ-N-027;REF-* |
| Traceability | Provenance to evidence | All objects | Evidence IDs recorded | REQ-N-024;F-0090 |
| Auditability | Actions reconstructable | Financial; compliance; identity | Immutable audit trail | REQ-F-094;REQ-N-019 |
> Data-quality is constrained by fragmented baseline data (`CON-012`); quality expectations are business-level, verified via the V&V plan (ACT-018).

## Output 13 — Information Governance Register
| Governance area | Policy statement (business level) | Owner | Linked |
|-----------------|-----------------------------------|-------|--------|
| Ownership & stewardship | Every information object has a single owning domain and named steward | DOM-CFG | ownership register |
| Approval | Financial/compliance/permit data requires defined approval before use | DOM-CMP/FIN | BR-008;BR-020 |
| Retention & disposition | Records retained per statutory/business rules then dispositioned | DOM-DOC | BR-002;lifecycle |
| Privacy & consent | Personal data processed only with lawful basis and consent | DOM-IAM | BR-001;REQ-N-013;REG-0024 |
| Classification & access | Information classified and access granted on least privilege | DOM-IAM | classification register;REQ-N-010 |
| Reference/master data | Controlled vocabularies centrally governed and versioned | DOM-CFG | REF-*;REQ-N-021 |
| Compliance reporting | Regulatory data reported in prescribed formats/timelines | DOM-CMP | BR-003/004/014;REQ-N-023 |
| Audit & accountability | Key actions logged immutably and retained | DOM-AUDIT | REQ-F-094;REQ-N-019 |
| Data sharing | Cross-domain/external sharing governed by consent and agreements | DOM-IAM/CMP | cross-domain matrix |

## Output 14 — Cross-Domain Information Matrix (which domains share which information)
| Information object | Owning domain | Also consumed by |
|--------------------|---------------|------------------|
| Person Identity (INFO-040) | DOM-IAM | ALL domains |
| Reference/Master Data (INFO-045) | DOM-CFG | ALL domains |
| Payment (INFO-014) | DOM-FIN | DOM-AGRI;DOM-TRADE;DOM-LOG;DOM-CMP |
| Land/Plot (INFO-002) | DOM-GEO | DOM-AGRI;DOM-MINE;DOM-CONS;DOM-ENV |
| Permit/Licence (INFO-027) | DOM-CMP | DOM-MINE;DOM-ENV;DOM-CONS |
| Env Monitoring (INFO-024) | DOM-ENV | DOM-MINE;DOM-CMP;DOM-ANALYTICS |
| Asset/Equipment (INFO-022) | DOM-INV | DOM-MINE;DOM-CONS;DOM-LOG |
| Inventory/Stock (INFO-038) | DOM-INV | DOM-AGRI;DOM-LOG;DOM-MINE |
| Order/Trade (INFO-013) | DOM-TRADE | DOM-AGRI;DOM-LOG;DOM-FIN |
| Weather (INFO-008) | DOM-EXT | DOM-AGRI;DOM-LOG;DOM-ENV |
| Audit Log (INFO-043) | DOM-AUDIT | DOM-CMP;DOM-IAM;ALL |
| Report/KPI (INFO-046) | DOM-ANALYTICS | ALL cores;DOM-CMP |
> Most-shared information: **identity, reference/master data, payments, spatial land data, permits, and audit** — mirroring the foundational domains identified in ACT-019 (`F-0093`).

## Information Gap Register (`GAP-IN-01`–`GAP-IN-08`)
| Gap ID | Gap | Notes |
|--------|-----|-------|
| GAP-IN-01 | Statutory retention periods stated at business level; exact schedules to confirm per regulator | verify with ZRA/ZEMA/MMMD |
| GAP-IN-02 | Personal-data inventory completeness depends on DPA lawful-basis confirmation | tie to REQ-N-013 |
| GAP-IN-03 | Livestock/aquaculture information thinly evidenced | lower confidence (INFO-009) |
| GAP-IN-04 | Reference-data authoritative source lists to be confirmed (e.g., admin areas, crop lists) | verify with GRZ/MoA |
| GAP-IN-05 | Some information objects lack a confirmed named steward organisationally | assign stewards on adoption |
| GAP-IN-06 | Data-quality baselines (current accuracy/completeness) unknown | measure during operation |
| GAP-IN-07 | Cross-border data-sharing/residency rules for logistics/customs to confirm | tie to CON-005;GAP-I06 |
| GAP-IN-08 | Attribute catalogue covers core entities, not exhaustively all entities | expand as needed (no invention) |

## Discipline & uncertainties
All objects are **business information**, not schemas. No SQL/tables/Firestore/PostgreSQL/APIs/GraphQL/REST/cloud/UI/classes/DTOs. Every information object traces to evidence, requirement, capability, workflow, stakeholder, and business domain; every entity has >=1 relationship; every relationship carries evidence. Uncertain items are recorded as gaps (`GAP-IN-*`) rather than invented.
