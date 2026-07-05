---
id: WP2.3-P1-HANDBOOK
title: Construction Industry Operations Handbook — Zambia (WP2.3 Phase 1)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research (breadth-first sprint)
work_package: WP2.3
industry: TAX-IND.3 (Construction)
topic: Construction operations intelligence
keywords: [construction, NCC, procurement, project-lifecycle, BOQ, workflows]
summary: High-level operational intelligence for Zambian construction using the Agriculture framework. Contains all 9 sprint outputs. Evidence-first; no software, features, competitors, or AI.
source: SRC-0067;SRC-0068;SRC-0021;SRC-0035
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 80
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
related_workflows: [WF-C01..WF-C13]
---

# Construction Industry Operations Handbook — Zambia

> Breadth-first, high-level; same framework as Agriculture. The 9 sprint outputs appear as numbered sections.

## Output 1 — Industry Overview
- **Value chain:** Project origination → Feasibility/design → Statutory approvals (planning permission, ZEMA where required) → Procurement/tender → Contractor selection → Construction/site works → Inspection & quality → Handover (completion/occupancy certificate) → Operation/maintenance [SRC-0068] (PCLP, pub. 2024; confidence 76/100; retrieved 2026-07-05).
- **Market size:** construction is part of the industry sector (~35% of GDP with mining/manufacturing; construction a major sub-sector — see WP1.1 economic register). Corridor/infrastructure programmes drive demand (WP1.1 logistics).
- **Key regulators/bodies:** **National Council for Construction (NCC)** — NCC Act No. 13 of 2003, registers & grades contractors and regulates the industry [SRC-0067] (NCC, pub. 2024; confidence 84/100; retrieved 2026-07-05); **local planning authorities** (city/municipal councils) for development approval and occupancy certificates [SRC-0068]; **ZPPA** (public procurement, e-GP); **Engineering Institution of Zambia / Engineers Registration Board** (professionals, WP1.1 SRC-0021); **ZEMA** (environmental clearance where required); **RDA** (roads, SRC-0035).
- **Typical organisations:** clients (government via ZPPA, private developers); consultants (architects, engineers, quantity surveyors); NCC-graded contractors (Grades 1–6; categories Building/Civil/Road/Electrical/Mechanical/Specialist A–B); subcontractors; material suppliers/manufacturers; equipment-hire firms.
- **Operational structure:** project-based; contractors must operate **within their registered grade/category** (grade sets max tender value); foreign contractors restricted to grades 1, 2, A [SRC-0067].

## Output 2 — Workflow Library (WF-C01..WF-C13)
| ID | Workflow | Purpose | Key actors | Key docs | Assets | Pain/risk | KPI | Cited |
|----|----------|---------|-----------|----------|--------|-----------|-----|-------|
| WF-C01 | Project origination & feasibility | Define viable project | Client, consultants | brief, feasibility | — | scope/funding uncertainty | projects initiated | [SRC-0068] |
| WF-C02 | Design & BOQ | Produce design & quantities | Architect, engineer, QS | drawings, BOQ, specs | CAD | design errors; rework | design completeness | [SRC-0068] |
| WF-C03 | Statutory approvals | Obtain planning/ZEMA | Client, local authority, ZEMA | planning approval, EIA | — | approval delays | approval time | [SRC-0068] |
| WF-C04 | Procurement & tender | Select contractor | Client, ZPPA, bidders | tender docs, bids | e-GP portal | irregularities; delays | tender cycle time | [SRC-0068] |
| WF-C05 | Contractor registration/verification | Ensure NCC compliance | Contractor, NCC | NCC certificate | NCC portal | unregistered firms | compliant contractors | [SRC-0067] |
| WF-C06 | Contract award & mobilisation | Start project | Client, contractor | contract, bonds | — | cash flow; mobilisation | mobilisation time | [SRC-0068] |
| WF-C07 | Site operations & construction | Build the works | Site manager, workers, subs | site diary, drawings | plant, tools | weather, labour, materials | progress vs plan | [SRC-0068] |
| WF-C08 | Procurement of materials & inventory | Supply site | QS, storekeeper, suppliers | PO, delivery note, stock card | store, plant | material price/availability | material availability | [SRC-0068] |
| WF-C09 | Equipment & plant management | Keep plant running | Plant manager, hire firms | plant register, service log | cranes, mixers, excavators | breakdown; hire cost | plant uptime | — |
| WF-C10 | Workforce & safety mgmt | Manage/protect labour | Site manager, SHE | attendance, permits | PPE | injuries; skills; labour law | LTIFR; productivity | — |
| WF-C11 | Quality assurance & inspection | Meet standards/plans | Engineer, clerk of works, authority | inspection reports, tests | test equipment, labs | defects; non-conformance | defect rate | [SRC-0068] |
| WF-C12 | Progress claims, valuations & finance | Pay for work done | QS, client, contractor | valuation, IPC, invoice | — | payment delays; disputes | payment turnaround | [SRC-0068] |
| WF-C13 | Handover & close-out | Complete & certify | Client, contractor, authority | completion/occupancy cert, snag list | — | defects liability; retention | close-out time | [SRC-0068] |
*(Cross-cutting planning/procurement/operations/inventory/asset/workforce/safety/compliance/reporting/logistics/finance/close-out all represented.)*

