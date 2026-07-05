---
id: WP2.1-P1-WFL
title: Agricultural Workflow Library — Zambia (WP2.1 Phase 1)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Agricultural operational workflows
keywords: [workflows, operations, FISP, extension, marketing, contract-farming, season]
summary: End-to-end operational workflows across Zambian agriculture, documented as an operations consultant. No crops research, no software requirements, no features.
source: SRC-0045;SRC-0046;SRC-0047;SRC-0048;SRC-0049;SRC-0050;SRC-0051;SRC-0052;SRC-0053;SRC-0054;SRC-0055;SRC-0056;SRC-0057
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
related_entities: [ENT-FARM, ENT-FARMER]
related_apis: []
related_modules: []
related_workflows: [WF-001..WF-040]
---

# Agricultural Workflow Library — Zambia

> Operational intelligence: how work is actually performed, end to end. Zambia-specific mechanisms are cited; generic operational structure is consultant synthesis of practitioner practice. **No software requirements, features, competitors, or AI analysis.**
>
> **Season anchor** (drives most timing): rainy season **Oct–April**; land prep Sep–Nov; planting **Nov–Dec** (reliable rains); crop management Dec–Apr; harvest **May–Aug**; marketing/storage Jun–Oct [SRC-0056] (UNCTAD, pub. 2023; confidence 80/100; retrieved 2026-07-05).

## 1. Workflow master table (40 workflows)

Columns: **Trig** = trigger · **Actors** · **In→Out** · **Docs** · **Assets** · **Decisions** · **Pain/Risk** · **KPI** · **Season**. Each workflow has an ID `WF-0xx` (registered in the knowledge graph).

