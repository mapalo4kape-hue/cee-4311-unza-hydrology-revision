---
id: WP5-RULES
title: Business Rules, Constraints, Assumptions & User Goals (WP5)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 5 (transition) — Requirements Engineering
work_package: WP5
industry: cross-industry
topic: Business rules, constraints, assumptions, user goals
keywords: [business-rules, constraints, assumptions, user-goals, requirements, traceability]
summary: Outputs 3-6. Business Rules Catalogue, Constraints Register, Assumptions Register, and User Goal Catalogue. Requirements engineering only — no architecture, database, API, or UI design.
source: F-0053;F-0073;F-0077;F-0078;F-0084;F-0086
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 68
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_FUNCTIONAL_REQUIREMENTS.csv, 02_NON_FUNCTIONAL_REQUIREMENTS.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Business Rules, Constraints, Assumptions & User Goals (Outputs 3–6)

> Requirements engineering only. Rules/constraints trace to evidence; **assumptions are clearly separated** from verified evidence with rationale, confidence, and a verification plan. No architecture, database, API, or UI design.

## Output 3 — Business Rules Catalogue
| Rule ID | Type | Rule | Source (REG/F) | Linked REQ | Confidence |
|---------|------|------|----------------|------------|------------|
| BR-001 | Regulatory | Personal data may only be processed with a lawful basis and recorded consent | REG-0024 | REQ-F-105;REQ-N-013 | 62 |
| BR-002 | Data-retention | Records shall be retained for statutory periods then dispositioned | REG-0024;REG-0027 | REQ-F-087;REQ-N-017 | 56 |
| BR-003 | Regulatory | Mining production and royalties shall be reported per statutory schedule | REG-0009;REG-0010 | REQ-F-045 | 60 |
| BR-004 | Compliance | Environmental monitoring exceedances shall be reportable to ZEMA | REG-0017;REG-0018 | REQ-F-043;REQ-F-063 | 58 |
| BR-005 | Regulatory | Water abstraction/discharge requires a valid WARMA permit | REG-0019 | REQ-F-043;REQ-F-063 | 56 |
| BR-006 | Calculation | Tax (VAT/PAYE) shall be computed per prevailing rates | REG-0026;REG-0028 | REQ-F-080;REQ-F-081 | 58 |
| BR-007 | Calculation | Payroll deductions shall include NAPSA and statutory contributions | REG-0035;REG-0027 | REQ-F-081 | 56 |
| BR-008 | Approval | Procurement above a threshold requires defined approval levels | REG-0029 | REQ-F-082;REQ-F-093 | 54 |
| BR-009 | Validation | Warehouse receipt quantity shall not exceed verified stored stock | REG-0012 | REQ-F-012;REQ-F-013 | 56 |
| BR-010 | Workflow | Permit-to-work shall be approved before high-risk work begins | REG-0034 | REQ-F-042 | 54 |
| BR-011 | Compliance | Safety incidents above severity threshold shall be reported to the regulator | REG-0034 | REQ-F-040;REQ-F-057 | 56 |
| BR-012 | Validation | Agrochemical application records shall reference an approved product | REG-0016 | REQ-F-008 | 52 |
| BR-013 | Calculation | Interim payment certificate = measured work value minus retention and prior payments | F-0060 | REQ-F-052 | 54 |
| BR-014 | Reporting | Statutory/financial reports shall use prescribed formats | REG-0028 | REQ-F-090;REQ-N-023 | 54 |
| BR-015 | Regulatory | Mining licences and cadastre submissions shall follow Mines Act procedure | REG-0009 | REQ-F-045 | 58 |
| BR-016 | Validation | Financial postings shall balance (double-entry) | REG-0027 | REQ-F-076 | 60 |
| BR-017 | Compliance | Cross-border movements shall have valid customs documentation | REG-0030 | REQ-F-074 | 54 |
| BR-018 | Workflow | Subsidy/e-voucher redemption shall be validated against beneficiary eligibility | REG-0013 | REQ-F-021 | 54 |
| BR-019 | Validation | Payment disbursement shall verify recipient mobile-money/bank details | REG-0031 | REQ-F-022;REQ-F-078 | 56 |
| BR-020 | Audit | All financial and compliance actions shall be recorded in the audit trail | REG-0024 | REQ-F-094;REQ-N-019 | 58 |

