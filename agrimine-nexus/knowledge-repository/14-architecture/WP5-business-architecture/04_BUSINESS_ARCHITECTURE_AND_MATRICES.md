---
id: WP5-BIZARCH
title: Enterprise Business Architecture — Domains, Bounded Contexts & Matrices (WP5)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 5 — Enterprise Business Architecture
work_package: WP5
industry: cross-industry
topic: Business architecture and domain model (DDD)
keywords: [business-architecture, DDD, domains, bounded-context, business-events, business-objects, cross-domain]
summary: Outputs 1-12. Enterprise Business Architecture document, domain taxonomy, bounded context catalogue, interaction/dependency/cross-domain matrices, and domain risk/constraint registers. Business architecture only — no software/DB/API/cloud/UI design.
source: F-0053;F-0056;F-0060;F-0067;F-0077;F-0088;F-0090
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 70
evidence_level: 3
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_ENTERPRISE_DOMAIN_CATALOGUE.csv, 02_BUSINESS_OBJECT_CATALOGUE.csv, 03_BUSINESS_EVENT_CATALOGUE.csv]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Enterprise Business Architecture (Outputs 1–12)

> Domain-Driven Design at the **business** level. Every domain traces to capabilities (`CAP-`), requirements (`REQ-`), workflows (`WF-`), stakeholders (`STK-`), regulations (`REG-`) and findings (`F-`). This is **not** software/microservices/database/API/cloud/UI design. No implementation, deployment, or UML.

## Output 1 — Enterprise Business Architecture Document (narrative)
AgriMine Nexus is modelled as a **multi-domain enterprise** serving Zambia's agriculture, mining, construction, environmental, and logistics sectors on a shared enterprise foundation. The architecture separates **Core** value-creating industry domains from **Supporting** business domains (finance, procurement, HR, compliance, document, analytics, notifications, extension, geospatial) and **Generic** domains (identity, audit, configuration, monitoring, file, messaging, scheduling). Core domains own sector-specific operations and language; supporting/generic domains provide reusable business services consumed across cores. The design reflects three evidence-based realities: (1) **offline-first, mobile/USSD** operation is mandatory (`F-0078`); (2) **regulatory compliance** is a first-class concern spanning cores via a dedicated Compliance domain (`F-0073`); and (3) **cross-industry commons** (finance, identity, geospatial, notifications) are the largest reused surface (`F-0088`). All 24 domains satisfy the quality rule: each maps to >=1 capability, requirement, workflow, and stakeholder (and regulations where applicable) — see the domain catalogue.

## Output 3 — Domain Taxonomy
| Class | Domains |
|-------|---------|
| **Core** (6) | Agriculture Operations (DOM-AGRI) · Mining Operations (DOM-MINE) · Construction Operations (DOM-CONS) · Environmental Management (DOM-ENV) · Logistics Operations (DOM-LOG) · Commodity Trading & Marketplace (DOM-TRADE) |
| **Supporting** (11) | Finance & Payments (DOM-FIN) · Procurement (DOM-PROC) · Inventory & Asset (DOM-INV) · HR (DOM-HR) · CRM (DOM-CRM) · Compliance & Reporting (DOM-CMP) · Document Management (DOM-DOC) · Analytics & Reporting (DOM-ANALYTICS) · Notifications & Engagement (DOM-NOTIF) · Extension & Advisory (DOM-EXT) · Geospatial & Earth Observation (DOM-GEO) |
| **Generic** (7) | Identity & Access (DOM-IAM) · Audit & Traceability (DOM-AUDIT) · Configuration & Reference Data (DOM-CFG) · Monitoring (DOM-MON) · File & Content (DOM-FILE) · Messaging & Integration (DOM-MSG) · Scheduling (DOM-SCHED) |