## Output 3 — Stakeholder Register
| Stakeholder | Role / responsibilities | Decisions | Info used | Pain points | Interactions |
|-------------|-------------------------|-----------|-----------|-------------|--------------|
| Client / developer (public/private) | Commission & fund project | scope, budget, award | feasibility, cost | funding, delays, quality | consultants, contractor, ZPPA |
| Architect | Design & aesthetics | design decisions | brief, codes | changes, coordination | client, engineers |
| Structural/civil/services engineer | Technical design & supervision | design, approvals | loads, standards | rework, site issues | architect, contractor |
| Quantity surveyor (QS) | Cost, BOQ, valuations | rates, valuations | BOQ, prices | price volatility, claims | client, contractor |
| Contractor (NCC-graded) | Execute works | methods, resourcing | drawings, BOQ, program | cash flow, materials, labour | client, subs, suppliers, NCC |
| Subcontractor | Specialist works | trade methods | drawings | payment, coordination | contractor |
| Site manager / foreman | Run the site | daily works, labour | program, drawings | weather, labour, materials | crews, engineer |
| SHE officer | Site safety | controls, stop-work | incidents | injuries, compliance | workers, authority |
| NCC | Register/grade & regulate | registration, grade | contractor data | unregistered firms, capacity | contractors |
| Local planning authority | Approvals & occupancy | permits, certificates | plans | approval delays | client, contractor |
| ZPPA | Public procurement rules | tender compliance | bids, thresholds | irregularities | client, bidders |
| ZEMA | Environmental clearance | approvals | EIA | compliance | client, contractor |
| Material supplier / manufacturer | Supply materials | orders, delivery | specs, quantities | payment, lead times | contractor, QS |
| Equipment-hire firm | Provide plant | hire, service | schedules | utilisation, spares | contractor |
| Financier / bank | Project/works finance | credit, guarantees | valuations | risk, security | client, contractor |

## Output 4 — Information Catalogue
- **Master data:** Project, Client, Contractor (NCC grade/category), Consultant, Subcontractor, Supplier, Material item, Plant/equipment, Employee, Site, Contract, BOQ item, Location/plot.
- **Transactions:** Project registration, planning-approval application, tender submission/award, contractor registration, purchase order, material delivery (GRN), site-work record, inspection/test, progress valuation (IPC), payment, variation order, snag/defect.
- **Documents:** Drawings/specs, BOQ, tender documents, bids, contract (e.g. FIDIC-type), bonds/guarantees, planning approval, EIA, delivery notes, inspection/test reports, interim payment certificates (IPC), variation orders, completion/occupancy certificate, snag list.
- **Measurements:** Quantities (m³ concrete, m² area, tonnes steel), progress %, cost/earned value, material stock, plant hours, labour hours, test results (strength, compaction), defects count.
- **Events:** Approval granted, contract awarded, mobilisation, milestone reached, inspection passed/failed, variation issued, payment certified, practical completion, handover.
- **Reports:** Progress reports, cost reports, safety statistics, quality/NCR reports, valuation reports, project close-out report.

## Output 5 — Operational Asset Register
Excavators; loaders; graders; rollers/compactors; cranes; concrete mixers/batching plant; dumpers/tippers; scaffolding; formwork; hand & power tools; surveying instruments (total station, GPS); testing equipment (concrete/soil labs); site offices/stores; temporary services; safety equipment/PPE.

## Output 6 — Document Register
BOQ; drawings & specifications; tender documents & bids; construction contract & bonds; planning approval & building permits; EIA/ZEMA clearance; NCC registration certificate; delivery notes/GRNs; inspection & materials-test reports; interim payment certificates; variation orders; completion & occupancy certificates; defects/snag lists; retention records.

## Output 7 — Pain Point Register (no solutions)
| ID | Pain point | Type |
|----|-----------|------|
| PP-C01 | Planning/EIA approval delays | Delay/compliance [SRC-0068] |
| PP-C02 | Payment delays & disputes (esp. public works) | Financial |
| PP-C03 | Material price volatility & availability | Resource |
| PP-C04 | Use of unregistered/under-graded contractors | Compliance [SRC-0067] |
| PP-C05 | Paper-based site records; data duplication | Manual/data |
| PP-C06 | Design changes & rework | Waste |
| PP-C07 | Plant downtime & spares | Resource |
| PP-C08 | Skilled-labour shortages | Workforce |
| PP-C09 | Weather/seasonal disruption (rainy season) | Delay |
| PP-C10 | Procurement irregularities / tender delays | Compliance |
| PP-C11 | Quality defects & weak inspection trail | Quality |
| PP-C12 | Fragmented communication (client-consultant-contractor) | Communication |

## Output 8 — KPI Register
Schedule variance (progress vs plan); cost variance / earned value; payment turnaround; material availability; plant uptime; labour productivity; defect/NCR rate; LTIFR; approval/tender cycle time; variation count/value; retention released; close-out time.

## Output 9 — Knowledge Graph Updates
Finding `F-0059` (NCC grading, permits, procurement) added; workflow nodes `WF-C01..WF-C13`; entities `ENT-PROJECT`, `ENT-BOQ`, `ENT-SITE`, `ENT-MATERIAL`, `ENT-CONTRACTOR` (shared graph CSVs). Relationships: Client `CONTRACTS` Contractor (`GOVERNED_BY` NCC/ZPPA); Project `HAS` BOQ; Contractor `REGISTERED_IN` NCC; Project `GOVERNED_BY` local authority & ZEMA.

## Recorded uncertainties
Firm-level project-management tools and public-sector procurement data need primary collection (deferred). FIDIC/standard-form contract prevalence to be confirmed.
