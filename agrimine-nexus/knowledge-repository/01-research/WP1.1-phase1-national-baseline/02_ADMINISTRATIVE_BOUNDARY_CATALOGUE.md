---
id: WP1.1-P1-ADMIN
title: Administrative Boundary Catalogue — Zambia (WP1.1 Phase 1)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 1 — Foundation Research
work_package: WP1.1
industry: cross-industry
topic: Administrative geography
keywords: [provinces, districts, constituencies, wards, chiefdoms, ISO-3166-2, CRS, boundaries]
summary: Authoritative record of Zambia's administrative geography, codes, coordinate reference systems, and boundary data sources. Evidence acquisition only — no interpretation.
source: SRC-0003;SRC-0004;SRC-0005;SRC-0006;SRC-0007
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 92
evidence_level: 1
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../../02-evidence/EVIDENCE_REGISTER.csv]
related_requirements: []
related_entities: [ENT-LOCATION]
related_apis: []
related_modules: []
related_workflows: []
---

# Administrative Boundary Catalogue — Zambia

> Citation format: `[SRC-NN] (Organization, pub. date; confidence NN/100; retrieved 2026-07-05)`. This is an evidence record; no analysis or recommendations.

## 1. Administrative hierarchy (levels)

National → Province (ADM1) → District (ADM2) → Constituency (electoral) / Ward (ADM3) → (customary) Chiefdom / Village.

## 2. Administrative units (counts)

- Zambia is divided into **10 provinces** [SRC-0003] (ISO, pub. 2014-11-03; confidence 96/100; retrieved 2026-07-05).
- At the time of the 2022 Census, Zambia had **116 districts, 156 constituencies, and 1,858 wards** [SRC-0004] (ZamStats, pub. 2023; confidence 97/100; retrieved 2026-07-05).
- **Uncertainty (wards):** an open dataset lists 1,853 wards versus ZamStats' 1,858 [SRC-0004]. The ZamStats figure is treated as authoritative; the discrepancy is logged (`CONTRADICTS`) in the Gap Register.
- **Chiefdoms:** there is **no single fixed official count**; customary authority is held by **over 250 chiefs and sub-chiefs** [SRC-0005] (USAID/World Bank, pub. 2016; confidence 70/100; retrieved 2026-07-05). Recorded as an explicit uncertainty; an authoritative count (House of Chiefs / Ministry of Chiefs & Traditional Affairs) is a research gap.

## 3. Provinces and ISO 3166-2 codes

Source: ISO 3166-2:ZM [SRC-0003] (ISO, pub. 2014-11-03; confidence 96/100; retrieved 2026-07-05). Capitals per ISO/statoids.

| ISO code | Province | Capital |
|----------|----------|---------|
| ZM-01 | Western | Mongu |
| ZM-02 | Central | Kabwe |
| ZM-03 | Eastern | Chipata |
| ZM-04 | Luapula | Mansa |
| ZM-05 | Northern | Kasama |
| ZM-06 | North-Western | Solwezi |
| ZM-07 | Southern | Choma |
| ZM-08 | Copperbelt | Ndola |
| ZM-09 | Lusaka | Lusaka |
| ZM-10 | Muchinga | Chinsali |

Note: Muchinga (ZM-10) was added to ISO 3166-2 on 2014-11-03 [SRC-0003]. Lusaka is the national capital [SRC-0004].

## 4. Administrative codes
- **National:** ISO 3166-1 alpha-2 **ZM**, alpha-3 **ZMB**, numeric **894** [SRC-0009] (Wikipedia, pub. 2026; confidence 70/100; retrieved 2026-07-05) — to corroborate against the ISO primary at next pass.
- **Province:** ISO 3166-2 `ZM-01`…`ZM-10` [SRC-0003].
- **District:** no ISO classification exists for districts; secondary schemes (e.g. HASC, ad-hoc `ZM-<prov>-<n>`) are used by third parties and are **not** official — flagged as a gap for an official district code list (ZamStats/Ministry of Local Government).

## 5. Coordinate reference systems (CRS)
- **Geographic:** WGS84 (EPSG:4326) is the common modern reference [SRC-0006] (EPSG, pub. 2024; confidence 90/100; retrieved 2026-07-05).
- **Projected (national mapping):** UTM zones **34S, 35S, 36S** on the **Arc 1950** datum (Clarke 1880 ellipsoid) — EPSG **20934 / 20935 / 20936**; central meridians 21°E / 27°E / 33°E [SRC-0006].
- **Seamless national grid:** no single official UTM zone covers Zambia; a unified plane coordinate system (central meridian 28°E, scale factor 0.9984, false easting 800,000 m) has been proposed in academic work for country-wide mapping [SRC-0007] (UNZA, pub. 2019; confidence 75/100; retrieved 2026-07-05).

## 6. Boundary data sources (spatial formats, licensing, quality)

| Source | Levels | Format | Licence | Quality note |
|--------|--------|--------|---------|--------------|
| ZamStats (census GIS) | ADM0–ADM3 | (to confirm) | Official (confirm) | Authoritative for 2022 boundaries [SRC-0004] |
| geoBoundaries | ADM0–ADM3 | GeoJSON/SHP | CC-BY/ODbL | Academic, versioned (see Master Source Register MSR-038) |
| GADM | ADM0–ADM3 | SHP/GPKG | Free non-commercial | Vintage may lag official changes |
| HDX / OCHA | ADM0–ADM3 | SHP/GeoJSON | Mostly open | Often mirrors official/UN boundaries |
| OpenStreetMap | mixed | PBF/GeoJSON | ODbL | Completeness varies rurally |

## 7. Gazette references & boundary update history
- New districts have been created over recent years (post-2011 and post-2021), and "recently established new districts" are noted as not-well-understood in independent literature [SRC-0005]. **Official gazette notices / Statutory Instruments** establishing districts and boundary changes are a **research gap** to be closed from the Government Gazette / Ministry of Local Government (recorded in the Gap Register).
- Muchinga province creation reflected in ISO on 2014-11-03 [SRC-0003].

## 8. Authoritative source hierarchy for administrative geography
1. **ZamStats** (census, official counts and enumeration boundaries) [SRC-0004].
2. **Ministry of Local Government & Rural Development** (district/ward establishment, gazette).
3. **Ministry of Lands / Survey Department** (surveyed boundaries, CRS).
4. **ISO 3166-2** (province codes) [SRC-0003].
5. Independent/open datasets (geoBoundaries, GADM, HDX, OSM) — for spatial geometry, corroborated against 1–4.

## 9. Recorded uncertainties (→ Gap Register)
- Exact current **district count** (post-2022 changes) and an **official district code list**.
- **Ward count** discrepancy (1,858 vs 1,853).
- **Official chiefdom count** and chiefdom boundary data.
- **Gazette/SI** references for boundary changes.
- Confirmation of ZamStats spatial **formats and licensing**.
