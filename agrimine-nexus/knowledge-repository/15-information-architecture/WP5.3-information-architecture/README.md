# WP5.3 — Enterprise Information & Data Architecture (ACT-020)

The technology-neutral **business information model** underpinning all later technical design. **No** databases, SQL, Firestore/PostgreSQL, APIs, GraphQL/REST, cloud, UI, classes, DTOs, or implementation. Every object traces to evidence.

## Files
| File | Contents |
|------|----------|
| `01_ENTERPRISE_INFORMATION_CATALOGUE.csv` | 47 information objects (`INFO-001`–`INFO-047`) with full traceability + CIA/retention/scope (Output 1) |
| `02_MASTER_DATA_ENTITY_CATALOGUE.csv` | 32 business entities (`DENT-001`–`DENT-032`) (Output 2) |
| `03_ATTRIBUTE_CATALOGUE.csv` | 56 business attributes (`ATR-001`–`ATR-056`), no SQL types (Output 3) |
| `04_RELATIONSHIP_CATALOGUE.csv` | 38 business relationships (`IREL-001`–`IREL-038`) (Output 4) |
| `05_REFERENCE_DATA_REGISTER.csv` | 25 reference-data sets (`REF-001`–`REF-025`) (Output 8) |
| `06_MASTER_TRANSACTION_METADATA.md` | Master-data + transaction-data registers + business metadata (Outputs 9–11) |
| `07_LIFECYCLE_OWNERSHIP_CLASSIFICATION.md` | Lifecycle + ownership + classification registers (Outputs 5–7) |
| `08_QUALITY_GOVERNANCE_CROSSDOMAIN.md` | Quality + governance registers + cross-domain matrix + info gap register (Outputs 12–14) |
| `09_EXECUTIVE_SUMMARY.md` | Executive summary (Output 16) |

Activity record: `activity-log/2026-07-05_ACT-020_*` (Output 17).
KG (Output 15): `../../10-requirements/GRAPH_*.csv` (`F-0094`–`F-0096`; `E-0213`–`E-0220`).
Evidence: synthesis reuses `SRC-0001`–`SRC-0121` (no new sources).

## Totals
47 information objects · 32 entities · 56 attributes · 38 relationships · 25 reference-data sets · 8 information gaps.

## Quality rules honoured
Every information object references evidence, requirement, capability, workflow, stakeholder, and domain (no orphans); every entity has ≥1 relationship; every relationship carries evidence; no duplicate entities; business vocabulary only.

## Honest limitation
Statutory retention periods and reference-data source lists need regulator/GRZ confirmation (`GAP-IN-01/04`); attribute catalogue covers core entities, not exhaustively all (`GAP-IN-08`).
