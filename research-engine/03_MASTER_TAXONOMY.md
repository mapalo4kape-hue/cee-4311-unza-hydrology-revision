# AgriMine Nexus — Master Taxonomy (Deliverable 3 / Component 3)

> The controlled vocabulary for classifying **everything** in AgriMine Nexus research. Every artifact and entity is tagged with one or more taxonomy node IDs. The taxonomy is a directed hierarchy of **facets** (top-level) → **nodes** (children). It is extensible: new nodes are added via an activity record and allocated an ID from the `TAX-` series.
>
> **Node ID format:** `TAX-<FACET>.<n>` (e.g. `TAX-IND.1` = Agriculture). Every node records: **Definition · Parent · Children · Aliases · Related Concepts · Examples.**

---

## 0. Facet index (top-level classes)

| Facet | Code | Covers |
|-------|------|--------|
| Industries | `IND` | The productive sectors served |
| Business Domains | `DOM` | Cross-industry functional domains |
| Stakeholders | `STK` | People/organizations with an interest |
| Assets | `AST` | Things of value that are owned/managed |
| Equipment & Machines | `EQP` | Tools, machines, plant |
| Vehicles | `VEH` | Mobile transport/plant |
| Processes | `PRC` | Repeatable business processes |
| Activities | `ACT` | Discrete units of work |
| Inputs | `INP` | Consumed resources |
| Outputs | `OUT` | Produced goods/results |
| Products | `PRD` | Sellable goods |
| Services | `SVC` | Sellable services |
| Documents | `DOC` | Records & artifacts |
| Reports | `RPT` | Structured reporting outputs |
| Licenses & Permits | `LIC` | Authorizations |
| Regulations | `REG` | Binding legal/normative rules |
| Sensors | `SEN` | Measurement devices |
| Vehicles/Machines telemetry | `MAC` | Machine assets (see EQP/VEH) |
| Laboratories | `LAB` | Testing facilities |
| Organizations | `ORG` | Legal/organizational bodies |
| Locations | `LOC` | Geographic/administrative places |
| Weather | `WEA` | Atmospheric conditions |
| Environmental Factors | `ENV` | Ecological/environmental variables |
| Financial Records | `FIN` | Money-related records |
| Supply Chain Objects | `SCM` | Logistics/supply-chain items |
| Software Modules | `MOD` | Platform functional modules |
| Technology Components | `TEC` | Underlying technologies |
| AI Models | `AIM` | ML/AI capabilities |
| GIS Layers | `GIS` | Spatial data layers |
| IoT Devices | `IOT` | Connected devices |
| Drone Data | `DRN` | UAV-captured data products |
| Analytics | `ANA` | Analytical methods/outputs |
| KPIs | `KPI` | Performance indicators |
| Dashboards | `DSH` | Visual reporting surfaces |

## 1. Facet: Industries (`IND`)

| Node | Definition | Parent | Children | Aliases | Related | Examples |
|------|-----------|--------|----------|---------|---------|----------|
| `TAX-IND.1` Agriculture | Cultivation of crops and rearing of animals for food, fibre, income | IND | Crop production, Livestock, Aquaculture, Forestry | Farming, Agribusiness | `DOM.*`, `LOC` provinces | Maize farming, dairy |
| `TAX-IND.2` Mining | Extraction and processing of minerals | IND | Exploration, Extraction, Processing, Tailings mgmt | Extractives | `REG` mining law | Copper mine, quarry |
| `TAX-IND.3` Construction | Building of infrastructure and structures | IND | Buildings, Civil works, Roads | Building, Infrastructure | BOQ, BIM | Road project |
| `TAX-IND.4` Environmental Engineering | Managing environmental quality & compliance | IND | Waste, Water treatment, Air quality, EIA | EnviroEng | `REG` environmental | EIA, WWTP |
| `TAX-IND.5` Logistics & Supply Chains | Movement/storage of goods | IND | Transport, Warehousing, Cold chain | Logistics | `SCM.*` | Fleet, last-mile |
| `TAX-IND.6` Water Resources | Management of water bodies and supply | IND | Hydrology, Irrigation, Supply | Water | `ENV`, `GIS` | Dam, borehole |
| `TAX-IND.7` Government & Compliance | Public administration & regulatory oversight | IND | Licensing, Taxation, Reporting | Public sector | `REG`, `LIC` | ZRA, ZEMA |
| `TAX-IND.8` Industrial Supply | Industrial inputs & equipment supply | IND | Distribution, Procurement | Industrial | `SCM` | Spare-parts supplier |

