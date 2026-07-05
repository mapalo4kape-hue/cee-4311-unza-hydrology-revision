# AgriMine Nexus — Master Entity Catalogue (Deliverable 8 / Component 7)

> The initial enterprise domain model: the core entities (`ENT-`) the platform will manage across all industries, with their key attributes and relationships. Each entity becomes a candidate database entity (`DB-`) during design. Entities are classified by the Master Taxonomy and linked in the Knowledge Graph (D4).

---

## 1. Cross-industry core entities

| Entity ID | Entity | Definition | Key attributes | Key relationships | Taxonomy |
|-----------|--------|-----------|----------------|-------------------|----------|
| `ENT-ORG` | Organization | Any legal/organizational body | name, type, registration_no, sector | employs `ENT-EMPLOYEE`; owns `ENT-ASSET` | `TAX-ORG` |
| `ENT-STAKEHOLDER` | Stakeholder | Party with an interest | name, category, influence, contact | linked to `ENT-ORG`, roles | `TAX-STK` |
| `ENT-EMPLOYEE` | Employee/Worker | Person performing work | name, role, skills, employer | has `ENT-ROLE`; performs `ENT-TASK` | `TAX-STK.15` |
| `ENT-ROLE` | Role | Function a person holds | title, permissions, domain | held by `ENT-EMPLOYEE` | `TAX-STK` |
| `ENT-TASK` | Task | Discrete unit of work | name, status, due, assignee | part of `ENT-WORKFLOW` | `TAX-ACT` |
| `ENT-ASSET` | Asset | Owned item of value | asset_no, type, value, condition | owned_by `ENT-ORG`; located_at `ENT-LOCATION` | `TAX-AST` |
| `ENT-EQUIPMENT` | Equipment/Machine | Machine/tool | model, serial, hours, status | monitored_by `ENT-SENSOR` | `TAX-EQP` |
| `ENT-VEHICLE` | Vehicle | Mobile transport/plant | reg_no, type, capacity, fuel | tracked_by `ENT-SENSOR` (GPS) | `TAX-VEH` |
| `ENT-LOCATION` | Location | Geographic/admin place | name, province, district, geometry | contains sub-locations | `TAX-LOC` |
| `ENT-SUPPLIER` | Supplier | Provider of inputs/services | name, category, rating | supplies via `ENT-CONTRACT` | `TAX-STK.8` |
| `ENT-BUYER` | Buyer/Off-taker | Purchaser of outputs | name, category | buys via `ENT-CONTRACT` | `TAX-STK.13` |
| `ENT-CONTRACT` | Contract | Binding agreement | parties, value, term, terms | generates `ENT-INVOICE` | `TAX-DOC` |
| `ENT-INVOICE` | Invoice | Billing document | number, amount, due, status | settled by `ENT-TRANSACTION` | `TAX-DOC` |
| `ENT-TRANSACTION` | Financial Transaction | Money movement | amount, date, type, account | relates to `ENT-INVOICE` | `TAX-FIN` |
| `ENT-INSPECTION` | Inspection | Formal check/audit | date, inspector, result | governed_by `ENT-REGULATION` | `TAX-DOC` |
| `ENT-PERMIT` | Permit/Licence | Authorization to operate | type, issuer, valid_from/to | governed_by `ENT-REGULATION` | `TAX-LIC` |
| `ENT-REGULATION` | Regulation | Binding rule | title, authority, effective_date | governs many entities | `TAX-REG` |
| `ENT-DOCUMENT` | Document | Any record/artifact | type, date, author | evidenced_by `SRC-` | `TAX-DOC` |
| `ENT-REPORT` | Report | Structured reporting output | type, period, author | derived from data | `TAX-RPT` |
| `ENT-WORKFLOW` | Workflow | Repeatable process instance | name, steps, owner | composed of `ENT-TASK` | `TAX-PRC` |
| `ENT-SENSOR` | Sensor/IoT device | Measurement device | type, unit, location, status | monitors assets/environment | `TAX-SEN`/`TAX-IOT` |
| `ENT-WEATHER` | Weather Observation | Atmospheric reading | variable, value, time, location | at `ENT-LOCATION` | `TAX-WEA` |
| `ENT-ENVSAMPLE` | Environmental Sample/Report | Env. measurement/record | medium, parameter, result | produced_by `ENT-LABORATORY` | `TAX-ENV` |
| `ENT-LABORATORY` | Laboratory | Testing facility | name, accreditation, tests | analyses `ENT-LABSAMPLE` | `TAX-LAB` |
| `ENT-LABSAMPLE` | Laboratory Sample | Sample sent for testing | id, medium, collected_at | analysed_by `ENT-LABORATORY` | `TAX-DOC` |
| `ENT-SATIMAGE` | Satellite Image | Remote-sensing raster | date, sensor, bounds | feeds `GIS-`/`AI-` | `TAX-GIS`/`TAX-DRN` |
| `ENT-DRONEDATA` | Drone Data | UAV-captured data product | type, date, area | feeds `GIS-`/`AI-` | `TAX-DRN` |

