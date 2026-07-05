---
id: WP2.5-P1-WFL
title: Logistics Workflow Library & Supply Chain Process Library — Zambia (WP2.5)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research (logistics layer)
work_package: WP2.5
industry: TAX-IND.5 (Logistics & Supply Chains)
topic: Logistics workflows & supply chain
keywords: [workflows, supply-chain, procurement, cross-border, corridors]
summary: Outputs 2 & 5. End-to-end logistics workflows (full attribute capture) linked back to Agriculture/Mining/Construction/Environmental workflows, plus procurement and cross-border supply-chain processes. Evidence-first; no software design.
source: SRC-0041;SRC-0051;SRC-0052;SRC-0090;SRC-0092;SRC-0093
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 80
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_NATIONAL_LOGISTICS_OPERATIONS_HANDBOOK.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: [WF-L01..WF-L26]
---

# Logistics Workflow Library & Supply Chain Process Library

## Output 2 — Logistics Workflow Library
> Attributes captured per workflow: Purpose · Trigger · In→Out · Actors/Orgs · Docs · Vehicles/Equipment/Assets · Info exchanged · Decisions · Pain/Risk · KPI · Compliance · Season · Geography · Upstream→Downstream (incl. **links to industry workflows** WF-*/WF-M*/WF-C*/WF-E*).

| ID | Workflow | Purpose | Trigger | Key actors/orgs | Docs | Vehicles/assets | Decisions | Pain/risk | KPI | Compliance | Links (industry) |
|----|----------|---------|---------|-----------------|------|-----------------|-----------|-----------|-----|-----------|------------------|
| WF-L01 | Inbound input distribution | Move inputs to point of use | Order/FISP | supplier, transporter, agro-dealer | PO, waybill, GIN | truck, store | mode, route | timing vs planting, roads | on-time % | RTSA, weighbridge | WF-007/008 (ag), WF-M04 (mine), WF-C08 (constr) |
| WF-L02 | Fertilizer/seed movement | Deliver fertilizer/seed | Season/FISP | NCZ/importer, distributor (e.g. Thamoema) | delivery note | tanker/truck, bags | bulk vs bagged | stockouts, rainy roads | delivery lead time | phytosanitary | WF-008 |
| WF-L03 | Agrochemical/hazmat movement | Move chemicals/explosives safely | Order | supplier, licensed transporter | hazmat docs, permit | ADR-type truck | routing, escort | safety, spill | incident rate | hazmat, ZEMA | WF-009 (ag), WF-M04 (mine explosives) |
| WF-L04 | Harvest collection & aggregation | Gather & bulk produce | Harvest | farmer, cooperative, aggregator (CHC) | aggregation record | trucks, shed, scale | grade, consolidate | quality variance | aggregated volume | grades | WF-024/031 (ag) |
| WF-L05 | Cold chain movement | Keep perishables chilled | Perishable dispatch | cold-store, reefer operator | temp log | reefer, cold room | chill vs fresh | power, gaps | spoilage % | food safety | WF-027 (ag) |
| WF-L06 | Commodity transport to market/FRA | Move commodity to buyer | Sale/FRA call | farmer, transporter, FRA | waybill, sale record | trucks, depot | buyer, route | payment delay, roads | price realised, cost/t | FRA rules | WF-029 (ag) |
| WF-L07 | Warehouse-receipt logistics | Deposit/withdraw stored grain | Deposit/sale | warehouse operator, bank, ZAMACE | warehouse receipt | certified warehouse | store vs sell | quality, financing | throughput | Ag Credits Act | WF-026 (ag) |
| WF-L08 | Ore/concentrate haulage | Move ore/concentrate | Production | mine, haulage contractor | dispatch log | haul trucks, rail | road vs rail, corridor | uptime, cost/t | haul cycle, availability | axle-load | WF-M06/M07 (mine) |
| WF-L09 | Mineral export logistics | Export cathode/concentrate | Export order | mine, C&F agent, rail/port | export docs, SAD | rail, trucks, port | corridor choice | border dwell, forex | export tonnes, transit time | ASYCUDA, royalty | WF-M13 (mine) |
| WF-L10 | Spare-parts & heavy-equipment transport | Move parts/machines | Maintenance/mobilise | supplier, transporter | GIN, abnormal-load permit | low-loader, crane | own vs hire | forex, lead time | delivery time | abnormal-load | WF-M04/M12 (mine), WF-C09 (constr) |
| WF-L11 | Fleet dispatch | Assign vehicles to loads | Load ready | fleet controller, driver | trip sheet | trucks | vehicle/driver assign | utilisation | fleet utilisation | RTSA | all |
| WF-L12 | GPS tracking & monitoring | Track vehicles/cargo | In transit | operator, control room | tracking log | GPS units | reroute, alert | theft, deviation | on-time, incidents | — | WF-L08/L09/L06 |
| WF-L13 | Preventive maintenance | Keep fleet running | Service due | workshop, driver | service log | workshop, spares | repair vs replace | downtime, spares | availability | roadworthiness | all fleet |
| WF-L14 | Driver management | Manage/comply drivers | Assignment | fleet, RTSA | licence, logbook | — | hire, rest | fatigue, cross-border docs | compliance % | RTSA, cross-border | WF-L08/L09 |
| WF-L15 | Route/corridor selection | Choose least-cost/fastest route | Trip planning | planner | route plan | — | corridor, border | congestion, season | transit cost/time | corridor rules | WF-L06/L08/L09 |
| WF-L16 | Fuel logistics/management | Supply & control fuel | Ops need | fuel supplier, tanker | fuel log | tanker, tanks | quantity, timing | price, theft, supply | fuel/km | — | WF-M (mine), WF-C (constr) |
| WF-L17 | Warehouse receiving & inspection | Take goods into store | Delivery | storekeeper | GRN, inspection | dock, scale, moisture meter | accept/reject | quality, discrepancy | receiving accuracy | grades | WF-026 (ag), WF-C08 (constr) |
| WF-L18 | Storage & WRS | Hold goods; issue receipts | Put-away | operator | stock card, WR | warehouse, silo | on-farm vs certified | loss, aflatoxin | storage loss % | Ag Credits Act | WF-026 (ag) |
| WF-L19 | Picking/loading/dispatch | Prepare & send goods out | Order | storekeeper, loaders | pick list, waybill | forklift, truck | load plan | damage, delay | dispatch on-time % | — | WF-028/029 (ag) |
| WF-L20 | Inventory counting & adjustment | Reconcile stock | Cycle/annual | storekeeper | count sheet | scanner (rare) | adjust, write-off | shrinkage | stock accuracy | audit | WF-010 (ag) |
| WF-L21 | Site delivery (construction) | Deliver materials to site | Site call-off | supplier, transporter | delivery note | tipper, mixer, crane | JIT vs stockpile | site access, timing | delivery reliability | site rules | WF-C07/C08 (constr) |
| WF-L22 | Quarry/aggregate transport | Move aggregate/cement/steel | Order | quarry, transporter | weighbridge ticket | tippers | source, haul distance | dust, road wear | cost/t delivered | environmental | WF-C08 (constr) |
| WF-L23 | Waste & hazardous-waste transport | Move waste to disposal | Collection | waste operator, ZEMA | waste manifest | waste trucks | route, disposal | leakage, compliance | waste moved, diverted | ZEMA, hazmat | WF-E09 (env) |
| WF-L24 | Laboratory sample transport / chain-of-custody | Move samples to lab | Sampling | consultant, courier, lab | chain-of-custody form | cooler box | preserve, timing | integrity, delay | turnaround, integrity | accreditation | WF-004 (ag), WF-M09 (mine assay), WF-E03/E10 (env) |
| WF-L25 | Monitoring-equipment logistics | Deploy/retrieve monitors | Monitoring plan | consultant/operator | deployment log | sensors, vehicles | siting | access, calibration | uptime | EMP | WF-E10 (env) |
| WF-L26 | Recycling / landfill / medical-waste logistics | Move recyclables/medical waste | Collection | operator, local authority | manifest | trucks, landfill | segregate, treat | biohazard, capacity | volume, compliance | ZEMA, health | WF-E09 (env) |

