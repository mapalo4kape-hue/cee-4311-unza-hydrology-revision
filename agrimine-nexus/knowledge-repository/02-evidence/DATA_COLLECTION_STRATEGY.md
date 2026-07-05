---
id: WP1.1-DCS
title: Data Collection Strategy — WP1.1
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 1 — Foundation Research
work_package: WP1.1
industry: cross-industry
topic: Data collection strategy
keywords: [collection, api, csv, pdf, gis, satellite, survey]
summary: Specifies, per source, how data will be collected (manual/API/CSV/PDF/portal/GIS/satellite/survey/interview/field) and its future integration potential for the platform.
source: derived
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 100
evidence_level: 1
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [MASTER_SOURCE_REGISTER.csv, SOURCE_VALIDATION_PLAN.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Data Collection Strategy — WP1.1

> How each source will actually be collected, and whether it is a candidate for **future live platform integration** (a signal for Stage 3 technology / integration work — recorded, not designed here).

## 1. Collection-method legend
- **MANUAL** — human download/extraction · **API** — programmatic endpoint · **CSV/XLSX** — tabular file · **PDF** — extract from report · **PORTAL** — web data portal · **GIS** — geospatial service/file · **SATELLITE** — earth-observation retrieval · **OFFICIAL-STATS** — official statistical release · **SURVEY/INTERVIEW/FIELD** — primary collection (deferred unless a gap forces it).

## 2. Per-source collection plan

| Source | Primary method | Secondary method | Format(s) | Future integration potential |
|--------|----------------|------------------|-----------|------------------------------|
| MSR-001 ZamStats | OFFICIAL-STATS / PDF | MANUAL XLSX | PDF/XLSX | Med — reference data feed if portal/API emerges |
| MSR-002 Bank of Zambia | PORTAL / CSV | MANUAL | CSV/XLSX | High — FX/rates API for finance module |
| MSR-003 MoFNP | PDF | MANUAL | PDF | Low — narrative policy |
| MSR-004 ZICTA | PDF | MANUAL | PDF | Med — connectivity reference |
| MSR-005/006/007 Energy | PDF | MANUAL | PDF | Med — tariffs/reliability feeds |
| MSR-008 RDA | PDF / GIS | MANUAL | PDF/GIS | High — road network baselayer |
| MSR-009 RTSA | PDF | MANUAL | PDF | Low |
| MSR-010/011 Water | PDF / GIS | MANUAL | PDF/GIS | Med — water infra layer |
| MSR-012 ZEMA | PDF | MANUAL | PDF | Med — compliance reference |
| MSR-013 ZMD | PDF | (see MSR-043/044 for API) | PDF | High — weather integration |
| MSR-014 ZDA | PDF | MANUAL | PDF | Low |
| MSR-016 ZRA | PDF | via MSR-022 API | PDF/CSV | Med — trade data |
| MSR-017 MLGRD | PDF | MANUAL | PDF | Med — admin reference data |
| MSR-018/019 Agri/Mines | PDF | MANUAL | PDF | Med — sector context |
| MSR-020/021 Health/Education | PDF | via MSR-036 | PDF/CSV | Low–Med |
| MSR-022 World Bank | API | CSV | CSV/JSON/API | High — indicator API ingestion |
| MSR-023 IMF | API | MANUAL | CSV/API | High — macro API |
| MSR-024 UNDP | API/PORTAL | CSV | CSV | Med |
| MSR-025 FAO | API (FAOSTAT) | CSV | CSV/API | High — agri/water API |
| MSR-026 WFP | API (VAM) | CSV | CSV/API | Med — market prices |
| MSR-027 UNICEF | PORTAL | CSV | CSV/XLSX | Low |
| MSR-028 AfDB | PDF | CSV | PDF/CSV | Low |
| MSR-029 ITU | CSV | MANUAL | CSV/XLSX | Med |
| MSR-030 GSMA | PDF | MANUAL | PDF/CSV | Med |
| MSR-031 FSD/FinScope | PDF | MANUAL | PDF/XLSX | Med |
| MSR-032/033 UNZA/IAPRI | PDF | MANUAL | PDF | Low |
| MSR-034 WHO | API (GHO) | CSV | CSV/API | Low |
| MSR-035 OpenStreetMap | API (Overpass) / GIS | Geofabrik extract | PBF/SHP/GeoJSON | High — GIS baselayer + live queries |
| MSR-036 HDX | API (CKAN) | MANUAL | CSV/SHP/GeoJSON | High — humanitarian/geo data pipeline |
| MSR-037 WorldPop | API / GIS | MANUAL | GeoTIFF/CSV | Med — population raster |
| MSR-038 geoBoundaries | API / GIS | MANUAL | GeoJSON/SHP | High — admin boundary reference |
| MSR-039 GADM | GIS (download) | MANUAL | SHP/GPKG | Med — boundary fallback |
| MSR-040 Copernicus | SATELLITE (STAC/API) | MANUAL | GeoTIFF/SAFE | High — EO pipeline (later stages) |
| MSR-041 NASA Earthdata | SATELLITE (API) | MANUAL | GeoTIFF/NetCDF | High — EO/DEM pipeline |
| MSR-042 CHIRPS | API / data server | MANUAL | GeoTIFF/NetCDF | High — rainfall feed |
| MSR-043 NASA POWER | API | MANUAL | CSV/JSON | High — weather/solar feed |
| MSR-044 ERA5 (CDS) | API (CDS) | MANUAL | NetCDF/GRIB | Med — reanalysis feed |

## 3. Sequencing (execution order at ACT-006+)
1. **Reference & boundaries first** (MSR-017/038/039) — the spatial spine everything joins to.
2. **Core statistics** (MSR-001/002/022/023) — demographics & economy.
3. **Infrastructure & sectoral** (transport, energy, water, telecoms, financial inclusion).
4. **Climate/EO** (MSR-013/040/041/042/043/044) — heavier data, pipeline-based.
5. **Data-landscape close-out** — finalise the National Data Catalogue and gap matrix.

## 4. Primary collection (deferred)
Surveys, interviews, and field collection are **not** used in WP1.1 desk research. If a critical gap cannot be closed from secondary sources, it is logged as a gap and proposed for a primary-collection activity in a later work package.

## 5. Guardrail
This is a **strategy**, not execution. No data is downloaded or analysed in ACT-005. Collection begins only after Gate-1/PIP review approval, at ACT-006.