## Output 4 — Bounded Context Catalogue
| Domain | Responsibilities (owns) | Inputs (upstream) | Outputs (downstream) | Shared concepts | Ubiquitous language (examples) |
|--------|-------------------------|-------------------|----------------------|-----------------|-------------------------------|
| DOM-AGRI | Farm/crop/livestock operations & records | identity; geospatial; weather | harvest/yield; produce for trade | Farm; Plot; Season | Plot, Season, Input, Scouting, Yield |
| DOM-MINE | Exploration→production; safety | geospatial; identity; procurement | production; env readings; reports | Site; Asset; Permit | Block, Grade, Haul cycle, Permit-to-work |
| DOM-CONS | Project delivery lifecycle | procurement; documents; HR | valuations; progress; assets | Project; Site; BOQ | WBS, BOQ, IPC, Snag, Variation |
| DOM-ENV | EIA; monitoring; ESG; compliance data | geospatial; lab samples | exceedances; compliance reports | Permit; Reading; Sample | EIA, ESMP, Exceedance, Rehabilitation |
| DOM-LOG | Transport/warehouse/dispatch | orders; inventory; geospatial | deliveries; POD; transit status | Order; Shipment; Vehicle | Consignment, Route, POD, Corridor |
| DOM-TRADE | Listing/matching/receipts | produce; finance | orders; receipts; market info | Order; WarehouseReceipt | Listing, Match, Receipt, Grade |
| DOM-FIN | Ledger; payments; mobile money | invoices; payroll; procurement | payments; statements | Invoice; Payment; Account | GL, AP/AR, Disbursement, MoMo |
| DOM-CMP | Compliance obligations & submissions | monitoring; production; finance | statutory reports; permits | Permit; Report; Incident | Obligation, Submission, Exceedance |
| DOM-IAM | Authentication/authorisation/tenancy | national ID (ext) | identities; access decisions | Person; Org; Account | Identity, Role, Tenant, Consent |
| DOM-GEO | Spatial data & earth observation | imagery (ext); field capture | maps; indices; boundaries | Plot; Site; Layer | Layer, CRS, NDVI, Boundary |
| DOM-NOTIF | Multichannel messaging | events; contacts | delivered messages | Person; Message | SMS, USSD, Push, Delivery report |
> Overlap avoidance: environmental monitoring is owned by **DOM-ENV** (mining consumes it); financial postings owned by **DOM-FIN** (all consume); identity owned by **DOM-IAM** (all consume); spatial owned by **DOM-GEO** (cores consume). No duplicated ownership.

## Output 5 — Domain Interaction Matrix (consumes ← / produces →)
| Domain | Consumes information from | Produces information for | Shared business objects |
|--------|---------------------------|--------------------------|-------------------------|
| DOM-AGRI | DOM-GEO; DOM-EXT; DOM-FIN; DOM-IAM | DOM-TRADE; DOM-LOG; DOM-ANALYTICS | Farm; Plot; Order |
| DOM-MINE | DOM-GEO; DOM-PROC; DOM-INV; DOM-IAM | DOM-ENV; DOM-CMP; DOM-ANALYTICS | Site; Asset; Permit; MinePlan |
| DOM-CONS | DOM-PROC; DOM-DOC; DOM-HR; DOM-INV | DOM-FIN; DOM-CMP; DOM-ANALYTICS | Project; BOQ; Asset |
| DOM-ENV | DOM-GEO; DOM-MINE | DOM-CMP; DOM-ANALYTICS | Permit; MonitoringReading; Sample |
| DOM-LOG | DOM-TRADE; DOM-INV; DOM-GEO | DOM-FIN; DOM-ANALYTICS; DOM-TRADE | Order; Shipment; Vehicle |
| DOM-TRADE | DOM-AGRI; DOM-FIN | DOM-LOG; DOM-FIN | Order; WarehouseReceipt |
| DOM-FIN | DOM-PROC; DOM-HR; DOM-TRADE; all | all cores; DOM-CMP | Invoice; Payment |
| DOM-CMP | DOM-ENV; DOM-MINE; DOM-FIN | regulators (ext); DOM-AUDIT | Permit; Report; Incident |
| DOM-IAM | DOM-CFG; national ID (ext) | ALL domains | Person; Org; Account |
| DOM-GEO | imagery (ext); field capture | DOM-AGRI; DOM-MINE; DOM-ENV; DOM-LOG | Plot; Site |
| DOM-NOTIF | business events; DOM-CRM | end users (ext) | Person; Message |

