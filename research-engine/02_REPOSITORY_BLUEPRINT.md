# AgriMine Nexus — Repository Blueprint (Deliverable 2 / Component 1)

> Authoritative specification of the knowledge-repository folder hierarchy. Every folder's **Purpose, Contents, Naming Convention, Versioning Rules, Metadata Requirements, and Relationships** are defined here. Physical folders live under [`../knowledge-repository/`](../knowledge-repository/).

---

## 1. Hierarchy overview

```
agrimine-nexus/
├── ROM_Internalisation.md          # governance (canonical)
├── MREP_Internalisation.md         # governance (canonical)
├── CITATION_STANDARD.md            # governance (canonical)
├── templates/                      # template library (canonical)
├── activity-log/                   # activity records (canonical)
├── research-engine/                # REIS specifications (this engine)
└── knowledge-repository/
    ├── 00-governance/              # pointers to canonical governance + ID registry
    ├── 01-research/                # completed research reports
    ├── 02-evidence/                # master Evidence Register + raw evidence index
    ├── 03-sources/                 # saved primary source files
    ├── 04-interviews/              # interview records
    ├── 05-surveys/                 # survey instruments + responses
    ├── 06-industries/              # {agriculture, mining, construction, environmental, logistics}
    ├── 07-technology/              # {ai, gis, iot, drones, cloud-architecture}
    ├── 08-regulations/             # acts, regulations, licences, standards
    ├── 09-competitors/             # competitor profiles + comparison matrices
    ├── 10-requirements/            # requirement registers + entity/data model
    ├── 11-architecture/            # enterprise architecture documents
    ├── 12-business/                # business model, pricing, GTM
    ├── 13-product/                 # feature catalogues, UI screens, reports
    ├── 14-integrations/            # integration catalogue + API registers
    ├── 15-datasets/                # structured datasets
    ├── 16-images/                  # photos, screenshots
    ├── 17-maps/                    # spatial/GIS map files
    ├── 18-videos/                  # video evidence
    ├── 19-templates/               # pointer → ../../templates (canonical)
    ├── 20-activity-logs/           # pointer → ../../activity-log (canonical)
    ├── 21-quality-assurance/       # QA gate logs + dashboard snapshots
    └── 22-archives/                # superseded/retired artifacts
```

> **Canonical-location note:** Governance, templates, and activity logs already exist at the `agrimine-nexus/` root and remain the single source of truth. Folders `00-governance`, `19-templates`, and `20-activity-logs` are kept in the hierarchy for completeness and contain a README pointing to the canonical location (no duplication).

## 2. Global conventions (apply to all folders unless overridden)

- **Naming:** lowercase-kebab, prefixed with the owning work package where relevant: `WP<stage.wp>_<slug>_vNN.md` (e.g. `WP1.1_zambia-country-profile_v03.md`). Registers use UPPER_SNAKE (e.g. `EVIDENCE_REGISTER.csv`).
- **Versioning:** semantic-ish `vNN` in the filename for human-facing docs; git history is the authoritative version trail. Superseded versions move to `22-archives/` with a `SUPERSEDED_BY` note. Never delete evidence.
- **Metadata:** every Markdown artifact starts with the YAML front-matter block defined in the [Metadata Standard (D5)](05_METADATA_STANDARD.md). Registers carry column headers per their standard.
- **Evidence:** every factual claim cites `SRC-NN` per the Citation Standard; the `SRC-NN` must exist in `02-evidence/EVIDENCE_REGISTER.csv`.

## 3. Per-folder specification

