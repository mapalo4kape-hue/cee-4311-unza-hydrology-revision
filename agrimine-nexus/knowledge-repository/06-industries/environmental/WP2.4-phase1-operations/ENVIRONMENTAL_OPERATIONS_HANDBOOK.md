---
id: WP2.4-P1-HANDBOOK
title: Environmental Engineering Operations Handbook — Zambia (WP2.4 Phase 1)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research (breadth-first sprint)
work_package: WP2.4
industry: TAX-IND.4 (Environmental Engineering)
topic: Environmental operations intelligence
keywords: [environment, ZEMA, EIA, WARMA, NWASCO, monitoring, workflows]
summary: High-level operational intelligence for Zambian environmental engineering using the Agriculture framework. Contains all 9 sprint outputs. Evidence-first; no software, features, competitors, or AI.
source: SRC-0069;SRC-0070;SRC-0012
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 82
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../../../02-evidence/EVIDENCE_REGISTER.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: [WF-E01..WF-E12]
---

# Environmental Engineering Operations Handbook — Zambia

> Breadth-first, high-level; same framework as Agriculture. The 9 sprint outputs appear as numbered sections.

## Output 1 — Industry Overview
- **Value chain:** Screening (Project Brief) → Environmental & Social Impact Assessment (ESIA) → Decision/authorisation → Environmental Management Plan implementation → Monitoring & measurement (air/water/soil/noise/waste) → Compliance auditing & reporting → Remediation/rehabilitation [SRC-0069] (ZEMA, pub. 2011; confidence 86/100; retrieved 2026-07-05).
- **EIA process (cited):** developer submits **Project Brief → ZEMA screening →** (if required) **ZEMA-registered consultant prepares EIS → ZEMA review → decision letter** (approve with/without conditions, amend, or refuse); then monitoring plan, environmental audit **12–36 months** post-completion, and **annual reports** to ZEMA [SRC-0069]; governed by **EIA Regulations SI No. 3 of 2026** (replaced 1997 regs) [SRC-0070] (Global Law Experts/NCEA, pub. 2026; confidence 78/100; retrieved 2026-07-05).
- **Key regulators/bodies:** **ZEMA** (Environmental Management Act No. 12 of 2011; central authority for EIA/SEA, pollution control, `Central Environmental Information System` s.87) [SRC-0069]; **WARMA** (Water Resources Management Act No. 21 of 2011; water permits via My-WARMA) [SRC-0070]; **NWASCO** (water supply & sanitation utilities); local authorities (solid waste); **ZABS** (standards); **Data Protection** (WP1.1) for personal data.
- **Typical organisations:** ZEMA-registered EIA/environmental consultants; accredited environmental laboratories; water/wastewater utilities (commercial utilities under NWASCO); waste-management operators (local authorities/private); mines, factories, and infrastructure projects as regulated proponents; monitoring/instrumentation providers.
- **Operational structure:** compliance-driven and project/asset-based; heavy reliance on **licensed consultants and accredited labs**; strong overlap with mining, construction, water, and agriculture as regulated sectors.