## Output 8 — Domain Dependency Matrix (depends on)
| Domain | Depends on |
|--------|-----------|
| All cores (AGRI/MINE/CONS/ENV/LOG/TRADE) | DOM-IAM; DOM-AUDIT; DOM-DOC; DOM-NOTIF; DOM-CFG; DOM-MSG |
| DOM-AGRI | DOM-GEO; DOM-EXT; DOM-FIN; DOM-TRADE |
| DOM-MINE | DOM-GEO; DOM-ENV; DOM-INV; DOM-PROC; DOM-CMP |
| DOM-CONS | DOM-PROC; DOM-INV; DOM-HR; DOM-DOC |
| DOM-ENV | DOM-GEO; DOM-CMP; DOM-ANALYTICS |
| DOM-LOG | DOM-INV; DOM-FIN; DOM-GEO; DOM-TRADE |
| DOM-TRADE | DOM-FIN; DOM-LOG; DOM-AGRI |
| DOM-FIN | DOM-IAM; DOM-AUDIT; DOM-MSG (payment integration) |
| DOM-CMP | DOM-AUDIT; DOM-ANALYTICS; DOM-MSG (regulator submission) |
| DOM-ANALYTICS | DOM-CFG; DOM-MON; DOM-GEO |
> **Foundational domains** (most-depended-on): DOM-IAM, DOM-AUDIT, DOM-FIN, DOM-GEO, DOM-NOTIF, DOM-MSG — consistent with the requirement dependency analysis (`F-0091`).

## Output 9 — Cross-Domain Capability Matrix (shared capabilities)
| Shared capability | Domains sharing |
|-------------------|-----------------|
| Asset/equipment management (CAP-053/134/080/106) | DOM-MINE; DOM-CONS; DOM-LOG; DOM-INV |
| Safety/HSE (CAP-057/085) | DOM-MINE; DOM-CONS; DOM-CMP |
| Monitoring (CAP-060/091/092) | DOM-MINE; DOM-ENV |
| Inventory/warehousing (CAP-015/113/054) | DOM-AGRI; DOM-LOG; DOM-INV; DOM-MINE |
| Payments/mobile money (CAP-124/125/039) | DOM-FIN; DOM-AGRI; DOM-TRADE |
| Geospatial (CAP-162/002) | DOM-GEO; DOM-AGRI; DOM-MINE; DOM-ENV; DOM-LOG |
| Identity/audit (CAP-153/156-159) | DOM-IAM; DOM-AUDIT; ALL |
| Notifications (CAP-149/169) | DOM-NOTIF; DOM-EXT; DOM-CRM; ALL |

## Output 10 — Cross-Domain Workflow Matrix (shared workflows)
| Shared workflow theme | Domains |
|-----------------------|---------|
| Compliance reporting (WF-035; WF-M11; WF-E14) | DOM-CMP; DOM-MINE; DOM-ENV; DOM-FIN |
| Financial transactions (WF-006; WF-032; WF-037) | DOM-FIN; DOM-AGRI; DOM-TRADE; all |
| Field data capture & sync (WF-033) | ALL cores; DOM-IAM |
| Procurement (WF-032; WF-M07; WF-C04) | DOM-PROC; DOM-MINE; DOM-CONS |
| Advisory/notifications (WF-038; WF-039) | DOM-EXT; DOM-NOTIF; DOM-AGRI |
| Spatial operations (WF-003; WF-M03; WF-E11) | DOM-GEO; DOM-AGRI; DOM-MINE; DOM-ENV |

## Cross-Domain Analysis (shared stakeholders / regulations / integrations / technologies)
- **Shared stakeholders:** finance functions (STK-029/060), regulators (STK-022/010/009), IT/admin (STK-070) recur across domains.
- **Shared regulations:** Data Protection Act REG-0024 (IAM/audit/doc/all); sector reporting REG-0009/0017 (CMP+cores); tax REG-0027/28 (FIN+HR).
- **Shared integrations:** mobile money INT-003/006 (FIN/AGRI/TRADE); comms INT-091/092/102 (NOTIF/EXT); identity INT-105/108/115 (IAM/all); spatial/EO INT-057/066 (GEO/cores); gov INT-030/035 (CMP).
- **Shared technologies:** offline-sync TECH-127/129; IAM TECH-136-139; GIS/RS TECH-047/060; BI TECH-123/124; mobile-money/USSD TECH-150 — the cross-cutting Zambia enablers.
