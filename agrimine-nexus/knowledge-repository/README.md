# AgriMine Nexus — Knowledge Repository

Version-controlled, structured knowledge base. The folder hierarchy is defined by the **[Repository Blueprint](../research-engine/02_REPOSITORY_BLUEPRINT.md)** (Research Engine, ACT-003), which specifies each folder's Purpose, Contents, Naming Convention, Versioning Rules, Metadata Requirements, and Relationships. Every document links to its supporting evidence and complies with the [Citation & Evidence-Traceability Standard](../CITATION_STANDARD.md).

## Hierarchy

| Folder | Purpose |
|--------|---------|
| `00-governance/` | Pointers to ROM/MREP/Citation Standard + `ID_REGISTRY.md` |
| `01-research/` | Completed research reports |
| `02-evidence/` | Master **Evidence Register** (`EVIDENCE_REGISTER.csv`) |
| `03-sources/` | Stored primary source files |
| `04-interviews/` | Interview records |
| `05-surveys/` | Survey instruments + responses |
| `06-industries/` | agriculture · mining · construction · environmental · logistics |
| `07-technology/` | ai · gis · iot · drones · cloud-architecture |
| `08-regulations/` | Acts, regulations, licences, standards |
| `09-competitors/` | Competitor profiles + comparison |
| `10-requirements/` | **Requirement Register (RTM)**, graph nodes/edges, data model |
| `11-architecture/` | Enterprise architecture documents |
| `12-business/` | Business model, pricing, GTM |
| `13-product/` | Feature catalogues, UI screens, reports |
| `14-integrations/` | Integration catalogue + API register |
| `15-datasets/` · `16-images/` · `17-maps/` · `18-videos/` | Raw data & media evidence |
| `19-templates/` | Pointer → `../templates/` |
| `20-activity-logs/` | Pointer → `../activity-log/` |
| `21-quality-assurance/` | QA gate log + dashboard snapshots |
| `22-archives/` | Superseded artifacts |

## Progress

Work-package and QA-gate status: [`WORK_PACKAGE_TRACKER.md`](WORK_PACKAGE_TRACKER.md).

## How to add content

1. Copy the right template from [`../templates/`](../templates/) into the correct folder.
2. Name it per the Blueprint convention; fill mandatory metadata (D5).
3. Register every source in `02-evidence/EVIDENCE_REGISTER.csv`; cite every claim.
4. Link requirements up to evidence and down to implementation (D6).
5. Log the change as an activity record and update the tracker; commit and push.
