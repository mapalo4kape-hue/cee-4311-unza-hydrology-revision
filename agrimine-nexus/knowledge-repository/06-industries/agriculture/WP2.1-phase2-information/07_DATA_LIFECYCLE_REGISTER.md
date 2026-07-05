---
id: WP2.1-P2-LIFE
title: Data Lifecycle Register — Zambian Agriculture (WP2.1 Phase 2)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research
work_package: WP2.1
industry: TAX-IND.1 (Agriculture)
topic: Data lifecycle
keywords: [lifecycle, retention, data-ownership, records]
summary: Lifecycle of key agricultural information — created, received, updated, stored, exchanged, reported, owned, modified, consumed, retained, and how recorded. Information intelligence only.
source: SRC-0045;SRC-0058;SRC-0061;SRC-0062
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 78
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [01_MASTER_DATA_CATALOGUE.md, 02_TRANSACTION_CATALOGUE.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Data Lifecycle Register — Zambian Agriculture

> For key information domains, the ACT-009 objective questions: **Created → Received → Updated → Stored → Exchanged → Reported → Owner → Who modifies → Consumes → Retention → How recorded.**

## 1. Farmer registry data
- **Created:** at registration (District Ag Office) · **Received:** MoA/ZIAMIS · **Updated:** annual review; continuous update recommended [SRC-0060] · **Stored:** ZIAMIS central DB · **Exchanged:** with agro-dealers, banks (deposits), insurers · **Reported:** beneficiary counts to MoA/PDU · **Owner:** MoA/ZIAMIS · **Modifies:** MoA officers · **Consumes:** MoA, agro-dealers, suppliers [SRC-0058] · **Retention:** persistent registry · **How recorded:** digital (ZIAMIS) + paper at intake.

## 2. FISP voucher / redemption (GIN)
- **Created:** deposit → voucher; redemption → GIN · **Received:** farmer (SMS), agro-dealer · **Updated:** on redemption · **Stored:** ZIAMIS + signed GIN · **Exchanged:** farmer↔dealer↔MoA↔bank · **Reported:** subsidy reconciliation · **Owner:** MoA/ZIAMIS · **Modifies:** SZI/MoA, dealer (redeem) · **Consumes:** MoA (payment to dealer), farmer · **Retention:** per season (reconciliation) · **How recorded:** digital + signed paper [SRC-0045].

## 3. Field / agronomic records (planting, scouting, applications)
- **Created:** during operations · **Received:** rarely beyond farmer · **Updated:** ad hoc · **Stored:** farm diary/memory · **Exchanged:** verbally with extension · **Reported:** seldom · **Owner:** Farmer · **Modifies:** Farmer · **Consumes:** Farmer, occasionally extension · **Retention:** not standardised · **How recorded:** paper/verbal (largely undigitised).

## 4. Harvest / yield data
- **Created:** at harvest / forecast · **Received:** ZamStats (survey), buyer · **Updated:** post-harvest survey · **Stored:** survey systems; farmer paper · **Exchanged:** with ZamStats/FRA/buyer · **Reported:** Crop Forecast, national statistics · **Owner:** Farmer (own) / ZamStats (aggregate) · **Modifies:** Farmer, ZamStats · **Consumes:** planners, FRA, buyers · **Retention:** statistical archive · **How recorded:** survey (partly digital) + paper [SRC-0056].

## 5. Warehouse receipt / stored-commodity data
- **Created:** at deposit (issue) · **Received:** depositor, financier · **Updated:** on transfer/release · **Stored:** WRS + Collateral Registry [SRC-0062] · **Exchanged:** depositor↔warehouse↔bank↔ZAMACE · **Reported:** to Warehouse Licensing Authority · **Owner:** Warehouse operator (issuer); title to holder · **Modifies:** operator (issue/cancel) · **Consumes:** farmer, bank, buyer · **Retention:** legal record (statutory) [SRC-0061] · **How recorded:** WRS (digital) + paper.

## 6. Sale / payment data
- **Created:** at sale · **Received:** farmer, buyer, bank · **Updated:** on payment · **Stored:** depot system / mobile-money / paper · **Exchanged:** farmer↔buyer↔bank · **Reported:** FRA purchase records · **Owner:** transacting parties · **Modifies:** buyer/bank · **Consumes:** farmer, buyer · **Retention:** transaction/programme period · **How recorded:** mobile money (digital) + paper [SRC-0052].

## 7. Contract / credit ledger (outgrower)
- **Created:** at contracting · **Received:** farmer, company · **Updated:** input issue & buyback deduction · **Stored:** company central registry · **Exchanged:** company↔distributor↔farmer · **Reported:** to company · **Owner:** Agribusiness · **Modifies:** company/distributor · **Consumes:** company, farmer · **Retention:** contract term · **How recorded:** company registry + paper [SRC-0055].

## 8. Weather / advisory data
- **Created:** ZMD/providers · **Received:** farmer, extension · **Updated:** daily/seasonal · **Stored:** provider systems; ZIAMIS early-warning · **Exchanged:** via SMS/radio · **Reported:** seasonal outlooks · **Owner:** ZMD/provider · **Modifies:** provider · **Consumes:** farmer, extension, insurer · **Retention:** provider archive · **How recorded:** SMS/digital [SRC-0059].

## Observation (not a recommendation)
Retention and modification rights are **only standardised** where a **legal or programme framework** exists (warehouse receipts; FISP/ZIAMIS). Field/agronomic and most transactional data have **no defined lifecycle** today — recorded as the key information-ecosystem gap.
