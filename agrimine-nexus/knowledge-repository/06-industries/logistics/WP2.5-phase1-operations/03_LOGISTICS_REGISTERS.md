---
id: WP2.5-P1-REGISTERS
title: Logistics Registers — Corridor / Distribution / Asset / Stakeholder / Document / KPI / Pain Point (WP2.5)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research (logistics layer)
work_package: WP2.5
industry: TAX-IND.5 (Logistics & Supply Chains)
topic: Logistics registers
keywords: [corridors, distribution, assets, stakeholders, documents, KPI, pain-points]
summary: Outputs 6-12. Evidence-first registers for the logistics layer. No software design.
source: SRC-0041;SRC-0087;SRC-0088;SRC-0089;SRC-0090;SRC-0092;SRC-0093
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
related_workflows: []
---

# Logistics Registers (Outputs 6–12)

## Output 6 — Transport Corridor Register
| ID | Corridor | Route (from Zambia) | Mode | Sea port | Notes | Cited |
|----|----------|---------------------|------|----------|-------|-------|
| COR-01 | Dar es Salaam | Nakonde/Tunduma → Tanzania | road + TAZARA rail | Dar es Salaam | main NE corridor | [SRC-0087] |
| COR-02 | North-South | Chirundu/Kazungula → Zimbabwe/Botswana → RSA | road + rail | Durban | busiest; Chirundu OSBP | [SRC-0041][SRC-0092] |
| COR-03 | Beira | via Zimbabwe → Mozambique | road + rail | Beira | agri/mineral | [SRC-0041] |
| COR-04 | Nacala | via Malawi → Mozambique | road + rail | Nacala | deep-water port | [SRC-0041] |
| COR-05 | Walvis Bay–Ndola–Lubumbashi | west via Namibia | road | Walvis Bay | mineral/DRC transit | [SRC-0041] |
| COR-06 | Lobito | Copperbelt/NW → DRC/Angola | rail (developing) | Lobito | emerging Atlantic route | [SRC-0041] |
| COR-07 | Central / Trans-Caprivi / Kalahari | regional interconnects | road | various | interconnecting spurs | [SRC-0087] |

## Output 7 — Distribution Network Register
| ID | Node type | Examples | Cited |
|----|-----------|----------|-------|
| DN-01 | One-Stop Border Posts | Chirundu, Nakonde, Kasumbalesa, Kazungula, Mwami, Chanida, Katima-Mulilo | [SRC-0092] |
| DN-02 | Weighbridges/truck stops | major corridor road sections | [SRC-0087] |
| DN-03 | Dry ports / inland ports | Kapiri Mposhi; LS-MFEZ (PPP); Nacala land | [SRC-0089] |
| DN-04 | Airports | Kenneth Kaunda Int'l (Lusaka), Simon Mwansa Kapwepwe (Ndola), Harry Nkumbula (Livingstone), Mfuwe | (to confirm) |
| DN-05 | SEZ/MFEZ & industrial parks | Lusaka South, Chambishi, Lusaka East, Kalumbila, Jiangxi, Sub-Saharan Gemstones IP, Roma IP | [SRC-0088] |
| DN-06 | Fuel distribution | TAZAMA pipeline (Dar→Ndola), INDENI refinery, depots | [SRC-0089] |
| DN-07 | Agri aggregation & storage | community aggregation centres, district certified warehouses, FRA depots + satellite collection points | [SRC-0051][SRC-0093] |
| DN-08 | Fertilizer manufacture/distribution | NCZ (Compound D, Urea); distributor depots (CHC, Thamoema) | [SRC-0093] |
| DN-09 | Commodity exchange & WRS | ZAMACE + certified warehouses | [SRC-0082] |

## Output 8 — Logistics Asset Register
Trucks (rigid, articulated, tippers); haul trucks (mining); fuel tankers; low-loaders; reefers/cold rooms; ox-carts (rural); rail wagons & locomotives (Zambia Railways, TAZARA); forklifts; cranes (mobile/tower); warehouses (on-farm, community, certified, MFEZ); silos & grain sheds; weighbridges; GPS/telematics units; workshops & spares; fuel storage (pipeline, depots, tanks); handling equipment (scales, moisture meters, sieves); cooler boxes (sample transport); waste-collection trucks & landfills.