## Output 2 — Workflow Library (WF-E01..WF-E12)
| ID | Workflow | Purpose | Key actors | Key docs | Assets | Pain/risk | KPI | Cited |
|----|----------|---------|-----------|----------|--------|-----------|-----|-------|
| WF-E01 | Screening (project brief) | Determine EIA need | Proponent, ZEMA | project brief, screening decision | — | delays; scoping | screening time | [SRC-0069] |
| WF-E02 | Scoping & ESIA study | Assess impacts | ZEMA-registered consultant | ToR, EIS/ESIA report | field kit, labs | data quality; independence | EIS completeness | [SRC-0069] |
| WF-E03 | Baseline data collection | Establish baseline | Consultant, labs | baseline data | samplers, monitors | access; lab capacity | baseline coverage | [SRC-0070] |
| WF-E04 | ZEMA review & decision | Authorise/refuse | ZEMA | decision letter | — | review timeframes | decision time | [SRC-0069] |
| WF-E05 | Environmental Management Plan (EMP) implementation | Manage impacts | Proponent, SHE | EMP, impact mgmt plan | controls | resourcing; adherence | EMP compliance | [SRC-0069] |
| WF-E06 | Water-resource permitting | Abstraction/impoundment rights | Proponent, WARMA | water permit (My-WARMA) | boreholes, meters | permit delays; monitoring | permit status | [SRC-0070] |
| WF-E07 | Effluent & wastewater management | Treat/discharge safely | Utility/operator, lab | discharge licence, results | WWTP, samplers | capacity; compliance | effluent compliance | [SRC-0070] |
| WF-E08 | Air-quality monitoring | Measure emissions | Consultant/operator, lab | monitoring report | analysers, diffusion tubes | equipment; standards | exceedances | [SRC-0070] |
| WF-E09 | Solid & hazardous waste management | Handle/dispose waste | Local authority/operator | waste manifests | trucks, landfill, recycling | capacity; producer duty (s.58) | waste diverted | [SRC-0069] |
| WF-E10 | Environmental monitoring (water/soil/noise) | Track conditions | Consultant/operator, lab | monitoring data | sensors, labs | station sparsity; data mgmt | monitoring cadence | [SRC-0070] |
| WF-E11 | Compliance audit & reporting | Verify conformance | Proponent, ZEMA | audit report, annual report | — | audit backlog; data | audit pass rate | [SRC-0069] |
| WF-E12 | Remediation & rehabilitation | Restore environment | Proponent, ZEMA | rehab plan, records | earthmoving, revegetation | cost; closure liability | rehab progress | [SRC-0069] |
*(Cross-cutting planning/procurement/operations/inventory/asset/workforce/safety/compliance/reporting/logistics/finance/close-out represented via EMP, monitoring, audit, and rehabilitation flows.)*

## Output 3 — Stakeholder Register
| Stakeholder | Role / responsibilities | Decisions | Info used | Pain points | Interactions |
|-------------|-------------------------|-----------|-----------|-------------|--------------|
| ZEMA | Regulate EIA/SEA, pollution, monitoring | screening, approval, enforcement | project briefs, EIS, monitoring | capacity, audit backlog, data | proponents, consultants, labs, other regulators |
| ZEMA-registered EIA consultant | Prepare ESIA & monitoring | study methods, findings | baseline, standards | data access, timelines, independence | proponent, ZEMA, labs |
| Accredited environmental laboratory | Analyse samples | test methods | samples | accreditation, capacity | consultants, operators |
| Proponent (mine/factory/project) | Comply, implement EMP | mitigation, monitoring | EMP, conditions | cost, compliance burden | ZEMA, WARMA, community |
| WARMA | Water-resource permits & monitoring | grant permits | abstraction, hydrogeology | monitoring data, capacity | proponents, ZEMA |
| NWASCO | Regulate water/sanitation utilities | tariffs, standards | utility data | utility performance | utilities |
| Water/wastewater utility | Supply water; treat effluent | operations | quality, demand | infrastructure, power | NWASCO, WARMA, ZEMA |
| Local authority (waste) | Manage municipal waste | collection, disposal | waste volumes | capacity, funding | operators, community |
| Waste operator (private) | Collect/treat/recycle waste | logistics | manifests | capacity, markets | local authority, producers |
| Community / affected public | Participate, raise grievances | consent, complaints | impact info | health, environment, information | ZEMA, proponent |
| Other regulators (MRC, NCC, local authority) | Sector approvals needing ZEMA input | permits | project info | coordination | ZEMA (integrated decisions) |