## 2. Facet: Business Domains (`DOM`)

Cross-industry functions each industry shares. Nodes: `TAX-DOM.1` Operations · `.2` Procurement · `.3` Finance & Accounting · `.4` HR & Workforce · `.5` Asset Management · `.6` Compliance & Regulatory · `.7` Health, Safety & Environment (HSE) · `.8` Sales & Marketplace · `.9` Logistics & Distribution · `.10` Quality Assurance · `.11` Maintenance · `.12` Reporting & Analytics.
*(Each: Definition = the functional area; Parent = DOM; Children = sub-functions; Aliases; Related = relevant `PRC`/`MOD`; Examples.)*

## 3. Facet: Stakeholders (`STK`)

`TAX-STK.1` Government Agency · `.2` Regulator · `.3` Farmer · `.4` Mining Company · `.5` Contractor · `.6` Engineer · `.7` Environmental Professional · `.8` Supplier · `.9` Financial Institution · `.10` NGO · `.11` University/Research · `.12` Technology Provider · `.13` Buyer/Off-taker · `.14` Cooperative · `.15` Employee/Worker · `.16` Community.

*Node attribute pattern (example):*
- **`TAX-STK.3` Farmer** — *Definition:* an individual or entity engaged in crop/livestock production. *Parent:* STK. *Children:* Smallholder, Commercial, Cooperative member. *Aliases:* Grower, Producer. *Related:* `ENT-FARMER`, `IND.1`, `DOM.1`. *Examples:* smallholder maize farmer, commercial dairy farm owner.

## 4. Facet: Assets (`AST`) & Equipment (`EQP`) & Vehicles (`VEH`)

- **AST:** Land, Building, Water body, Crop stand, Livestock herd, Mineral deposit, Machinery, Infrastructure, Inventory, Financial asset.
- **EQP:** Tractor, Plough, Harvester, Irrigation pump, Drill rig, Crusher, Excavator, Concrete mixer, Generator, Lab instrument.
- **VEH:** Truck, Haul truck, Tractor-unit, Pickup, Loader, Drone (see `DRN`), Boat.

## 5. Facet: Processes (`PRC`) & Activities (`ACT`)

- **PRC** (repeatable, cross-cutting): Land preparation, Planting, Irrigation, Harvesting, Exploration, Drilling, Extraction, Processing, Procurement, Inspection, Permitting, Reporting, Dispatch, Warehousing, Maintenance, Compliance audit.
- **ACT** (discrete work units within a process): e.g. `Soil test`, `Apply fertilizer`, `Blast`, `Assay sample`, `Raise purchase order`, `Weighbridge capture`.

## 6. Facet: Inputs (`INP`) / Outputs (`OUT`) / Products (`PRD`) / Services (`SVC`)

- **INP:** Seed, Fertilizer, Pesticide, Fuel, Water, Explosives, Cement, Aggregate, Labour, Energy, Spare parts.
- **OUT:** Harvested crop, Milk, Ore, Concentrate, Constructed structure, Treated water, Waste, Emissions.
- **PRD:** Grain, Livestock product, Refined metal, Building unit, Packaged goods.
- **SVC:** Extension advisory, Assaying, Inspection, Transport, Equipment rental, Compliance consulting, Data/analytics service.

## 7. Facet: Documents (`DOC`), Reports (`RPT`), Licenses/Permits (`LIC`), Regulations (`REG`)