| Folder | Purpose | Typical contents | Naming | Versioning | Metadata | Relationships |
|--------|---------|------------------|--------|------------|----------|---------------|
| **00-governance** | Locate the binding rules + central ID allocation | Pointer README, `ID_REGISTRY.md` | fixed names | git history | n/a | Referenced by every folder |
| **01-research** | Finished research reports (ROM quality checklist) | `WPx.y_*_vNN.md` | WP-prefixed | vNN + archive | full front-matter | pulls from 02–09; feeds 10 |
| **02-evidence** | Master register of all evidence + raw-evidence index | `EVIDENCE_REGISTER.csv`, index notes | UPPER_SNAKE / WP-prefixed | append-only register | register columns (D7) | source of truth for all `SRC-` links |
| **03-sources** | Stored primary source files (PDFs, docs) | source files | `SRC-NNNN_<slug>.<ext>` | never overwrite | filename = SRC ID | 1:1 with Evidence Register rows |
| **04-interviews** | Stakeholder interview records | `INT-NNNN_<role>_vNN.md` | INT-prefixed | vNN | interview template metadata | feeds stakeholder profiles, findings |
| **05-surveys** | Survey instruments + response data | `SRV-NNNN_*` | SRV-prefixed | vNN | survey template metadata | feeds findings, KPIs |
| **06-industries** | Operational research per industry | subfolders per industry | WP-prefixed | vNN | full front-matter | Stage 2 home; feeds requirements |
| **07-technology** | Differentiating technology research | subfolders per tech | WP-prefixed | vNN | full front-matter | Stage 3 home; feeds architecture |
| **08-regulations** | Acts, regulations, licences, standards | `REG-NNNN_<title>.md` + source in 03 | REG-prefixed | supersede on amendment | reg metadata + effective date | feeds compliance matrices, requirements |
| **09-competitors** | Competitor profiles + comparison | `CMP-NNNN_<company>_vNN.md` | CMP-prefixed | vNN | competitor template | feeds feature catalogue, opportunities |
| **10-requirements** | Requirement registers + data/entity model | `REQUIREMENT_REGISTER.csv`, `DATA_MODEL.md`, `ENTITY_CATALOGUE.md` | UPPER_SNAKE | append/version | requirement metadata (D6) | central spine of traceability |
| **11-architecture** | Enterprise architecture blueprints | `ARC-NNNN_*_vNN.md` | ARC-prefixed | vNN | full front-matter | consumes requirements; feeds modules |
| **12-business** | Business model, pricing, GTM | `BIZ-*_vNN.md` | BIZ-prefixed | vNN | full front-matter | Stage 5 home |
| **13-product** | Feature catalogues, UI screens, reports | `FEA-/UI-/RPT-*` | prefixed | vNN | full front-matter | links requirements ↔ UI/reports |
| **14-integrations** | Integration catalogue + API opportunity register | `INTEGRATION_CATALOGUE.csv`, `API_REGISTER.csv` | UPPER_SNAKE | append | integration metadata | links to APIs, modules |
| **15-datasets** | Structured datasets | `DS-NNNN_<slug>/` | DS-prefixed | dated snapshots | dataset datasheet | evidence for findings |
| **16-images** | Photos, screenshots | `IMG-NNNN_<slug>.<ext>` | IMG-prefixed | never overwrite | caption + SRC link | evidence attachments |
| **17-maps** | Spatial / GIS map files | `MAP-NNNN_<slug>.<ext>` | MAP-prefixed | dated | spatial metadata | supports GIS layers |
| **18-videos** | Video evidence | `VID-NNNN_<slug>.<ext>` | VID-prefixed | never overwrite | caption + SRC link | evidence attachments |
| **19-templates** | Template library (pointer) | pointer README | fixed | git history | n/a | used by all authoring folders |
| **20-activity-logs** | Activity records (pointer) | pointer README | fixed | append-only | activity metadata | logs every change to the repo |
| **21-quality-assurance** | QA gate logs + dashboard snapshots | `QA_GATE_LOG.csv`, dashboard exports | UPPER_SNAKE / dated | append | gate metadata | reads all registers; enforces MREP §7 |
| **22-archives** | Superseded / retired artifacts | moved files | keep original name + `_archived_YYYYMMDD` | frozen | original + SUPERSEDED_BY | historical trace only |

## 4. Mapping from the initial MREP §6 scaffold

The ACT-002 scaffold used 18 flat categories; they are preserved within this richer hierarchy:

| MREP §6 category | New location |
|------------------|--------------|
| Research Reports | `01-research` |
| Raw Evidence | `02-evidence` + `03-sources` |
| Interview Notes | `04-interviews` |
| Survey Data | `05-surveys` |
| Process Maps | `13-product` / `06`,`07` workflow files (`WF-`) |
| Regulations | `08-regulations` |
| Standards | `08-regulations` (standards subset) |
| Data Models | `10-requirements` (`DATA_MODEL.md`) |
| API Documentation | `14-integrations` (`API_REGISTER.csv`) |
| Feature Catalogues | `13-product` |
| Competitor Profiles | `09-competitors` |
| AI Use Cases | `07-technology/ai` |
| GIS Layers | `07-technology/gis` + `17-maps` |
| IoT Device Profiles | `07-technology/iot` |
| Integration Specifications | `14-integrations` |
| Architecture Documents | `11-architecture` |
| Business Models | `12-business` |
| Product Requirements | `10-requirements` |