## 2. Agriculture entities

| Entity ID | Entity | Key attributes | Relationships |
|-----------|--------|----------------|---------------|
| `ENT-FARMER` | Farmer | name, type, cooperative | operates `ENT-FARM` |
| `ENT-FARM` | Farm | name, size, tenure, location | contains `ENT-FIELD` |
| `ENT-FIELD` | Field/Plot | area, soil, geometry | grows `ENT-CROP` |
| `ENT-CROP` | Crop | species, variety, season | on `ENT-FIELD`; has yield |
| `ENT-LIVESTOCK` | Livestock | species, count, health | on `ENT-FARM` |
| `ENT-INPUT` | Agri Input | type (seed/fertilizer), qty | consumed_by `ENT-CROP` |
| `ENT-HARVEST` | Harvest | crop, quantity, date, quality | output of `ENT-CROP` |

## 3. Mining entities

| Entity ID | Entity | Key attributes | Relationships |
|-----------|--------|----------------|---------------|
| `ENT-MINE` | Mine | name, mineral, licence | contains `ENT-PIT` |
| `ENT-PIT` | Pit/Shaft | id, depth, status | part_of `ENT-MINE` |
| `ENT-ORE` | Ore/Concentrate | grade, tonnage | output of extraction |
| `ENT-TAILINGS` | Tailings Facility | capacity, status | governed_by `ENT-REGULATION` |
| `ENT-ASSAY` | Assay Result | element, grade, method | from `ENT-LABSAMPLE` |
| `ENT-FLEET` | Haul Fleet | vehicles, utilization | subtype of `ENT-VEHICLE` |

## 4. Construction entities

| Entity ID | Entity | Key attributes | Relationships |
|-----------|--------|----------------|---------------|
| `ENT-PROJECT` | Construction Project | name, client, budget, schedule | has `ENT-BOQ` |
| `ENT-BOQ` | Bill of Quantities | items, quantities, rates | drives procurement |
| `ENT-SITE` | Site | location, phase | hosts `ENT-TASK` |
| `ENT-MATERIAL` | Material | type, qty, supplier | tracked on `ENT-SITE` |

## 5. Environmental & Logistics entities

| Entity ID | Entity | Key attributes | Relationships |
|-----------|--------|----------------|---------------|
| `ENT-EIA` | EIA Process | project, status, approval | produces `ENT-PERMIT` |
| `ENT-MONITORING` | Monitoring Point | parameter, threshold | uses `ENT-SENSOR` |
| `ENT-WAREHOUSE` | Warehouse | location, capacity | stores `ENT-INVENTORY` |
| `ENT-INVENTORY` | Inventory Item | sku, qty, location | in `ENT-WAREHOUSE` |
| `ENT-SHIPMENT` | Shipment | origin, dest, status | moves `ENT-INVENTORY` |
| `ENT-ROUTE` | Route | stops, distance, mode | used by `ENT-SHIPMENT` |

## 6. Expansion rule

This catalogue is the **seed** of the enterprise domain model. Work packages add entities (with new `ENT-` ids from the ID Registry), always specifying definition, attributes, relationships, taxonomy classification, and evidence. Entities are mirrored as rows in `GRAPH_NODES.csv` and become `DB-` candidates during architecture.
