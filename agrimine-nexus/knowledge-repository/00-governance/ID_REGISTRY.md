# AgriMine Nexus — ID Registry

> Central allocator for all object IDs. To mint a new ID, take `next` for the prefix, use it, then increment `next` in the same commit. **IDs are never reused or renumbered.**

| Prefix | Object | Next | Notes |
|--------|--------|------|-------|
| `SRC-` | Evidence/source | 0122 | ...0114-117 WP4 products; 0118-121 WP4.3 integrations |
| `F-` | Finding | 0097 | ...0092-0093 WP5 business arch; 0094-0096 WP5.3 information arch |
| `INFO-` | Information object | 048 | 001-047 allocated (Enterprise Information Catalogue, WP5.3) |
| `DENT-` | Business/data entity | 033 | 001-032 allocated (Master Data Entity Catalogue, WP5.3) |
| `ATR-` | Business attribute | 057 | 001-056 allocated (Attribute Catalogue, WP5.3) |
| `IREL-` | Business relationship | 039 | 001-038 allocated (Relationship Catalogue, WP5.3) |
| `REF-` | Reference-data set | 026 | 001-025 allocated (Reference Data Register, WP5.3) |
| `GAP-IN` | Information gap | IN-09 | IN-01..08 allocated (WP5.3) |
| `DOM-` | Business domain | (mnemonic) | 24 domains allocated (Enterprise Domain Catalogue, WP5); mnemonic IDs |
| `BO-` | Business object | 031 | 001-030 allocated (Business Object Catalogue, WP5) |
| `EVT-` | Business event | 036 | 001-035 allocated (Business Event Catalogue, WP5) |
| `DRK-` | Domain risk | 13 | 01-12 allocated (WP5) |
| `DCON-` | Domain constraint | 11 | 01-10 allocated (WP5) |
| `INT-` | Integration entry | 0151 | 001-150 allocated (Master Integration Catalogue, WP4.3) |
| `GAP-I` | Integration gap | I11 | I01-I10 allocated (WP4.3) |
| `CAP-` | Business capability | 0171 | 001-170 allocated (Master Enterprise Capability Catalogue, WP4.2) |
| `GAP-C` | Capability gap | C09 | C01-C08 allocated (WP4.2) |
| `TECH-` | Technology (catalogue) | 0151 | 001-150 allocated (Global Technology Catalogue, WP3) |
| `GAP-T` | Technology gap | T10 | T01-T09 allocated (WP3) |
| `GAP-M` | Market/product gap | M09 | M01-M08 allocated (WP4) |
| `REG-` | Legal instrument | 0038 | 0001-0037 allocated (Legal Instrument Register) |
| `STK-` | Stakeholder | 076 | 001-075 allocated (Master Stakeholder Register) |
| `ORG-` | Organisation node | (mnemonic) | ORG-MOA/MRC/ZEMA/ZRA/BOZ/NCC/FRA/ZPPA/MMO/DPC in graph |
| `WF-L-` | Logistics workflow | L27 | L01-L26 allocated (WP2.5) |
| `CMP-` | Competitor product | 0249 | 0001-0248 allocated (Global Product Catalogue; 0154-0248 added WP4) |
| `WF-M/C/E-` | Industry workflows | see handbooks | mining/construction/environmental |
| `TX-/EV-/MS-/MD-/DC-/REL-` | Ag info objects | see catalogues | WP2.1-P2 information ecosystem |
| `WF-` | Workflow | 042 | 001-041 allocated (WP2.1 agriculture) |
| `LOC-` | Location instance | ZM + ZM01-ZM10 used | Zambia + 10 provinces in graph |
| `ENT-` | Knowledge entity | see Master Entity Catalogue | uses mnemonic ids (e.g. ENT-FARM) |
| `TAX-` | Taxonomy node | per facet | see Master Taxonomy |
| `BR-` | Business requirement | 001 | |
| `REQ-F-` | Functional requirement | 107 | 001-106 allocated (FRS, WP5) |
| `REQ-N-` | Non-functional requirement | 033 | 001-032 allocated (NFR, WP5) |
| `BR-` | Business rule | 021 | 001-020 allocated (WP5) |
| `CON-` | Constraint | 013 | 001-012 allocated (WP5) |
| `ASM-` | Assumption | 011 | 001-010 allocated (WP5) |
| `RSK-R` | Requirement risk | R11 | R01-R10 allocated (WP5) |
| `GAP-RQ` | Requirement gap | RQ-09 | RQ-01..08 allocated (WP5) |
| `FR-` | Functional requirement (legacy) | 001 | superseded by REQ-F- |
| `NFR-` | Non-functional requirement (legacy) | 001 | superseded by REQ-N- |
| `US-` | User story | 001 | |
| `AC-` | Acceptance criterion | derived from US | |
| `DB-` | Database entity | mnemonic | |
| `API-` | API endpoint | 001 | |
| `UI-` | UI screen | 001 | |
| `AR-` | Automation rule | 001 | |
| `AI-` | AI model/use case | 001 | |
| `GIS-` | GIS layer | 001 | |
| `IOT-` | IoT device profile | 001 | |
| `RPT-` | Report | 001 | |
| `KPI-` | KPI | 001 | |
| `RISK-` | Risk | 001 | |
| `OPP-` | Opportunity | 001 | |
| `BO-` | Business objective | 001 | |
| `ORG-` | Organization | 001 | |
| `CMP-` | Competitor profile | 0001 | |
| `INT-` | Interview record | 0001 | |
| `ACT-` | Activity | 004 | 001–003 allocated |