| ID | Workflow | Purpose | Trig | Key actors | In → Out | Key docs | Assets | Key decision(s) | Pain / risk | KPI | Season |
|----|----------|---------|------|-----------|----------|----------|--------|-----------------|-------------|-----|--------|
| WF-001 | Farm establishment | Set up a viable farm | New land/tenure | Farmer, chief, Lands, surveyor | land, capital → registered farm | title/chief letter, lease | — | tenure type; site | tenure insecurity; capital | time-to-operational | any |
| WF-002 | Land preparation | Ready fields for planting | Season start | Farmer, labour, mech provider | land, fuel, labour → prepared field | work plan | tractor, plough, hoes | manual vs mechanised; tillage | draught power access; timing | ha prepared/day | Sep–Nov |
| WF-003 | Field mapping | Know field extents/zones | Planning | Farmer, extension, surveyor | field, GPS → field map/area | field sketch | GPS, phone | boundaries; block sizing | inaccurate area; disputes | mapped ha | pre-season |
| WF-004 | Soil testing | Match inputs to soil | Planning/advisory | Farmer, extension, lab | soil sample → soil report | sample form, lab report | auger, lab kit | test or not; lime need | lab access/cost; delay | % fields tested | pre-season |
| WF-005 | Input planning | Decide input needs | Budgeting | Farmer, extension, agro-dealer | plan, soil, area → input list | input plan | — | crop mix; input rates | wrong rates; forecast | plan accuracy | Aug–Oct |
| WF-006 | Budgeting | Plan season finances | Planning | Farmer, cooperative, bank | costs, prices → budget | budget sheet | phone/paper | self-fund vs credit | price uncertainty | budget variance | Aug–Oct |
| WF-007 | Seed procurement | Obtain seed | Input plan/FISP | Farmer, agro-dealer, FISP/ZIAMIS | voucher/cash → seed | e-voucher/GIN, receipt | agro-dealer store | variety; source | stock-outs; late redemption | on-time seed % | Sep–Dec |
| WF-008 | Fertilizer procurement | Obtain fertilizer | Input plan/FISP | Farmer, agro-dealer, FISP | voucher/cash → fertilizer | e-voucher/GIN | store, transport | basal/top-dressing qty | price; availability; timing | on-time fert % | Sep–Dec |
| WF-009 | Chemical procurement | Obtain agrochemicals | Pest/plan | Farmer, agro-dealer | cash/credit → chemicals | receipt, label | store | product choice; dosage | counterfeit; safety | correct-product % | as needed |
| WF-010 | Inventory management | Track inputs on hand | Post-procurement | Farmer, storekeeper, cooperative | inputs → stock records | stock card | store, bags | reorder; allocation | spoilage; theft | stock accuracy | season |
| WF-011 | Planting | Establish crop | Reliable rains | Farmer, labour | seed, land, labour → planted crop | planting record | planter, hoes | date; spacing; density | rain onset; labour peak | planting window hit % | Nov–Dec |
| WF-012 | Irrigation | Supply water | Dry spell/dry-season crop | Farmer, irrigation operator | water, energy → irrigated crop | irrigation log | pumps, pipes, canals | when/how much | water/energy cost; access | water-use efficiency | dry spells / dry season |
| WF-013 | Scouting | Detect field issues early | Routine monitoring | Farmer, extension, agronomist | field walk → scouting notes | scouting form | phone, notebook | intervene or not | labour; skill; coverage | scouting frequency | Dec–Apr |
| WF-014 | Crop monitoring | Track crop progress | Growth stages | Farmer, extension | observations → status | field diary | phone | stage actions | data capture; recall | monitoring cadence | Dec–Apr |
| WF-015 | Pest management | Control pests | Threshold/scouting | Farmer, extension, agro-dealer | chemicals/IPM → protected crop | spray record | sprayer, PPE | product; timing; threshold | FAW; resistance; safety | pest incidence | Dec–Apr |
| WF-016 | Disease management | Control disease | Symptom detection | Farmer, extension, lab | fungicide/IPM → healthy crop | diagnosis note | sprayer | diagnose; treat | misdiagnosis; spread | disease incidence | Dec–Apr |
| WF-017 | Weed control | Manage weeds | Weed emergence | Farmer, labour | herbicide/labour → clean field | — | sprayer, hoes | chemical vs manual | labour peak; timing | weeding timeliness | Dec–Feb |
| WF-018 | Nutrient management | Feed crop | Growth stage | Farmer, extension | fertilizer → nourished crop | top-dressing record | spreader | split timing; rate | leaching; cost | nutrient timeliness | Dec–Feb |
| WF-019 | Weather monitoring | Anticipate conditions | Daily/seasonal | Farmer, extension, ZMD | forecasts → decisions | advisory SMS | phone, radio | plant/spray/irrigate timing | forecast access/accuracy | advisory uptake | season |
| WF-020 | Labour management | Organise workforce | Peak tasks | Farmer, farm manager, labourers | labour → completed tasks | attendance, payroll | — | hire; task allocation | peak scarcity; wages | labour cost/ha | peaks |
| WF-021 | Equipment management | Keep machinery running | Ownership/hire | Farmer, mech provider, dealer | machines, fuel → field ops | service log | tractor, implements | own vs hire; service | breakdown; spares | machine uptime | season |
| WF-022 | Fuel management | Supply energy for ops | Mechanised ops | Farmer, supplier | fuel → operations | fuel log | jerry cans, tanks | quantity; timing | price; access; theft | fuel per ha | season |
| WF-023 | Harvest planning | Prepare to harvest | Maturity approach | Farmer, farm manager | maturity, labour → harvest plan | harvest plan | — | timing; sequence | labour; weather | harvest readiness | Apr–May |
| WF-024 | Harvest execution | Gather crop | Crop maturity | Farmer, labour, mech | mature crop → harvested produce | harvest record | combine, sickles, bags | manual vs combine; moisture | losses; rain; labour | harvest loss % | May–Aug |
| WF-025 | Yield estimation | Quantify output | Pre/post harvest | Farmer, extension, ZamStats | field data → yield estimate | crop forecast form | scale, GPS | sampling; method | accuracy; recall | estimate accuracy | Apr–Jul |
| WF-026 | Storage | Preserve produce | Post-harvest | Farmer, warehouse operator | produce → stored grain | stock/WRS receipt | store, silo, sheds | on-farm vs warehouse | pests; moisture; aflatoxin | storage loss % | Jun–Oct |
| WF-027 | Cold chain | Preserve perishables | Perishable harvest | Farmer, cold-store operator, transporter | perishables → chilled produce | temp log | cold room, reefer | chill or sell fresh | power; cost; gaps | spoilage % | harvest |
| WF-028 | Transport | Move produce/inputs | Dispatch need | Farmer, transporter, cooperative | goods → delivered goods | waybill/GIN | trucks, ox-cart | mode; route; cost | road access (rainy); cost | on-time delivery % | year |
| WF-029 | Market sales | Sell produce | Harvest/price | Farmer, buyer, FRA, ZAMACE | produce → payment | sale contract, WRS | scale, phone | buyer; price; timing | price; delayed payment | price realised | Jun–Oct |
| WF-030 | Contract farming | Produce under contract | Outgrower agreement | Farmer, agribusiness, distributor | inputs-on-credit → committed crop | outgrower contract | — | join scheme; side-selling | side-selling; debt | contract fulfilment % | season |
| WF-031 | Commodity aggregation | Bulk smallholder output | Post-harvest | Cooperative, aggregator, agent | many lots → bulked lot | aggregation record | shed, scale, moisture meter | grade; consolidate | quality variance; trust | aggregated volume | Jun–Sep |
| WF-032 | Financial management | Manage money flows | Ongoing | Farmer, cooperative, bank | income/costs → cash position | ledger | phone (mobile money) | spend; save; repay | cash-flow gaps; records | margin | year |
| WF-033 | Record keeping | Capture operations data | Every activity | Farmer, farm manager | activities → records | field diary, books | paper, phone | what to record | literacy; discipline; loss | record completeness | year |
| WF-034 | Compliance | Meet legal/quality rules | Regulatory/buyer | Farmer, regulator, buyer | activity → compliant status | permits, certs | — | which standards | awareness; cost | compliance rate | as required |
| WF-035 | Reporting | Report to programs/buyers | Program/season | Farmer, extension, cooperative | data → reports | forms, ZIAMIS | phone/paper | what/when to report | duplication; delay | on-time reporting % | periodic |
| WF-036 | Insurance claims | Recover losses | Loss event | Farmer, insurer, FISP | loss evidence → payout | claim form | phone | claim or not; evidence | proof; delays; basis-risk | claim turnaround | post-loss |
| WF-037 | Credit applications | Obtain finance | Season funding | Farmer, bank, MFI, cooperative | application, collateral → loan | loan forms, WRS | phone | borrow; collateral | collateral; approval time | approval rate | pre-season |
| WF-038 | Extension support | Get technical advice | Advisory need | Farmer, Camp Extension Officer | query → advice | ADEO diary, guides | phone, meetings | topic; channel | officer ratio 1:1200+ | advice reach | season |
| WF-039 | Digital advisory services | Get info digitally | Info need | Farmer, provider, MNO | query → digital advice | SMS/app records | phone | trust; channel | connectivity; literacy | digital reach | season |
| WF-040 | Emergency response | React to shocks | Drought/flood/pest | Farmer, DMMU, govt, NGO | alert → relief/action | disaster assessment | — | declare; respond | slow response; access | response time | event |
| WF-041 | Season close-out | Review & prepare next | Season end | Farmer, farm manager, extension | records → season review | close-out summary | — | carry-over; lessons | poor records; recall | review completion | Sep–Oct |

