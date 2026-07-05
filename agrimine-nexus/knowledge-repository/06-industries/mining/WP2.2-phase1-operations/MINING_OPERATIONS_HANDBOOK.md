---
id: WP2.2-P1-HANDBOOK
title: Mining Industry Operations Handbook — Zambia (WP2.2 Phase 1)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research (breadth-first sprint)
work_package: WP2.2
industry: TAX-IND.2 (Mining)
topic: Mining operations intelligence
keywords: [mining, operations, MRC, copper, ASM, workflows, stakeholders]
summary: High-level operational intelligence for Zambian mining using the Agriculture framework. Contains all 9 sprint outputs. Evidence-first; no software, features, competitors, or AI.
source: SRC-0017;SRC-0064;SRC-0065;SRC-0066
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
related_workflows: [WF-M01..WF-M14]
---

# Mining Industry Operations Handbook — Zambia

> Breadth-first, high-level. Same framework as Agriculture. The 9 sprint outputs appear as numbered sections. Zambia-specific facts cited; generic mining operations are consultant synthesis.

## Output 1 — Industry Overview
- **Value chain:** Exploration → Mineral-rights licensing → Mine development → Extraction (open-pit / underground) → Processing (crushing, milling, flotation → concentrate; smelting; SX/EW; refining → cathode) → Tailings management → Transport & export; plus progressive rehabilitation/closure [SRC-0066] (FQM/Mopani/MMMD, pub. 2024; confidence 80/100; retrieved 2026-07-05).
- **Market size:** mining & quarrying ~**19.4% of real GDP**, ~**49% of non-tax government revenue**, and ~**47% of national electricity** consumption; copper dominates exports [SRC-0065] (USGS, pub. 2023; confidence 84/100; retrieved 2026-07-05).
- **Key regulators:** **Minerals Regulation Commission (MRC)** — autonomous, under the **Minerals Regulation Commission Act No. 14 of 2024** (repealed the Mines & Minerals Development Act No. 11 of 2015), consolidating the former Directors of Mines, Mines Safety, Geological Survey, and Mining Cadastre; **Geological & Minerals Development Act 2025** (geological survey + ASM formalisation); **ZEMA** (environment/rehabilitation); **ZRA** (mineral royalty); **ZCCM-IH** (state investment vehicle) [SRC-0064] (ICLG/Dentons, pub. 2026; confidence 82/100; retrieved 2026-07-05); [SRC-0065].
- **Typical organisations:** large-scale mines (e.g. open-pit Kansanshi, Sentinel, Lumwana; underground Mopani; integrated KCM); smelters/refineries; contractors; equipment/OEM suppliers; **artisanal & small-scale miners (ASM)** organised into cooperatives (reserved for Zambian citizens) [SRC-0066].
- **Operational structure:** capital-intensive large-scale sector (mechanised, 24/7 shift operations, integrated processing) alongside a **formalising ASM subsector** (cooperatives, ASM Fund, safety/health/environment capacity building) [SRC-0066].

