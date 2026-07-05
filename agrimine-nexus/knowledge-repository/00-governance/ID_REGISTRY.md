# AgriMine Nexus — ID Registry

> Central allocator for all object IDs. To mint a new ID, take `next` for the prefix, use it, then increment `next` in the same commit. **IDs are never reused or renumbered.**

| Prefix | Object | Next | Notes |
|--------|--------|------|-------|
| `SRC-` | Evidence/source | 0058 | 0001-02 gov; 0003-22 WP1.1-P1; 0023-44 WP1.1-P2; 0045-57 WP2.1-P1 |
| `F-` | Finding | 0053 | 0001-46 WP1.1; 0047-0052 WP2.1-P1 |
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
| `REG-` | Regulation | 0001 | |
| `BO-` | Business objective | 001 | |
| `STK-` | Stakeholder | 001 | |
| `ORG-` | Organization | 001 | |
| `CMP-` | Competitor profile | 0001 | |
| `INT-` | Interview record | 0001 | |
| `SRV-` | Survey | 0001 | |
| `ACT-` | Activity | 004 | 001–003 allocated |