*(41 workflows registered to fully cover the 40 requested plus season close-out.)*

## 2. Key end-to-end deep-dives (Zambia-specific)

### 2.1 Input procurement via FISP e-voucher (WF-007/008)
Trigger: FISP registration opens (pre-season). Steps: farmer registers at **District Agriculture Office** (requires NRC, registered mobile number, proof of farmland, farmer-group/cooperative membership) → **e-KYC** verification in **ZIAMIS** → farmer pays contribution (**K400**; government adds **K8,000**) by bank/mobile money → SMS confirmation → **redeeming code created within 24 hrs** → farmer visits a **ZIAMIS-accredited agro-dealer**, presents **NRC + code**, selects inputs, **signs the GIN (goods issue note/invoice)**, receives transaction SMS; **30-day** redemption window [SRC-0045] (MoA, pub. 2025; confidence 90/100; retrieved 2026-07-05); [SRC-0048] (PDU, pub. 2025; confidence 84/100; retrieved 2026-07-05).
- Scale/variation: **~740k farmers / 74 districts (2024/25)** → all 116 districts / >1M (2025/26); **~650–779 accredited agro-dealers** [SRC-0046][SRC-0047]. Non-FISP farmers buy at market price (cash/credit).
- Decision points: eligibility (smallholder ≤5 ha), agro-dealer choice, input mix. Pain: stock-outs, late redemption vs planting window, database omissions (650k omitted after scrutiny) [SRC-0046]. Info produced: registration, transactions in ZIAMIS. Info consumed: farmer NRC, mobile number, farmland proof.

