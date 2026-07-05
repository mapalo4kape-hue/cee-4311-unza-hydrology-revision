---
id: WP1.1-P1-NSDI
title: National Spatial Data Catalogue — Zambia (WP1.1 Phase 1)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 1 — Foundation Research
work_package: WP1.1
industry: cross-industry
topic: National spatial data infrastructure
keywords: [GIS, NSDI, cadastre, satellite, DEM, remote-sensing, portals]
summary: Catalogue of Zambia's spatial data infrastructure — official/open portals, survey and sector data sources, and remote-sensing products. Evidence acquisition only.
source: SRC-0017
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 78
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../../15-datasets/NATIONAL_DATA_INVENTORY.csv, ../../02-evidence/MASTER_SOURCE_REGISTER.csv]
related_requirements: []
related_entities: [ENT-LOCATION]
related_apis: []
related_modules: []
related_workflows: []
---

# National Spatial Data Catalogue — Zambia

> Identifies where authoritative and open spatial data for Zambia can be obtained. Access, licences, and dataset lists are to be confirmed at retrieval (validation status noted).

## 1. Official / government spatial sources
| Portal / source | Domain | Confirmed | Notes |
|-----------------|--------|-----------|-------|
| Ministry of Mines — **Mining Cadastre** eGov portal | portal.miningcadastre.com; mmmd.gov.zm | Yes | Trimble Landfolio; mining/non-mining rights; map portal; ZIMIS [SRC-0017] (MMMD, pub. 2024; confidence 88/100; retrieved 2026-07-05) |
| **ZamStats** census GIS / enumeration boundaries | zamstats.gov.zm | Partial | Authoritative admin boundaries 2022 [SRC-0004] |
| **Ministry of Lands / Survey Department** | (confirm) | No | National surveys, CRS, cadastral; primary portal to locate (gap) |
| **Zambia National Spatial Data Infrastructure (ZNSDI)** / geoportal | (confirm) | No | Reported NSDI framework/geoportal; authoritative confirmation pending (gap) |
| **WARMA** hydrological data | warma.org.zm | No | Water resources/basins (gap: dataset access) |
| **ZMD** meteorological data | meteozambia.gov.zm | No | Weather/climate station data (gap: access) |
| **ZEMA** environmental monitoring | zema.org.zm | No | Environmental/EIA (gap: access) |
| **Ministry of Agriculture** crop/land data | agriculture.gov.zm | No | Agro data (gap) |
| **RDA** transport datasets | rda.org.zm | No | Road network (gap: GIS access) |

## 2. Open / international geospatial sources (Zambia coverage)
| Source | Products | Format | Licence | Ref |
|--------|----------|--------|---------|-----|
| geoBoundaries | Admin boundaries ADM0–ADM3 | GeoJSON/SHP | CC-BY/ODbL | MSR-038 |
| GADM | Admin boundaries | SHP/GPKG | Free non-commercial | MSR-039 |
| Humanitarian Data Exchange (HDX) | Boundaries, population, roads, health sites | CSV/SHP/GeoJSON | Mostly open | MSR-036 |
| OpenStreetMap | Roads, POIs, buildings | PBF/SHP/GeoJSON | ODbL | MSR-035 |
| WorldPop | Gridded population | GeoTIFF | CC-BY-4.0 | MSR-037 |

## 3. Satellite imagery, DEM & remote-sensing products
| Source | Products | Resolution | Ref |
|--------|----------|-----------|-----|
| Copernicus / Sentinel (ESA) | Sentinel-1/2 imagery; land cover | 10–20 m | MSR-040 |
| NASA Earthdata | Landsat, MODIS, **SRTM DEM** | 30 m (SRTM) | MSR-041 |
| CHIRPS | Rainfall time series | ~5 km | MSR-042 |
| NASA POWER | Meteorology & solar | point/grid | MSR-043 |
| Copernicus CDS (ERA5) | Reanalysis climate | gridded | MSR-044 |

## 4. Coordinate reference systems for spatial data
WGS84 (EPSG:4326) for exchange; UTM 34S/35S/36S (Arc 1950; EPSG 20934–20936) for national projected mapping [SRC-0006] (EPSG, pub. 2024; confidence 90/100; retrieved 2026-07-05).

## 5. Recorded uncertainties (→ Gap Register)
- Existence/status of an official **ZNSDI geoportal** and **Survey Department** data portal.
- Dataset access, formats, and licences for WARMA, ZMD, ZEMA, RDA, Ministry of Agriculture.
- Authoritative national **land-cover** and **soil** datasets.
