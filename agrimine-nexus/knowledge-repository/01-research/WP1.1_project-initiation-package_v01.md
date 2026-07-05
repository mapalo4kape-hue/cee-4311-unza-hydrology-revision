---
id: WP1.1-PIP
title: Project Initiation Package — Work Package 1.1 National Intelligence
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 1 — Foundation Research
work_package: WP1.1
industry: cross-industry
topic: National Intelligence (Zambia operating environment)
keywords: [zambia, national-intelligence, demographics, economy, infrastructure, digital-readiness, PIP, initiation]
summary: Defines exactly how WP1.1 National Intelligence research will be executed before data collection begins — objectives, scope, research questions, deliverables, sources, stakeholders, outputs, risks, acceptance criteria, and activity plan.
source: derived
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 100
evidence_level: 1
status: in-review
version: v01
reviewer: pending (QA Gate 1 — Scope completeness)
approval_status: pending
related_documents: [MREP_Internalisation.md, research-engine/02_REPOSITORY_BLUEPRINT.md, research-engine/06_REQUIREMENT_TRACEABILITY_FRAMEWORK.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Project Initiation Package (PIP) — Work Package 1.1: National Intelligence

**Client/Programme:** AgriMine Nexus · **Stage:** 1 (Foundation Research) · **Work Package:** WP1.1
**Prepared by:** Research Consultant · **Date:** 2026-07-05 · **Status:** For QA Gate 1 review

> **What this document is:** the consulting-style plan that defines *how* National Intelligence research will be executed. It is produced **before** any data is collected. It commits us to specific objectives, questions, sources, deliverables, and acceptance criteria so the work is scoped, auditable, and repeatable.
>
> **What this document is not:** it contains **no findings and asserts no statistics**. Any organisations named under *Required Sources* are **candidate/target sources to be verified at collection**, not factual claims. All future findings will carry inline citations per the [Citation Standard](../../CITATION_STANDARD.md).

---

## 1. Objectives

WP1.1 exists to answer one overarching question: **"What is the operating environment of Zambia, in enough operational and quantitative detail to design, build, and scale AgriMine Nexus with confidence?"**

Concretely, WP1.1 must answer:

- **O1.** Who lives in Zambia, where, and with what characteristics (population, settlement, workforce, literacy, connectivity)?
- **O2.** What is the structure, size, and trajectory of the economy — nationally, by sector, and by province/district?
- **O3.** What physical infrastructure exists (transport, energy, water, telecoms, storage) and how reliable/accessible is it?
- **O4.** How digitally ready is the country — device ownership, internet/mobile penetration, mobile money, digital skills, e-government?
- **O5.** How is the country administratively organised (provinces, districts, wards, traditional authorities) and how does that map to data availability?
- **O6.** What are the national development priorities and policies that AgriMine Nexus must align with?
- **O7.** Where are the environmental and climatic conditions (rainfall, temperature, water resources) that shape agriculture, mining, construction, and logistics?
- **O8.** What data sources, portals, and datasets exist, who owns them, and how current/reliable are they?
- **O9.** What national-level risks, constraints, and opportunities (market, digital, regulatory, logistical) are relevant to the platform?
- **O10.** What entities, relationships, and requirement candidates emerge that feed the knowledge graph and later stages?

**Definition of success for the objectives:** every objective O1–O10 has evidence-backed answers (multiple independent sources where material), a confidence score, and at least one downstream knowledge-graph entry or requirement candidate.

---

## 2. Scope

### 2.1 In scope
- **Geography:** the Republic of Zambia — national level, all **10 provinces**, and district level (≈116 districts; exact current count to be verified against ZamStats / Ministry of Local Government at collection).
- **Themes (the 12 MREP WP1.1 topics):** demographics; economy; infrastructure; provinces & districts; internet & mobile penetration; financial inclusion; digital maturity; trade & logistics; energy; climate; water resources; national development priorities.
- **Time horizon:** most recent authoritative data, with **historical trend** (last ~10 years where available) and **published forecasts** (next 5 years where available).
- **Cross-cutting (per MREP §5):** stakeholder analysis, risk assessment, AI/GIS/IoT/integration opportunities, KPIs, data entities, security/offline/accessibility considerations at the national level.

### 2.2 Out of scope (deferred to later work packages)
- Deep **industry operational** detail (crop agronomy, mining process engineering, construction methods) → Stage 2 (WP2.1–2.5).
- **Technology product** evaluation (specific AI models, GIS stacks, IoT vendors) → Stage 3.
- **Competitor** benchmarking → Stage 4.
- **Business model / pricing / GTM** → Stage 5.
- **Primary data collection** (field interviews, surveys, sensor deployment) — WP1.1 relies on **secondary/desk research**; primary collection is planned but executed later where gaps demand it.
- Countries beyond Zambia (regional/continental scaling context noted only where it frames Zambia).

### 2.3 Assumptions & constraints
- `[ASSUMPTION]` Authoritative Zambian statistics are accessible online or via published reports; where paywalled/unavailable, gaps will be logged (Risk R1).
- Desk research is primary; no budget assumption is made for paid datasets unless flagged.
- All outputs are version-controlled in the knowledge repository and comply with the Research Engine standards.

---

## 3. Research Questions

> Structured, granular questions grouped by theme. Each group has an ID prefix; individual questions are numbered for traceability (e.g. `RQ-ECON-07`). These become the checklist the research must close out. **~250 questions.**

### 3.1 Demographics & Population (`RQ-DEMO`)
1. Total national population (latest census) and reference date?
2. Population by each of the 10 provinces?
3. Population by district?
4. Population density by province and district?
5. Urban vs rural population split, nationally and by province?
6. Population growth rate (annual %), historical 10-year trend?
7. Age structure / population pyramid (youth %, working-age %, elderly %)?
8. Median age nationally and by province?
9. Sex ratio by province?
10. Household count and average household size by province?
11. Fertility rate and its trend?
12. Life expectancy nationally and by province?
13. Migration patterns (rural–urban, cross-border, internal by province)?
14. Literacy rate by province, by sex?
15. Educational attainment distribution?
16. Language distribution / dominant languages by province?
17. Labour force size and participation rate?
18. Employment by sector (agriculture, mining, services, manufacturing)?
19. Formal vs informal employment share?
20. Youth unemployment rate?
21. Poverty headcount ratio nationally and by province (rural vs urban)?
22. Population projections for next 5–10 years (national, provincial)?

### 3.2 Economy — National (`RQ-ECON`)
1. Nominal and real GDP (latest year, currency, source)?
2. GDP growth rate — latest and 10-year historical trend?
3. GDP per capita and its trend?
4. GDP composition **by sector** (agriculture, mining, manufacturing, construction, services, utilities)?
5. Agriculture's contribution to GDP (% and value)?
6. Mining's contribution to GDP (% and value)?
7. Construction's contribution to GDP?
8. Logistics/transport contribution to GDP?
9. GDP **by province** (where published)?
10. GDP **by district** (where published or estimable)?
11. Inflation rate (headline, food, non-food) and trend?
12. Policy interest rate / monetary policy stance?
13. Exchange rate (ZMW vs USD) and volatility trend?
14. Government budget size, revenue, and expenditure breakdown?
15. Public debt level (domestic/external) and debt-to-GDP?
16. Tax revenue composition (VAT, PAYE, mineral royalty, customs)?
17. Foreign Direct Investment (FDI) inflows by sector and origin?
18. Key exports (value, commodity mix — copper, agricultural)?
19. Key imports (value, categories)?
20. Trade balance and current account?
21. Sectoral growth forecasts (next 5 years, by source)?
22. Informal economy size estimate?
23. Cost of doing business indicators (where published)?
24. Access to finance for enterprises (SME credit availability)?
25. Major economic corridors and growth poles?

### 3.3 Economy — Provincial & District (`RQ-ECONP`)
1. Dominant economic activity per province?
2. Dominant economic activity per district?
3. Agricultural output/value by province (major crops, livestock)?
4. Mining activity and mineral type by province/district?
5. Construction activity concentration by province?
6. Provincial contribution to national exports?
7. Provincial poverty vs economic-output correlation?
8. Location of major markets, industrial areas, economic zones (MFEZ)?
9. Provincial GDP per capita disparities?
10. Cross-border trade hubs by province (border posts)?

### 3.4 Infrastructure — Transport (`RQ-INFRA-T`)
1. Total road network length (paved vs unpaved)?
2. Road network by province and condition?
3. Trunk/main/district/feeder road classification and coverage?
4. Rail network extent, operators, and condition?
5. Major airports and airstrips (location, capacity)?
6. Ports of entry / border posts (list, location, throughput)?
7. Inland water transport routes?
8. Road density relative to population/area by province?
9. Seasonal accessibility issues (rainy-season cutoffs)?
10. Major transport corridors (e.g., links to ports in neighbouring countries)?
11. Public transport and freight logistics providers?
12. Vehicle registration statistics and trends?

### 3.5 Infrastructure — Energy (`RQ-ENERGY`)
1. Total installed electricity generation capacity (by source: hydro, thermal, solar)?
2. Electricity generation mix and dependence on hydro?
3. National electrification rate (urban vs rural)?
4. Electrification rate by province and district?
5. Grid coverage and transmission/distribution network extent?
6. Reliability metrics (load-shedding frequency, outage duration)?
7. Electricity tariffs by customer class?
8. Off-grid / mini-grid / solar-home-system penetration?
9. Rural electrification programme targets and progress?
10. Petroleum/diesel supply chain and pricing?
11. Cooking-fuel mix (charcoal, firewood, LPG, electricity)?
12. Energy demand growth and forecasts?
13. Key generation assets (major dams/plants) and locations?
14. Renewable energy pipeline and policy incentives?

### 3.6 Infrastructure — Water & Sanitation (`RQ-WATER`)
1. Access to improved water sources (national, urban, rural)?
2. Water access by province and district?
3. Access to improved sanitation (national, urban, rural)?
4. Major water utilities and their service areas?
5. Borehole/groundwater reliance statistics?
6. Major rivers, lakes, and reservoirs (Zambezi, Kafue, Luangwa, Lake Kariba, etc.)?
7. Water resource availability and stress by basin?
8. Irrigation infrastructure and irrigated area?
9. Dam infrastructure (hydropower and water supply)?
10. Water quality monitoring coverage?
11. Flood- and drought-prone areas by province?
12. Transboundary water agreements relevant to Zambia?

### 3.7 Telecommunications & Internet (`RQ-TELCO`)
1. Mobile-cellular subscriptions (total, penetration %)?
2. Number and market share of mobile network operators?
3. Mobile broadband (3G/4G/5G) coverage by population and geography?
4. Internet penetration rate (individuals using internet)?
5. Fixed broadband subscriptions?
6. Smartphone vs feature-phone ownership split?
7. Mobile/internet penetration by province (urban vs rural)?
8. Average mobile data prices (per GB) and affordability?
9. Network coverage gaps / "not-spots" by province?
10. Data centre and fibre backbone infrastructure?
11. SIM registration and unique-subscriber estimates?
12. Quality-of-service metrics?
13. Spectrum allocation and regulatory environment?

### 3.8 Financial Inclusion (`RQ-FININC`)
1. % of adults with a formal financial account?
2. Mobile money account penetration and active-user rate?
3. Mobile money agent network size and distribution?
4. Financial inclusion by province, sex, and rural/urban?
5. Bank branch and ATM density by province?
6. Access to credit for individuals and SMEs?
7. Insurance penetration (agricultural insurance especially)?
8. Savings-group / cooperative membership prevalence?
9. Payment-system infrastructure (interoperability, national switch)?
10. Digital-payment adoption trend?
11. Remittance flows (domestic and international)?
12. Barriers to financial inclusion (documentation, distance, cost, trust)?

### 3.9 Digital Maturity & E-Government (`RQ-DIGITAL`)
1. National digital strategy / policy and its targets?
2. E-government services available and their maturity?
3. National digital ID system status and coverage?
4. Digital-skills levels in the population and workforce?
5. ICT contribution to GDP?
6. Tech/startup ecosystem presence (hubs, incubators)?
7. Government open-data portal(s) — existence, coverage, currency?
8. Data-protection and cybersecurity regulatory maturity?
9. Enterprise software adoption levels (ERP, accounting) by sector?
10. Prevalence of paper-based vs digital processes in key sectors?
11. Cloud adoption and hosting/localisation requirements?
12. Digital-divide indicators (gender, rural/urban, income)?

### 3.10 Trade & Logistics (`RQ-TRADE`)
1. Major trading partners (imports and exports)?
2. Border-post throughput and dwell times?
3. Logistics-performance indicators (where published)?
4. Warehousing and cold-chain capacity and location?
5. Key commodity flows (in/out) and corridors?
6. Customs procedures and digitisation status?
7. Regional trade bloc memberships (COMESA, SADC, AfCFTA) and implications?
8. Freight cost structures and transit dependencies (landlocked routing)?
9. Fuel and input supply-chain chokepoints?
10. Post-harvest loss estimates in agricultural supply chains?

### 3.11 Climate & Environment (`RQ-CLIMATE`)
1. Rainfall patterns and agro-ecological zones (I, IIa, IIb, III)?
2. Rainfall trends and variability by region?
3. Temperature ranges and trends?
4. Growing seasons and seasonal calendars by zone?
5. Drought frequency and affected regions?
6. Flood frequency and affected regions?
7. Climate-change projections relevant to agriculture/water?
8. Land-cover and land-use distribution?
9. Soil types and fertility by region?
10. Protected areas, forests, and biodiversity zones?
11. Environmental degradation hotspots (deforestation, mining impact)?
12. Availability of weather-station and satellite climate data?

### 3.12 National Development Priorities & Policy (`RQ-POLICY`)
1. Current National Development Plan (e.g., 8NDP) — pillars and targets?
2. Vision 2030 (or successor) long-term goals?
3. Sector strategies for agriculture, mining, energy, digital?
4. National priorities relevant to digitisation and industry?
5. Government reform programmes and flagship projects?
6. Alignment with SDGs and continental frameworks (Agenda 2063)?
7. Decentralisation policy and its data/administrative implications?
8. Investment-promotion priorities and incentives (ZDA)?
9. Public-sector digitisation commitments?
10. Policy gaps or contradictions relevant to the platform?

### 3.13 Data Landscape & Sources (`RQ-DATA`)
1. Which institutions publish authoritative statistics, and how current?
2. Which open-data portals exist and what do they cover?
3. What geospatial/GIS datasets are freely available (admin boundaries, roads, land use)?
4. What satellite/remote-sensing data is accessible for Zambia?
5. What weather/climate datasets and APIs are available?
6. What data licensing and usage restrictions apply?
7. Where are the biggest data gaps (theme × geography)?
8. How frequently is each key dataset updated?
9. What is the smallest reliable geographic unit per dataset (national/province/district/ward)?
10. Which datasets can be ingested directly vs require manual extraction?

*(Total ≈ 250 structured questions across 13 groups. Additional questions will be appended as sub-questions during collection and logged against these IDs.)*

---

## 4. Deliverables

WP1.1 will produce the following documents/artifacts (each authored from a Research Engine template, metadata-tagged, evidence-cited, and stored in the mapped repository folder):

| # | Deliverable | Description | Repo location |
|---|-------------|-------------|---------------|
| D1 | **Zambia Country Profile** | Consolidated national overview (geography, demographics, governance, economy snapshot) | `01-research` |
| D2 | **Economic Profile** | Structure, size, sectors, trends, forecasts; national + provincial | `01-research` |
| D3 | **Digital Readiness Report** | Connectivity, mobile money, digital skills, e-gov, digital divide | `01-research` |
| D4 | **Infrastructure Assessment** | Transport, energy, water, telecoms — coverage & reliability | `01-research` |
| D5 | **Technology Landscape** | National tech ecosystem, data-protection/cyber posture, cloud/localisation | `01-research` / `07-technology` |
| D6 | **Risk Assessment (National)** | National-level risks affecting platform rollout | risk register → `10-requirements` |
| D7 | **Province Profiles (×10)** | One profile per province | `01-research` |
| D8 | **District Profiles** | District-level fact sheets (prioritised, then expanded) | `01-research` |
| D9 | **Investment & Opportunity Report** | Market/digital/software opportunities inferred from the data | `12-business` (opportunities), `13-product` |
| D10 | **National Data Catalogue** | Inventory of every source/dataset (owner, currency, coverage, licence, access) | `02-evidence` + `15-datasets` |
| D11 | **National Knowledge-Graph Contribution** | Entities/relationships added to `GRAPH_NODES/EDGES.csv` | `10-requirements` |
| D12 | **Requirement Candidates (National)** | BR/FR/NFR candidates derived from findings | `10-requirements` (RTM) |
| D13 | **GIS Layer Inventory (National)** | Admin boundaries, roads, energy, water, land-use layers available | `07-technology/gis` + `17-maps` |

---

## 5. Required Sources

> **Candidate/target sources to consult and verify.** Grouped by ROM source tier. Existence and currency of each is confirmed at collection; nothing here is asserted as a finding.

### Tier 1 — Government & official (Zambia)
- Zambia Statistics Agency (**ZamStats**, formerly CSO) — Census 2022, Living Conditions Monitoring Survey, Labour Force Survey, national accounts.
- **Bank of Zambia** — monetary, exchange-rate, balance-of-payments, financial-stability data.
- **Ministry of Finance & National Planning** — budgets, National Development Plan (8NDP), debt.
- **ZICTA** (ICT Authority) — ICT/telecom surveys and coverage data.
- **Energy Regulation Board (ERB)**, **ZESCO**, **Rural Electrification Authority (REA)** — energy.
- **Road Development Agency (RDA)**, **RTSA** — roads and transport.
- **Water Resources Management Authority (WARMA)**, **NWASCO** — water resources and utilities.
- **Zambia Environmental Management Agency (ZEMA)** — environment.
- **Zambia Meteorological Department (ZMD)** — climate/weather.
- **Zambia Development Agency (ZDA)** — investment, MFEZs.
- **PACRA**, **Zambia Revenue Authority (ZRA)** — business registration, trade/customs.
- **Ministry of Local Government** — provinces/districts/wards administrative data.

### Tier 2 — Multilateral, academic, research
- **World Bank** (WDI, Zambia Economic Update, Poverty Assessment), **IMF** (Article IV, WEO).
- **UN** system: UNDP (HDI), FAO/FAOSTAT & GIEWS (agriculture/food), WFP, UNICEF, UN-Habitat.
- **African Development Bank (AfDB)** — country strategy, statistics.
- **ITU** (telecom indicators), **GSMA** (mobile/mobile-money), **FSD Zambia / FinScope** (financial inclusion).
- Universities & research institutes: **University of Zambia (UNZA)**, **IAPRI** (agricultural policy), peer-reviewed journals.

### Tier 3 — Industry & practitioner
- Industry associations (chambers of commerce/mines, bankers association).
- Consulting/market reports; operator annual reports (MNOs, banks, utilities).
- Technical manuals and vendor documentation.

### Tier 4 — Signal only (verify before use)
- News media, forums, blogs, social media — for pain-point signal, never as authoritative evidence.

### Geospatial / open / sensor data
- **OpenStreetMap**, **Humanitarian Data Exchange (HDX)**, **WorldPop**, **GADM/geoBoundaries** (admin boundaries).
- **Copernicus/Sentinel**, **NASA (Landsat, MODIS, SRTM/DEM)** — satellite/remote sensing.
- Climate/weather: **ZMD**, **NASA POWER**, **CHIRPS** (rainfall), **ERA5**.
- National open-data portal(s) — to be located and inventoried (D10).

---

## 6. Stakeholders

| Question | Stakeholders (national level) |
|----------|-------------------------------|
| **Who owns the information?** | ZamStats, Bank of Zambia, sector ministries & regulators (ERB, ZICTA, WARMA, ZEMA, RDA), utilities (ZESCO), multilaterals (WB/IMF/UN/AfDB). |
| **Who uses it?** | Government planners, investors, development partners, private enterprises, researchers — and, downstream, AgriMine Nexus itself. |
| **Who regulates it?** | Data-protection authority, ZICTA (ICT/data), sector regulators; statistics governed by ZamStats mandate. |
| **Who validates it?** | ZamStats (official statistics), peer review (academic), multilateral cross-checks (WB/IMF/UN), and our own cross-referencing (ROM Phase 3). |

A **Stakeholder Register** (using `stakeholder-profile.md`) will be produced for the national institutions above, feeding WP1.3 (Stakeholder Mapping) and the knowledge graph.

---

## 7. Expected Outputs

Beyond the narrative deliverables (§4), WP1.1 will generate structured, reusable outputs:

- **Tables:** population/economy/infrastructure/digital indicators — national, provincial, district — each cell cited.
- **Maps / GIS layers:** admin boundaries (province/district), roads, electrification, water resources, telecom coverage, agro-ecological zones, population density (`17-maps`, `07-technology/gis`).
- **Charts:** trend lines (GDP, inflation, penetration), sector composition, provincial comparisons.
- **Datasets:** cleaned CSVs per theme in `15-datasets` with a datasheet each.
- **Knowledge-graph entries:** entities (e.g., `ENT-LOCATION` for provinces/districts, `ENT-ORG` for institutions, `ENT-REGULATION`) and relationships (`LOCATED_AT`, `GOVERNED_BY`, `PART_OF`) in `GRAPH_NODES/EDGES.csv`.
- **Requirements (candidates):** e.g., offline-first (from connectivity gaps), multi-language support, mobile-money integration, province/district reference data — captured as `BR-/FR-/NFR-` in the RTM.
- **Entities & relationships:** the national reference model (provinces, districts, institutions) reused by every later work package.
- **Business opportunities (`OPP-`):** market-size signals, underserved regions, digital gaps.
- **Software opportunities:** platform capabilities implied by the national context (e.g., low-bandwidth sync, USSD/feature-phone support, GIS baselayers).

---

## 8. Risks

| ID | Risk | Likelihood | Impact | Mitigation |
|----|------|-----------|--------|------------|
| R1 | **Missing data** — no data at district/ward granularity for some themes | High | Med | Use best available level; flag gaps in Data Catalogue; triangulate with proxies; note as `[OPEN QUESTION]`. |
| R2 | **Conflicting statistics** — sources disagree (e.g., GDP, penetration) | High | Med | Record all values, prefer Tier-1/most-recent, log `CONTRADICTS`, lower confidence, document rationale. |
| R3 | **Outdated information** — latest available data is several years old | Med | Med | Timestamp every figure (publication + retrieval date); prefer most recent; note staleness in confidence. |
| R4 | **Political bias** — government figures may be optimistic | Med | Med | Cross-check with IMF/WB/UN independent sources; flag divergence. |
| R5 | **Regional bias** — over-representation of Lusaka/Copperbelt | Med | Med | Explicitly track coverage by province (dashboard panel); actively seek rural/underserved data. |
| R6 | **Commercial bias** — vendor/operator reports overstate coverage | Med | Low | Treat Tier-3 as claims; corroborate with regulator (ZICTA) data. |
| R7 | **Access/licensing** — paywalled or restricted datasets | Med | Med | Prefer open sources; log inaccessible datasets; escalate if critical. |
| R8 | **Scope creep** into Stage 2 industry detail | Med | Low | Enforce §2.2 boundaries at QA Gate 1; defer to correct WP. |
| R9 | **Currency/units inconsistency** (ZMW vs USD, rebasing) | Med | Low | Normalise units; state base year and FX date for every monetary figure. |

**Overall mitigation strategy:** every figure is timestamped and tiered; disagreements are preserved rather than hidden; coverage is monitored on the Quality Dashboard; gaps become explicit open questions rather than silent omissions.

---

## 9. Acceptance Criteria

WP1.1 is **complete** when **all** of the following hold (verified against the 8 MREP QA gates):

1. **Question closure:** every `RQ-*` question is answered or explicitly marked `[OPEN QUESTION]` with a reason and a gap entry.
2. **Deliverable completeness:** D1–D13 produced, each passing the ROM report quality checklist.
3. **Geographic coverage:** national + all 10 provinces profiled; districts covered at least at fact-sheet level (priority districts in depth).
4. **Evidence discipline:** 100% of factual claims carry compliant inline citations (org, publication date, confidence, retrieval date); every recommendation traces to evidence.
5. **Source quality:** material findings backed by ≥2 independent sources where they exist; Tier-1/2 preferred; verification rate ≥ 70% on the dashboard.
6. **Traceability:** every requirement candidate links up to a finding/evidence and down to at least a candidate entity/module; no orphans.
7. **Structured outputs:** knowledge-graph entries, datasets, and GIS layer inventory delivered and registered.
8. **Contradictions handled:** all `CONTRADICTS` links resolved or documented with rationale and confidence impact.
9. **Data catalogue:** every source used is a row in the Evidence Register; every dataset has a datasheet.
10. **QA sign-off:** QA Gates 1–8 recorded as passed in `QA_GATE_LOG.csv`.

**How quality is measured:** via the Research Quality Dashboard (D10 of the engine) — traceability completeness, evidence-quality index, verification rate, coverage by industry/province/stakeholder, contradiction load, and gate status.

---

## 10. Activity Plan

How the consultant (Cursor) will execute WP1.1, phase by phase (ROM 5-phase lifecycle), each step logged as an activity record:

**Phase 0 — Initiation (this PIP).** Approve scope at QA Gate 1. *(Current step.)*

**Phase 1 — Planning refinement (ACT-005).**
- Finalise the source shortlist; locate open-data portals and dataset access points; produce a data-collection matrix (theme × source × geographic level × access method).

**Phase 2 — Evidence collection (ACT-006 … per theme).**
- Collect per theme (demographics → economy → infrastructure → digital → provinces/districts → climate → policy → data landscape).
- Register **every** source in `EVIDENCE_REGISTER.csv` (`SRC-`), store files in `03-sources`, capture datasets in `15-datasets`.
- Pass QA Gate 2 (source validation) as sources are logged.

**Phase 3 — Validation (rolling).**
- Cross-reference figures; record contradictions; assign confidence; flag stale/biased data. QA Gates 3–4.

**Phase 4 — Knowledge extraction.**
- Populate the knowledge graph (provinces, districts, institutions, regulations); build tables/charts/GIS inventory; extract entities & relationships. 

**Phase 5 — Product translation.**
- Derive requirement candidates (offline-first, multi-language, mobile-money, reference data, GIS baselayers) into the RTM; log business/software opportunities. QA Gates 5–6.

**Assembly & review.**
- Compile D1–D13; run the dashboard; business-impact review (Gate 7); final review/sign-off (Gate 8); update the Work Package Tracker; write the closing activity record and Lessons Learned.

**Cadence & governance:** each activity is committed and pushed to GitHub with its own activity record (the standing directive). Progress is visible in the tracker and dashboard at all times.

---

### Sign-off
This PIP is submitted for **QA Gate 1 (Scope completeness)** review. On approval, execution proceeds to Phase 1 (ACT-005). No data collection begins until this PIP is approved.