### 2.2 Extension support (WF-038)
Delivered through the **block/camp network**: PACO → DACO → **Block Extension Officer** → **Camp Extension Officer (CEO)** (day-to-day farmer contact), with **346 blocks and 1,757 camps**; camps split into 4–6 zones and farmer groups [SRC-0050] (MEAS, pub. 2014; confidence 80/100; retrieved 2026-07-05). Constraint: **extension-to-farmer ratio up to 1:1,200 (crops), 1:3,000 (livestock)**; Farmer Field Schools/study groups used to extend reach [SRC-0049] (MoA, pub. 2023; confidence 85/100; retrieved 2026-07-05).

### 2.3 Marketing, storage & warehouse receipts (WF-026/029/031)
- **Food Reserve Agency (FRA)** buys maize at a **pan-territorial price (often above market)** at rural **depots**; dominant maize buyer; stores/exports/sells to millers [SRC-0052] (IZA/MSU, pub. 2015; confidence 82/100; retrieved 2026-07-05).
- **ZAMACE** operates an online trading platform and a **certified Warehouse Receipt System**; **community aggregation centres feed district certified warehouses**; warehouse receipts usable as **loan security** (Agricultural Credit Act); FRA–ZAMACE partnership for price discovery [SRC-0051] (PARM, pub. 2019; confidence 82/100; retrieved 2026-07-05); [SRC-0053] (ZAMACE, pub. 2023; confidence 72/100; retrieved 2026-07-05).
- Quality gates at aggregation: grading, **moisture meters, scales, shellers** [SRC-0051].

### 2.4 Contract farming / outgrower (WF-030)
Agribusiness provides **inputs on credit at season start (Oct–Dec)** and **buys back the harvest from June**, deducting input debt; **village-based distributors** mobilise, contract, distribute inputs, monitor crops and recover credit, each managing **15–20 farmers**; firms keep a **central contract-farmer registry** (cotton/tobacco/sugarcane; e.g. cotton outgrowers ~35,000) [SRC-0054] (J-PAL, pub. 2020; confidence 80/100; retrieved 2026-07-05); [SRC-0055] (World Bank, pub. 2009; confidence 78/100; retrieved 2026-07-05). Key risk: **side-selling** (farmers selling elsewhere to escape debt).

### 2.5 Yield estimation & reporting (WF-025/035)
National **Crop Forecast Survey** and **Post-Harvest Survey** (ZamStats/MoA); **National Remote Sensing Centre (est. 1999)** applies remote sensing to crop mapping and yield forecasting [SRC-0056] (UNCTAD, pub. 2023; confidence 80/100; retrieved 2026-07-05).

## 3. Cross-cutting operational characteristics
- **Rain-fed & seasonal:** most smallholders depend on rain; single main cropping season; timing is the dominant constraint [SRC-0056][SRC-0057].
- **Mostly offline & paper/verbal:** field records, extension advice, and many transactions are manual; mobile money and SMS (ZIAMIS) are the main digital touchpoints.
- **Intermittent connectivity** in rural camps; feature phones common.
- **Smallholder dominance:** ~70% of labour force in agriculture; 400,000+ in outgrower schemes [SRC-0057].

## 4. Recorded uncertainties (→ Risk/Gap registers)
- Exact per-workflow tool/software usage at farm level (mostly manual) to be confirmed by field interviews (WP2.1 later phase).
- Cooperative operational procedures; agro-dealer back-office processes; warehouse operator SOPs — primary SOPs not yet collected.
