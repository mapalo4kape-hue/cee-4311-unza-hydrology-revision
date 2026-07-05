---
id: WP2.1-P2-MSC
title: Measurement Catalogue — Zambian Agriculture (WP2.1 Phase 2)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Measurements
keywords: [measurements, variables, units, instruments]
summary: Catalogue of measurable variables across agricultural operations, their units, capture instruments, and workflows. Information intelligence only.
source: SRC-0051;SRC-0056;SRC-0059
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 80
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../WP2.1-phase1-operations/08_AGRICULTURAL_KPI_REGISTER.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Measurement Catalogue — Zambian Agriculture

| ID | Measurement | Unit (typical) | Captured by (instrument) | Where/Workflow | Notes |
|----|-------------|----------------|--------------------------|----------------|-------|
| MS-01 | Area (field/farm) | hectare | GPS / Field Area Measure App | WF-003 | app-based GPS [SRC-0059] |
| MS-02 | Yield | t/ha or kg | scale / estimation | WF-024,025 | PHS/Crop Forecast [SRC-0056] |
| MS-03 | Grain moisture | % | moisture meter | WF-026,031 | grading gate [SRC-0051] |
| MS-04 | Weight (produce/inputs) | kg / t | scale | WF-025,029,031 | net weight on WR [SRC-0061] |
| MS-05 | Temperature (ambient) | °C | thermometer / station | WF-019 | weather |
| MS-06 | Rainfall | mm | rain gauge / satellite | WF-019 | ZMD/CHIRPS (WP1.1) |
| MS-07 | Humidity | % | hygrometer / station | WF-019 | weather |
| MS-08 | Soil pH | pH | lab / test kit | WF-004 | soil test |
| MS-09 | Nitrogen (N) | ppm/kg-ha | lab | WF-004,018 | fertility |
| MS-10 | Phosphorus (P) | ppm/kg-ha | lab | WF-004,018 | fertility |
| MS-11 | Potassium (K) | ppm/kg-ha | lab | WF-004,018 | fertility |
| MS-12 | Water usage | litres/m³ | meter / estimate | WF-012 | irrigation |
| MS-13 | Fuel usage | litres | fuel log | WF-022 | mechanised ops |
| MS-14 | Labour hours | hours | attendance | WF-020 | peaks |
| MS-15 | Machine hours | hours | service log | WF-021 | uptime |
| MS-16 | Travel distance | km | odometer/GPS | WF-028 | logistics |
| MS-17 | Storage temperature | °C | temp log | WF-027 | cold chain |
| MS-18 | Market price | ZMW/unit | market/ZAMACE/FRA | WF-029 | price discovery |
| MS-19 | Exchange rate | ZMW/USD | Bank of Zambia | WF-029,032 | macro (WP1.1) |
| MS-20 | Commodity grade | grade class | grading sieves/standards | WF-031 | quality [SRC-0051] |
| MS-21 | Seed/plant density | plants/ha | count | WF-011 | agronomy |
| MS-22 | Application rate | kg or L/ha | measure | WF-015,018 | inputs |

## Note
Most field measurements are **eyeballed or captured on paper**; instrumented measurements (moisture meter, scales, GPS area, weather station) cluster at **aggregation/warehouse, field mapping, and weather** points. No units are being defined as data types — this is an information inventory.