## Output 4 — Information Catalogue
- **Master data:** Project/facility (regulated), Proponent, EIA consultant (ZEMA-registered), Laboratory (accredited), Monitoring point/station, Water permit, Discharge licence, Waste facility, Environmental standard/parameter, Location/catchment.
- **Transactions:** Project brief submission, screening decision, ESIA submission, ZEMA review/decision, water-permit application (My-WARMA), monitoring reading, sample & lab result, discharge report, waste manifest, environmental audit, annual compliance report.
- **Documents:** Project Brief, ToR, EIS/ESIA report, decision letter, EMP/impact-management plan, water permit, discharge licence, monitoring reports, laboratory reports, audit reports, annual reports, State of Environment Reports (ZEMA).
- **Measurements:** Air (SO₂, NOₓ, PM, O₃), water/effluent (pH, BOD, COD, phosphates, heavy metals, coliforms), noise (dB), soil contaminants, meteorology (wind, temp), groundwater level & quality, waste volumes, emissions [SRC-0070].
- **Events:** Brief submitted, screening decided, EIS submitted, decision issued, permit granted, monitoring exceedance, audit conducted, incident/spill, remediation milestone.
- **Reports:** ESIA report, monitoring reports, environmental audit, annual compliance report, State of Environment Report.

## Output 5 — Operational Asset Register
Air-quality analysers & passive diffusion tubes; water/effluent samplers & multiparameter probes; noise meters; monitoring boreholes; weather/meteorological sensors; accredited laboratory (wet chemistry, instruments); wastewater treatment plants; waste-collection trucks; landfills/transfer stations; recycling facilities; GIS/mapping; field survey kit.

## Output 6 — Document Register
Project Brief; Terms of Reference; EIS/ESIA report; ZEMA decision letter; Environmental Management Plan; water permit (WARMA); discharge licence; laboratory reports; monitoring reports; environmental audit reports; annual compliance reports; waste manifests; State of Environment Reports.

## Output 7 — Pain Point Register (no solutions)
| ID | Pain point | Type |
|----|-----------|------|
| PP-E01 | EIA/permit review & approval delays | Delay/compliance [SRC-0069] |
| PP-E02 | Monitoring-station sparsity & data gaps | Data |
| PP-E03 | Paper/siloed monitoring & audit records | Manual/data |
| PP-E04 | Limited accredited-lab capacity | Resource |
| PP-E05 | Compliance & reporting burden (audits, annual reports) | Compliance [SRC-0069] |
| PP-E06 | Weak enforcement / late detection of exceedances | Compliance |
| PP-E07 | Duplicate data across regulators (ZEMA/WARMA/local authority) | Data duplication |
| PP-E08 | Waste-management capacity & funding | Resource |
| PP-E09 | Water-permit & groundwater-monitoring obligations | Compliance [SRC-0070] |
| PP-E10 | Community information/grievance handling | Communication |
| PP-E11 | Power/utility reliability affecting treatment | Resource |
| PP-E12 | Rehabilitation/closure funding & liability | Financial |

## Output 8 — KPI Register
Screening/decision turnaround; EIS review time; EMP compliance rate; monitoring cadence & coverage; parameter exceedance count; effluent/air compliance %; audit pass rate; annual-report timeliness; permit status; waste diverted/recycled; incidents/spills; rehabilitation progress.

## Output 9 — Knowledge Graph Updates
Findings `F-0060` (ZEMA/EMA/EIA process), `F-0061` (WARMA/NWASCO & environmental monitoring) added; workflow nodes `WF-E01..WF-E12`; entities `ENT-EIA`, `ENT-MONITORING`, `ENT-ENVSAMPLE`, `ENT-LABORATORY`, `ENT-PERMIT` (shared graph CSVs). Relationships: Proponent `SUBMITS` Project Brief `TO` ZEMA; ZEMA `ISSUES` decision letter; Proponent `GOVERNED_BY` EMP conditions; Lab `ANALYSES` sample; WARMA `ISSUES` water permit.

## Recorded uncertainties
Utility- and lab-internal SOPs, ZEMA information-system content, and monitoring-network extent require primary collection (deferred). SI No.3 of 2026 is recent — procedural timelines still bedding in.
