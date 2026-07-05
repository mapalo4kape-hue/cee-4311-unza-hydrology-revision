---
id: WP2.5-P1-HANDBOOK
title: National Logistics Operations Handbook — Zambia (WP2.5 Phase 1)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research (logistics layer)
work_package: WP2.5
industry: TAX-IND.5 (Logistics & Supply Chains)
topic: Logistics operations intelligence
keywords: [logistics, corridors, fleet, warehouse, supply-chain, cross-border]
summary: High-level operational intelligence for Zambia's logistics & supply-chain layer connecting agriculture, mining, construction & environmental. Contains Outputs 1 (National handbook), 3 (Fleet), 4 (Warehouse). Evidence-first; no software/schema/requirements.
source: SRC-0041;SRC-0035;SRC-0087;SRC-0088;SRC-0089;SRC-0090;SRC-0092;SRC-0093
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 80
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../../../02-evidence/EVIDENCE_REGISTER.csv, ../../CROSS_INDUSTRY_COMPARATIVE_ANALYSIS.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: [WF-L01..WF-L20]
---

# National Logistics Operations Handbook — Zambia

> Connects the four researched industries. Zambia-specific facts cited; generic logistics operations are consultant synthesis. **No software design, schemas, or requirements.**

## Output 1 — National Logistics Operations Handbook

### 1.1 National logistics network
- **Regional corridors:** Dar es Salaam, North-South (Durban via Zimbabwe/Botswana, spur to Malawi), Beira, Nacala, Walvis Bay–Ndola–Lubumbashi, Lobito (emerging), Central, Trans-Caprivi, Kalahari, Maputo — rooted in the SADC Protocol on Transport, Communications & Meteorology; implemented via the "3 Is" (Instruments, Institutions, Infrastructure) [SRC-0041] (UN OHRLLS/GRZ, pub. 2024; confidence 84/100; retrieved 2026-07-05).
- **Rail:** Zambia Railways line (Livingstone → DRC border via Lusaka, Kapiri Mposhi, Copperbelt; North-South) and **TAZARA** (Kapiri Mposhi → Dar es Salaam; full run ~48 h) [SRC-0087] (JICA, pub. 2019; confidence 80/100; retrieved 2026-07-05).
- **Roads:** ~67,671 km classified network (core 40,454 km); road-fund surplus for the main network but feeder roads deteriorate in the rainy season [SRC-0035] (RDA); [SRC-0057] (Gates, pub. 2019; confidence 76/100; retrieved 2026-07-05).
- **Border posts / OSBPs:** Chirundu, Nakonde, Kasumbalesa, Kazungula, Mwami, Chanida, Katima-Mulilo; Chirundu is the flagship North-South Corridor OSBP [SRC-0041][SRC-0092].
- **Weighbridges & truck stops:** installed at major road sections along corridors [SRC-0087].
- **Dry ports / inland ports:** Kapiri Mposhi dry port (TAZARA/Zambia Railways); LS-MFEZ dry port via PPP; land secured in Nacala (Mozambique) [SRC-0089].
- **Fuel distribution:** **TAZAMA pipeline** (Dar es Salaam → Ndola) + **INDENI** refinery (Ndola), onward road distribution [SRC-0089].
- **SEZ / industrial parks / distribution hubs:** 7 operational SEZ (5 MFEZ + 2 IP) — Lusaka South (govt/IDC), Chambishi (mining, Copperbelt), Lusaka East (near airport), Kalumbila, Jiangxi (Chibombo), Sub-Saharan Gemstones IP (Ndola), Roma IP (Lusaka) [SRC-0088] (ZDA, pub. 2024; confidence 84/100; retrieved 2026-07-05).

### 1.2 Landlocked reality
Zambia is landlocked; freight relies on regional corridors to sea ports (Dar es Salaam, Durban, Beira, Nacala, Walvis Bay, Lobito), raising haulage cost and exposing supply chains to **border dwell times** and **rainy-season road access** [SRC-0057][SRC-0092].

### 1.3 How logistics connects the four industries
Agriculture (inputs in / commodities out), Mining (consumables & fuel in / ore & concentrate out via corridors & rail), Construction (materials & equipment mobilisation), Environmental (waste, samples, monitoring gear) all move over the **same corridor/road/rail/border/warehouse network** — the unifying operational layer.

## Output 3 — Fleet Operations Handbook
| Area | Current practice (Zambia) | Cited |
|------|---------------------------|-------|
| Fleet mix | Trucks (rigid/artic), haul trucks (mining), tippers, tankers (fuel), ox-carts (rural), reefers (limited) | [SRC-0093] |
| Ownership | Large/medium trucking firms + owner-operators; competitive, low entry barriers | [SRC-0057][SRC-0093] |
| Dispatch & scheduling | Manual/phone at SME level; larger firms use scheduling & GPS | [SRC-0093] |
| GPS tracking | Web-based GPS monitoring by established operators (e.g. Agro-Fuel) | [SRC-0093] |
| Fuel management | Fuel logs; tanker supply from Ndola (TAZAMA/INDENI); price/theft risk | [SRC-0089] |
| Maintenance | In-house workshops (larger firms); spares/forex constraints | [SRC-0093] |
| Driver management | Licensing (RTSA); cross-border documentation; fatigue on long corridors | [SRC-0019] |
| Route optimisation | Corridor choice by cost/border congestion; mostly manual | [SRC-0092] |
| Fleet compliance | RTSA registration, weighbridge/axle-load, TIP & third-party insurance at borders | [SRC-0019][SRC-0092] |
| Tyre management | Ad hoc; significant cost on poor roads | (consultant synthesis) |
**Fleet workflows:** WF-L11 dispatch, WF-L12 GPS tracking, WF-L13 preventive maintenance, WF-L14 driver management, WF-L15 route/corridor selection, WF-L16 fuel management (see Workflow Library).

## Output 4 — Warehouse Operations Handbook
| Stage | Practice (Zambia) | Cited |
|-------|-------------------|-------|
| Receiving | Delivery note/waybill check; weighbridge for bulk | [SRC-0090] |
| Inspection & grading | Quality/moisture checks (grain: moisture meter, sieves) | [SRC-0051] |
| Put-away & storage | On-farm sheds, community aggregation centres, district **certified warehouses** (WRS), FRA depots, MFEZ warehouses | [SRC-0051][SRC-0093] |
| Warehouse receipt | Certified warehouses issue WRS receipts (collateralisable) | [SRC-0051][SRC-0062] |
| Picking/packing/loading | Manual; bagged commodities; bulk for minerals | (synthesis) |
| Dispatch | Waybill + gate-out; export docs for cross-border | [SRC-0090] |
| Inventory counting / adjustments | Stock cards (paper) at SME level; WRS/systemised at certified warehouses | [SRC-0051] |
| Returns | Ad hoc | (synthesis) |
**Warehouse workflows:** WF-L17 receiving/inspection, WF-L18 storage & WRS, WF-L19 picking/loading/dispatch, WF-L20 inventory count (see Workflow Library).

## Recorded uncertainties (→ Gap Register)
- Freight volumes, corridor modal split, weighbridge locations, and warehouse capacity figures need primary/operator data.
- Fleet-operator internal SOPs and cold-chain capacity require field collection.