*(26 logistics workflows, each linked upstream/downstream to the industry workflows from ACT-008/010.)*

## Output 5 — Supply Chain Process Library

### 5.1 Procurement logistics (purchase-to-pay)
Purchase request → **Purchase Order** → supplier fulfilment → delivery → **Goods Received Note (GRN)** / delivery verification → **invoice matching** (PO–GRN–invoice 3-way) → payment workflow (bank/mobile money). Public sector runs via **ZPPA e-GP** (WP2.3). [SRC-0090 for delivery/customs docs; WP2.3 SRC-0068 for public procurement].

### 5.2 Cross-border trade process (import)
Supplier pre-alert (invoice, bill of lading) → forward to **licensed clearing agent (ZAFFA)** → agent prepares **SAD/Bill of Entry (CE 20)** in **ASYCUDA World** → duties/ASYCUDA fee paid (e-payment/mobile money) → **SELECTIVITY** risk lane (Red/Yellow/Blue/Green) → examination → **Release Order** → **Exit Note** → goods exit customs; vehicles need **Temporary Import Permit (TIP)** + third-party insurance at OSBP [SRC-0090][SRC-0092]. Clearing agent mandatory for **CIF > USD 2,000** [SRC-0090]. Preferential treatment under **COMESA/SADC/AfCFTA** with certificates of origin [SRC-0092]. Product permits: meat (Veterinary), plants/seeds (phytosanitary, Mount Makulu), food/drugs (MoH/ZAMRA), firearms (Police) [SRC-0091].

### 5.3 Cross-border trade process (export)
Export order → C&F agent → export declaration (ASYCUDA) → permits/certificates of origin → corridor/rail routing → border clearance → onward to sea port (Dar/Durban/Beira/Nacala/Walvis Bay/Lobito) [SRC-0041][SRC-0092]. Mineral exports also carry royalty/MRC obligations (WP2.2).

### 5.4 Border performance
Chirundu (North-South Corridor) is busy/congested; **transit can clear in ~3 h but imports average 2–7 days** depending on documentation; Kasumbalesa is a noted bottleneck; **Single Window / Coordinated Border Management** being adopted [SRC-0092].

## Recorded uncertainties
Exact procurement SOPs per organisation, 3-way-match digitisation levels, and current border dwell-time statistics require operator/ZRA primary data.