## Output 9 — Logistics Stakeholder Register
| Stakeholder | Role | Info used | Pain points | Interactions |
|-------------|------|-----------|-------------|--------------|
| Trucking firm / owner-operator | Move cargo | loads, routes, rates | fuel, roads, forex, borders | shippers, ZRA, RTSA |
| Clearing & forwarding agent (ZAFFA) | Customs clearance | SAD, permits, tariffs | border congestion, doc accuracy | ZRA, importer |
| Zambia Revenue Authority (ZRA) | Customs & tax at borders | ASYCUDA declarations | risk, evasion, throughput | agents, importers |
| Zambia Railways / TAZARA | Rail freight | wagon schedules | asset condition, capacity | mines, agri, ports |
| Road Development Agency (RDA) | Road network | condition, funding | feeder-road backlog | operators |
| RTSA | Vehicle & driver compliance | registrations, licences | enforcement | operators, drivers |
| Warehouse operator | Store & issue receipts | stock, grades | certification, financing | farmers, banks, ZAMACE |
| FRA | Grain reserves & depots | stock, prices | payment, logistics | farmers, transporters |
| Fuel supplier (TAZAMA/INDENI/OMCs) | Supply fuel | demand, prices | supply, price | fleets, mines |
| ZDA / MFEZ operators | Industrial/logistics zones | zone occupancy | infrastructure, power | investors |
| Cross-border agencies (COMESA/SADC) | Trade facilitation | trade rules | harmonisation | ZRA, agents |
| Waste/environmental transporter | Move waste/samples | manifests, CoC | compliance, biohazard | ZEMA, labs |
| Integrated agri-logistics (CHC/Thamoema) | Inputs + aggregation + transport | orders, stock | working capital | farmers, buyers |

## Output 10 — Logistics Document Register
Purchase order; delivery note / waybill; goods received note (GRN); Single Administrative Document (SAD) / Bill of Entry (CE 20); petty consignment (CE 6); clearing-agent form (CE 34); Temporary Import Permit (TIP); certificate of origin (COMESA/SADC/AfCFTA); phytosanitary/veterinary/health permits; hazmat/abnormal-load permits; weighbridge ticket; warehouse receipt (WRS); chain-of-custody form (samples); waste manifest; trip sheet / driver logbook; GPS tracking log; fuel log; export documentation; third-party insurance.

## Output 11 — Logistics KPI Register
On-time delivery %; transit time per corridor; border dwell/clearance time (2–7 days imports at Chirundu [SRC-0092]); cost per tonne-km; fleet utilisation & availability; fuel per km; vehicle downtime; storage loss %; warehouse throughput & stock accuracy; aggregated volume; export tonnes & transit time; customs clearance-lane distribution; damage/loss rate; cold-chain spoilage %; sample turnaround & integrity; waste moved/diverted.

## Output 12 — Logistics Pain Point Register (no solutions)
| ID | Pain point | Type | Cited |
|----|-----------|------|-------|
| PP-L01 | Border congestion & long clearance (2–7 days) | Delay | [SRC-0092] |
| PP-L02 | Rainy-season feeder-road impassability | Bottleneck | [SRC-0057] |
| PP-L03 | High landlocked haulage cost | Cost | [SRC-0057] |
| PP-L04 | Fuel price/supply/theft | Cost/risk | [SRC-0089] |
| PP-L05 | Paper documentation & duplication (waybills, GRNs) | Manual/data | [SRC-0090] |
| PP-L06 | Fragmented tracking / limited visibility | Information | [SRC-0093] |
| PP-L07 | Weighbridge/axle-load & road damage | Compliance | [SRC-0087] |
| PP-L08 | Cold-chain gaps (power) | Loss | (synthesis) |
| PP-L09 | Payment delays in commodity logistics | Financial | [SRC-0052] |
| PP-L10 | Spare-parts lead times & forex | Resource | [SRC-0093] |
| PP-L11 | Multiple permits/agencies at borders | Compliance | [SRC-0091] |
| PP-L12 | Kasumbalesa bottleneck (DRC traffic) | Bottleneck | [SRC-0092] |
| PP-L13 | Hazardous/waste transport compliance | Risk | (WP2.4) |
| PP-L14 | Sample chain-of-custody integrity | Quality | (WP2.4) |

## Recorded uncertainties (→ Gap Register)
Airport inventory (DN-04) to confirm; corridor volumes/modal split; weighbridge locations; warehouse capacity; fleet-size statistics — all require primary/operator data.