- **DOC:** Contract, Invoice, Purchase order, Delivery note, BOQ, EIA report, Assay certificate, Weighbridge ticket, Inspection form, Payslip.
- **RPT:** Production report, Compliance report, Financial statement, Environmental monitoring report, Safety report, KPI dashboard export.
- **LIC:** Mining licence, Water permit, EIA approval, Business licence, Import/export permit, Operating permit, Professional registration.
- **REG:** Act, Statutory Instrument, National standard, International standard, Reporting requirement, Safety requirement, Tax regulation. (Each REG node links to the source in `08-regulations`.)

## 8. Facet: Sensors (`SEN`), Laboratories (`LAB`), IoT Devices (`IOT`), Drone Data (`DRN`)

- **SEN:** Weather station, Soil moisture sensor, Water quality sensor, Air quality sensor, GPS tracker, RFID reader, Energy meter, Fuel sensor, Vibration/telemetry sensor.
- **LAB:** Soil lab, Assay lab, Water/effluent lab, Materials-testing lab.
- **IOT:** (device instances of SEN) — gateway, edge node, telemetry unit.
- **DRN:** RGB imagery, Thermal imagery, Multispectral imagery, LiDAR point cloud, Orthomosaic, Survey DSM/DEM.

## 9. Facet: Organizations (`ORG`), Locations (`LOC`), Weather (`WEA`), Environmental Factors (`ENV`)

- **ORG:** Government ministry, Regulatory authority, Company, Cooperative, NGO, University, Bank, Insurer.
- **LOC:** Country (Zambia), Province (×10), District, Ward, Site/Facility, Field/Block, Coordinate/Geofence.
- **WEA:** Rainfall, Temperature, Humidity, Wind, Solar radiation, Evapotranspiration, Forecast.
- **ENV:** Soil type, Water quality, Air quality, Noise level, Biodiversity, Carbon emissions, Land use.

## 10. Facet: Financial (`FIN`) & Supply Chain (`SCM`)

- **FIN:** Transaction, Invoice, Payment, Payroll record, Loan, Subsidy, Tax record, Budget, Cost centre, Revenue stream.
- **SCM:** Shipment, Consignment, Inventory item, Warehouse, Route, Order, Delivery, Cold-chain unit, Customs declaration.

## 11. Facet: Software Modules (`MOD`) & Technology Components (`TEC`)

- **MOD:** Farm Management, Mining Operations, Construction PM, Environmental Compliance, Logistics/Fleet, Procurement, Finance/ERP, Marketplace, Reporting/BI, Admin/Identity.
- **TEC:** Microservices, Serverless, Event-driven bus, Offline sync, Identity/IAM, Spatial DB, Time-series DB, Object storage, Message queue, API gateway.

## 12. Facet: AI (`AIM`), GIS (`GIS`), Analytics (`ANA`), KPIs (`KPI`), Dashboards (`DSH`)

- **AIM:** Computer vision, ML classifier, Forecasting model, LLM/NLP, OCR, Recommendation engine, Anomaly detection, Digital twin.
- **GIS:** Land-use layer, Soil layer, Hydrology layer, Mining-concession layer, Elevation model, Geofence layer, Crop-health (NDVI) layer.
- **ANA:** Descriptive, Diagnostic, Predictive, Prescriptive, Spatial analytics.
- **KPI:** Yield/ha, Downtime %, Compliance rate, On-time delivery %, Cost per tonne, Water-use efficiency, Incident rate.
- **DSH:** Executive dashboard, Operations dashboard, Compliance dashboard, Research Quality dashboard (see D10).

---

## 13. Governance of the taxonomy

- New nodes require an activity record and a new `TAX-` ID; nodes are never renumbered.
- Deprecated nodes are marked `[DEPRECATED → TAX-xx]`, never deleted (traceability).
- Every knowledge-graph entity (D4/D8) references at least one taxonomy node via its `classification` attribute.