## Output 4 — Constraints Register
| Constraint ID | Type | Constraint | Source (F) | Linked REQ | Confidence |
|---------------|------|------------|------------|------------|------------|
| CON-001 | Connectivity | Rural connectivity is intermittent; offline operation is mandatory for field use | F-0078 | REQ-N-001;REQ-N-029 | 70 |
| CON-002 | Device | Many end users are on feature phones/low-end devices | F-0078 | REQ-N-015;REQ-F-092 | 66 |
| CON-003 | Infrastructure | Power reliability is variable; edge/on-prem must tolerate outages | F-0078 | REQ-N-016;REQ-N-026 | 58 |
| CON-004 | Cost | Foreign-currency SaaS/licensing is a barrier; low willingness/ability to pay at smallholder tier | F-0084 | REQ-N-026 | 60 |
| CON-005 | Legal | Data Protection Act governs personal-data processing and possibly residency | F-0077 | REQ-N-013;REQ-N-014 | 60 |
| CON-006 | Legal | Sector regulators (ZEMA/WARMA/Mines/ZRA) mandate reporting formats/timelines | F-0073 | REQ-N-023;REQ-F-063 | 58 |
| CON-007 | Operational | Government access is portal-first with few open APIs; integration may be manual | F-0087 | REQ-N-024;REQ-N-025 | 62 |
| CON-008 | Operational | Bank/central-switch rails are regulated/restricted; mobile money is the accessible rail | F-0086 | REQ-F-079;REQ-N-025 | 62 |
| CON-009 | Geographic | Users are distributed across provinces with varying coverage | F-0078 | REQ-N-007;REQ-N-029 | 56 |
| CON-010 | Skills | Digital literacy and in-house IT capacity are limited | F-0084 | REQ-N-015;REQ-N-021 | 56 |
| CON-011 | Language | Multiple local languages in use (Bemba/Nyanja/Tonga/Lozi etc.) | F-0078 | REQ-N-022;REQ-F-106 | 54 |
| CON-012 | Data | Baseline datasets are fragmented and of variable quality | F-0079 | REQ-N-027 | 54 |

## Output 5 — Assumptions Register (separated from verified evidence)
| Assumption ID | Assumption | Rationale | Confidence | Verification plan |
|---------------|-----------|-----------|------------|-------------------|
| ASM-001 | Mobile-money APIs (MTN/Airtel) are commercially obtainable for integration | Vendors publish developer portals; widely integrated in region | 60 | Obtain sandbox/production terms; confirm coverage (`GAP-I03`) |
| ASM-002 | ZamPass/ZamPay/GSB expose an integration path for accredited parties | Government Service Bus exists and connects agencies | 50 | Request technical specs from Smart Zambia (`GAP-I04`) |
| ASM-003 | Open EO data (Copernicus/USGS/NASA) remains free for operational use | Longstanding open-data policies | 66 | Re-check licensing terms periodically (`GAP-I06`) |
| ASM-004 | Weather data adequate for advisory is obtainable (open or licensed) | Multiple providers with free tiers | 58 | Evaluate ZMD terms and API providers |
| ASM-005 | Target users have at least feature-phone access and mobile-money accounts | High mobile/mobile-money penetration nationally | 64 | Confirm via field baseline in target segments |
| ASM-006 | Regulatory reporting formats can be satisfied by configurable reports | Regulators publish templates | 52 | Validate exact formats with each regulator |
| ASM-007 | Local-language content can be produced/maintained for key advisories | Existing services use local languages | 54 | Assess translation/ASR-TTS feasibility (`GAP-T02`) |
| ASM-008 | Intermittent-connectivity offline-first patterns are technically sufficient | Established OSS offline-sync stacks exist | 62 | Prototype/field-test sync under real conditions |
| ASM-009 | Existing sector software can interoperate via files/APIs where needed | Most enterprise products expose APIs/exports | 56 | Confirm per target integration (`GAP-M08`) |
| ASM-010 | Statutory rates/thresholds (tax/royalty) are obtainable and updatable | Published by ZRA/Ministry | 58 | Maintain reference-rate configuration |

## Output 6 — User Goal Catalogue (per stakeholder group)
| Stakeholder group | Objectives | Responsibilities | Information needs | Success measures |
|-------------------|-----------|------------------|-------------------|------------------|
| Smallholder farmers (STK-028) | Improve yields/income; access inputs/finance/markets | Record activities; follow advisories | Weather/prices/advisory; input availability | Yield/income up; timely inputs |
| Commercial farmers/agribusiness (STK-029) | Optimise operations & compliance | Manage farm ops/finance/staff | Operational KPIs; compliance status | Cost/ha down; compliance met |
| Agro-dealers (STK-032) | Sell inputs; manage stock/credit | Stock/sales/credit management | Demand; stock; farmer credit | Sales up; low stockouts |
| Cooperatives (STK-031) | Aggregate produce; bulk inputs; access finance | Member & aggregation mgmt | Membership; volumes; receipts | Aggregated volume; finance secured |
| Mines & engineers/geologists (STK-039;STK-047) | Safe, compliant, efficient production | Plan/operate/report | Geology; plans; production; safety/env | Production targets; zero major incidents; compliance |
| Contractors/consultants (STK-041;STK-048;STK-050) | Deliver projects on time/cost/quality | Site ops; QA/QC; HSE; docs | Progress; BOQ; valuations; safety | On-time/on-budget; quality; safety |
| Environmental regulators (STK-010) | Ensure compliance & protection | Review EIA; monitor; enforce | Monitoring data; permits; reports | Compliance rates; timely reporting |
| Fleet/logistics operators (STK-055) | Move goods efficiently/reliably | Dispatch; fleet; warehouse | Orders; routes; vehicle/stock status | On-time delivery; utilisation |
| Financial institutions/MMO (STK-060;STK-062;STK-069) | Extend/settle finance safely | Score; lend; settle payments | Creditworthiness; transaction data | Portfolio quality; settlement reliability |
| Government agencies (STK-001;STK-009;STK-022;STK-023) | Administer/regulate; collect revenue | Registries; licensing; oversight | Registrations; compliance; statistics | Coverage; compliance; revenue |
| IT/administrators (STK-029;STK-070) | Operate the platform securely | Config; access; data quality | Health; access; usage | Uptime; security; data quality |
