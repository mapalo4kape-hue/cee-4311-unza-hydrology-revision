# AgriMine Nexus — ID Registry

> Central allocator for all object IDs. To mint a new ID, take `next` for the prefix, use it, then increment `next` in the same commit. **IDs are never reused or renumbered.**

| Prefix | Object | Next | Notes |
|--------|--------|------|-------|
| `SRC-` | Evidence/source | 0122 | ...0114-117 WP4 products; 0118-121 WP4.3 integrations |
| `F-` | Finding | 0090 | ...0085-0087 WP4.3 integrations; 0088-0089 WP4.2 capabilities |
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
| `FR-` | Functional requirement | 001 | |
| `NFR-` | Non-functional requirement | 001 | |
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
| `SRV-` | Survey | 0001 | |
| `ACT-` | Activity | 004 | 001–003 allocated |