## Output 2 — Workflow Library (WF-M01..WF-M14)
| ID | Workflow | Purpose | Key actors | Key docs | Assets | Pain/risk | KPI | Cited |
|----|----------|---------|-----------|----------|--------|-----------|-----|-------|
| WF-M01 | Exploration & geological survey | Locate/define deposits | Geologist, MRC/Geological Survey | exploration licence, survey data | drill rigs, GIS | tenure/data; long lead | resource defined | [SRC-0064] |
| WF-M02 | Mineral-rights licensing | Obtain/maintain rights | Company, MRC (cadastre) | licence, cadastre record | cadastre portal | overlaps; renewals | licence status | [SRC-0017][SRC-0064] |
| WF-M03 | Mine planning & design | Plan extraction | Mine planner, engineers | mine plan | planning software | grade/geo risk | plan adherence | [SRC-0066] |
| WF-M04 | Procurement & contractor mgmt | Source goods/services | Procurement, suppliers, contractors | PO, contract | ERP | local-content rules; lead times | on-time supply | [SRC-0064] |
| WF-M05 | Drilling & blasting | Break ore/rock | Drill & blast crew | blast permit, records | rigs, explosives | safety; vibration | m drilled; fragmentation | [SRC-0066] |
| WF-M06 | Extraction (open-pit/underground) | Win ore | Operators, shift supervisors | production log | shovels, haul trucks, shafts | safety; dilution | tonnes mined; grade | [SRC-0066] |
| WF-M07 | Haulage & materials handling | Move ore/waste | Fleet operators | dispatch log | haul trucks, conveyors | fuel; uptime | haul cycle; availability | [SRC-0066] |
| WF-M08 | Processing (mill/flotation/smelt/refine) | Upgrade to metal | Metallurgists, plant ops | assay, plant log | crushers, mills, SX/EW, smelter | recovery; energy | recovery %; cathode t | [SRC-0066] |
| WF-M09 | Assaying & grade control | Measure metal content | Lab, grade control | assay certificate | assay lab | sampling error | assay turnaround | [SRC-0066] |
| WF-M10 | Tailings & waste management | Contain waste safely | TSF engineers, ZEMA | TSF monitoring | tailings dam, sensors | dam safety; environment | TSF stability | [SRC-0064] |
| WF-M11 | Safety & health (mine safety) | Protect workers | Mine Safety (MRC), SHE | incident report, permits | PPE, monitors, rescue | fatalities; exposure | LTIFR; incidents | [SRC-0064] |
| WF-M12 | Environmental compliance & rehabilitation | Meet EMA/MRC rules | SHE, ZEMA | EIA, audit, rehab plan | monitoring equipment | compliance; closure liability | compliance rate | [SRC-0064] |
| WF-M13 | Royalty, reporting & export | Pay tax; report; export | Finance, ZRA, MRC | royalty return, export docs | ERP | price volatility; delays | royalty paid; export t | [SRC-0064][SRC-0065] |
| WF-M14 | ASM operations & formalisation | Small-scale mining | ASM cooperatives, ASM Dept | ASM rights, cooperative reg | hand tools, small plant | safety; informality; finance | formalised miners | [SRC-0066] |
*(Cross-cutting: planning, procurement, operations, inventory, asset mgmt, workforce, safety, compliance, reporting, logistics, finance, closure — all represented above.)*

## Output 3 — Stakeholder Register
| Stakeholder | Role / responsibilities | Decisions | Info used | Pain points | Interactions |
|-------------|-------------------------|-----------|-----------|-------------|--------------|
| Large-scale mining company | Operate mine end-to-end | invest, produce, sell | geology, grade, prices, costs | energy (load-shedding), forex, tax stability | MRC, ZEMA, ZRA, ZESCO, suppliers |
| Mine manager / shift supervisor | Run production safely | shift plans, dispatch | production, grade, safety | uptime, safety, labour | crews, planners |
| Geologist / mine planner | Define & plan resource | drilling, cut-off | survey, assays | data quality, uncertainty | MRC, lab |
| Metallurgist / plant operator | Process ore to metal | plant settings | assays, recovery | recovery, energy | lab, maintenance |
| SHE / mine safety officer | Safety, health, environment | stop-work, controls | incidents, monitoring | fatalities, exposure, compliance | MRC (safety), ZEMA |
| MRC (regulator) | License, monitor, enforce | grant/suspend rights | cadastre, returns | capacity, compliance | companies, ZEMA |
| ZEMA | Environmental oversight | approvals, audits | EIA, monitoring | rehabilitation, TSF | mines, MRC |
| ZRA | Mineral royalty & tax | assessments | production, prices | valuation, evasion | mines, finance |
| ZCCM-IH | State equity holder | investment | financials | returns, governance | mines, govt |
| Contractor / OEM supplier | Provide services/equipment | bids, delivery | specs, schedules | payment, local content | procurement |
| ASM cooperative / miner | Small-scale extraction & trade | mine, sell | prices, rights | safety, finance, formalisation | ASM Dept, buyers |
| Equipment dealer / maintenance | Supply/service machinery | service, spares | asset data | spares, forex | mine maintenance |
| Community / traditional authority | Host, land, CSR | consent, grievances | impact info | displacement, environment | mine CSR, ZEMA |
| Transporter / logistics | Move concentrate/cathode | routing | volumes, corridors | corridor delays, cost | mine, export |

