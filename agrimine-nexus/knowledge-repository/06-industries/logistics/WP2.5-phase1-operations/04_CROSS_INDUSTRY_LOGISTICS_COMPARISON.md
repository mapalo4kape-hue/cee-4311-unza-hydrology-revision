---
id: WP2.5-P1-XIND
title: Cross-Industry Logistics Comparison — Zambia (WP2.5)
author: AgriMine Nexus Research Consultant (Cursor AI)
research_program: Stage 2 — Industry Research (logistics layer)
work_package: WP2.5
industry: cross-industry
topic: Cross-industry logistics comparison
keywords: [logistics, cross-industry, shared, corridors, warehouse, fleet]
summary: Output 13. Compares logistics across Agriculture, Mining, Construction & Environmental — shared vs industry-specific logistics. Evidence-first; no software design.
source: SRC-0041;SRC-0090;SRC-0093
publication_date: 2026-07-05
retrieval_date: 2026-07-05
confidence: 80
evidence_level: 2
status: in-review
version: v01
reviewer: pending
approval_status: pending
related_documents: [../../CROSS_INDUSTRY_COMPARATIVE_ANALYSIS.md, 02_LOGISTICS_WORKFLOW_AND_SUPPLY_CHAIN.md]
related_requirements: []
related_entities: []
related_apis: []
related_modules: []
related_workflows: []
---

# Cross-Industry Logistics Comparison — Zambia

> How logistics is shared vs industry-specific across the four researched sectors. Logistics is the **connective operational layer** identified in the ACT-010 comparative analysis.

## 1. Shared logistics (common across all four industries)
| Shared element | Evidence |
|----------------|----------|
| Same **corridor/road/rail/border** network (Dar/North-South/Beira/Nacala/Walvis Bay/Lobito) | [SRC-0041][SRC-0087] |
| Same **customs/cross-border** process (ASYCUDA, clearing agents, TIP, COMESA/SADC/AfCFTA) | [SRC-0090][SRC-0092] |
| Same **fleet operations** (dispatch, GPS, fuel, maintenance, RTSA compliance) | [SRC-0093] |
| Same **warehouse/inventory** primitives (receive → store → dispatch) | [SRC-0051] |
| Same **procurement** (PO → GRN → 3-way match → payment) & **fuel logistics** | [SRC-0090] |
| Same **documents** (waybill, GRN, SAD/CE20, weighbridge ticket, permits) | [SRC-0090] |
| Same **pain points** (border delays, feeder roads, fuel, paper/duplication, visibility) | [SRC-0092][SRC-0057] |
| Same **stakeholders** (trucking firms, C&F agents/ZAFFA, ZRA, RDA, RTSA, warehouses) | [SRC-0093] |

## 2. Industry-specific logistics
| Industry | Distinctive logistics | Evidence |
|----------|-----------------------|----------|
| **Agriculture** | seasonal input distribution (FISP), harvest aggregation, cold chain, FRA depots, warehouse-receipt logistics, fertilizer (NCZ) distribution | [SRC-0093][SRC-0051] |
| **Mining** | bulk ore/concentrate haulage (road+rail), explosives & hazmat supply, heavy-equipment/abnormal-load transport, mineral export via corridors/rail, high fuel volumes | [SRC-0087] (rail); WP2.2 |
| **Construction** | material call-offs to site (cement/steel/aggregate), quarry logistics, equipment mobilisation & crane logistics, temporary site storage | WP2.3; [SRC-0093] |
| **Environmental** | waste & hazardous-waste transport, lab-sample chain-of-custody, monitoring-equipment deployment, recycling/landfill/medical-waste logistics | WP2.4 |

## 3. Logistics as the connective layer (mapping to industry workflows)
- Agriculture: WF-L01/L02/L04/L05/L06/L07 ↔ WF-007/008/024/026/029/031.
- Mining: WF-L03/L08/L09/L10/L16 ↔ WF-M04/M06/M07/M13.
- Construction: WF-L10/L21/L22/L16 ↔ WF-C07/C08/C09.
- Environmental: WF-L23/L24/L25/L26 ↔ WF-E03/E09/E10.

## 4. Observations (operational, not design)
- The **same logistics backbone** carries every industry's goods, people, documents, and information — confirming logistics as the unifying operational layer across the productive-industry model.
- **Convergent frictions** (border delays, feeder roads, fuel, paper duplication, low visibility) recur regardless of industry, mirroring the ACT-010 cross-industry pain-point convergence.
- Industry-specific needs are **specialisations on the shared backbone** (seasonality/cold chain for agriculture; bulk & hazmat for mining; site call-offs for construction; chain-of-custody for environmental).

## Recorded uncertainties
Relative freight volumes by industry and modal split (road vs rail) require primary/operator data; recorded in the Gap Register.