## Output 4 — Information Catalogue
- **Master data:** Mining right/licence, Mine, Pit/Shaft, Ore body/deposit, Equipment/fleet, Employee, Contractor/supplier, Tailings facility, Assay lab, Product (concentrate/cathode), ASM cooperative, Location/cadastre parcel.
- **Transactions:** Licence application/renewal, Blast record, Production (tonnes/grade), Haul dispatch, Assay result, Plant run, Royalty return, Export shipment, Incident report, Environmental monitoring reading, Rehabilitation record, Procurement PO, ASM rights registration.
- **Documents:** Exploration/mining licence (cadastre), Mine plan, Blast permit, Assay certificate, EIA/environmental audit, TSF monitoring report, Safety/incident report, Royalty return, Export documents, Procurement contracts.
- **Measurements:** Tonnes mined/milled, ore grade (%), metal recovery (%), cathode tonnes, drill metres, haul cycle time, equipment availability, TSF pore-pressure/levels, dust/emissions, water quality, energy (kWh), LTIFR.
- **Events:** Licence granted, blast fired, ore extracted, plant batch, assay returned, shipment dispatched, incident occurred, monitoring exceedance, audit conducted, rehabilitation milestone.
- **Reports:** Production report, grade-control report, royalty return, environmental compliance/annual report to ZEMA, safety statistics, export statistics.

## Output 5 — Operational Asset Register
Drill rigs; blasthole drills; explosives magazines; hydraulic shovels/excavators; haul trucks (ultra-class); underground loaders/shafts (Mopani deep shafts) [SRC-0066]; crushers; SAG/ball mills; flotation cells; SX/EW plant; smelter/refinery; tailings storage facility (TSF); conveyors; assay laboratory; environmental monitors (dust, water, ground); mine dewatering pumps; fleet-management/GPS sensors; workshops/facilities; power infrastructure.

## Output 6 — Document Register
Mining rights/cadastre records [SRC-0017]; exploration reports; mine plans; blast permits & records; assay certificates; production logs; haul dispatch logs; plant/metallurgical reports; royalty returns (ZRA); export documentation; EIA/ESIA & environmental audits (ZEMA); TSF safety reports; safety/incident reports (mine safety); procurement contracts/POs; ASM rights & cooperative registration.

## Output 7 — Pain Point Register (no solutions)
| ID | Pain point | Type |
|----|-----------|------|
| PP-M01 | Electricity load-shedding disrupting processing | Resource/energy [SRC-0065] |
| PP-M02 | Copper price & forex volatility | Financial |
| PP-M03 | Fragmented paper safety/incident records | Manual/data |
| PP-M04 | Tailings dam safety & closure liabilities | Compliance/risk [SRC-0064] |
| PP-M05 | Assay/grade-control turnaround delays | Delay |
| PP-M06 | Equipment downtime & spares (forex) | Resource |
| PP-M07 | Licensing/cadastre & compliance burden | Compliance |
| PP-M08 | ASM informality, safety & finance exclusion | Access/safety [SRC-0066] |
| PP-M09 | Local-content & reporting obligations | Compliance [SRC-0064] |
| PP-M10 | Community grievances / land & environment | Communication |
| PP-M11 | Corridor/logistics delays for exports | Logistics |
| PP-M12 | Data duplication across production/finance/regulator | Data duplication |

## Output 8 — KPI Register
Tonnes mined/milled; head grade & recovery %; cathode/concentrate output; unit cost (US$/lb or /t); equipment availability & utilisation; haul cycle time; LTIFR / fatalities; energy per tonne; water use; TSF stability indicators; royalty paid; export tonnes; rehabilitation progress; ASM formalised count.

## Output 9 — Knowledge Graph Updates
Findings `F-0056` (MRCA 2024/MRC & royalties), `F-0057` (mining economics), `F-0058` (mine operations & ASM) added; workflow nodes `WF-M01..WF-M14`; entities: `ENT-MINE`, `ENT-PIT`, `ENT-ORE`, `ENT-TAILINGS`, `ENT-ASSAY`, `ENT-MININGRIGHT` (registered in the shared graph CSVs). Relationships: Company `HOLDS` MiningRight (`GOVERNED_BY` MRC); Mine `PRODUCES` Ore→Concentrate→Cathode; Mine `GOVERNED_BY` ZEMA (environment); Company `PAYS` royalty to ZRA.

## Recorded uncertainties
Company-internal SOPs, exact production data, and ASM field practices require primary collection (deferred). MRCA/GMDA are recent (2024/2025) — implementation details still settling.
