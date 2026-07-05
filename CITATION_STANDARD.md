# AgriMine Nexus — Citation & Evidence-Traceability Standard

> **Status:** Mandatory. This standard is a binding addendum to the [ROM](ROM_Internalisation.md) and [MREP](MREP_Internalisation.md). It applies to **every** research document, work-package output, activity record, and final deliverable produced for AgriMine Nexus.
>
> **Effective:** 2026-07-05

---

## 1. The two hard rules

**Rule A — Every factual claim must carry an inline citation** containing, at minimum, all four of:

1. **Source organization** — the authoring body (e.g., Zambia Statistics Agency, World Bank, Bank of Zambia).
2. **Publication date** — when the source was published/last updated (`YYYY-MM-DD`, or `YYYY` if only the year is known).
3. **Confidence level** — the researcher's confidence in the claim, `0–100`, informed by source tier and corroboration (see ROM §12 Evidence Scoring).
4. **Retrieval date** — the date the source was accessed (`YYYY-MM-DD`).

**Rule B — Every recommendation must explicitly trace back to the evidence that supports it.** A recommendation with no traceable evidence chain is not permitted and must be reclassified as an *assumption* or *open question*.

A "factual claim" is any statement presented as true about the world (statistics, regulations, market facts, technical capabilities, competitor features, prices, dates, etc.). Definitions, restatements of these governance documents, and clearly-labelled assumptions are exempt from Rule A but assumptions must be labelled `[ASSUMPTION]`.

---

## 2. Inline citation format

Place the citation immediately after the claim, in parentheses:

```
<factual claim> [SRC-NN] (Source Organization, pub. YYYY-MM-DD; confidence NN/100; retrieved YYYY-MM-DD).
```

- `SRC-NN` is a short evidence ID that also appears in the document's **References / Evidence table**, giving the full citation, URL/locator, and source tier (ROM §2).
- Where several sources support one claim, list all IDs: `[SRC-03, SRC-07]`.

**Example:**

> Zambia's mobile-cellular subscriptions reached 21.4 million [SRC-04] (Zambia ICT Authority — ZICTA, pub. 2025-03-31; confidence 88/100; retrieved 2026-07-05).

---

## 3. Evidence table (required in every document)

Every document that makes factual claims must include an evidence table. It extends ROM §12 with the four mandatory fields from Rule A:

| Evidence ID | Source organization | Title / locator | Source tier (1–4) | Publication date | Retrieval date | Confidence (0–100) | Verification status | Contradicts |
|-------------|--------------------|-----------------|-------------------|------------------|----------------|--------------------|---------------------|-------------|
| SRC-01 | | | | | | | | |

---

## 4. Recommendation traceability format

Every recommendation gets an ID and an explicit evidence chain:

```
REC-NN: <recommendation>
  ├─ Supported by findings: F-xx, F-yy
  └─ Evidence: [SRC-aa, SRC-bb]  (net confidence NN/100)
```

Findings (`F-xx`) are themselves backed by citations, so the chain is **Recommendation → Finding(s) → Evidence(s) → Source(s)**. If any link is missing, the recommendation is downgraded to `[ASSUMPTION]` or `[OPEN QUESTION]`.

---

## 5. Confidence-level guidance

| Confidence | Meaning |
|-----------|---------|
| 90–100 | Multiple Tier-1/Tier-2 sources agree; current; directly relevant to Zambia. |
| 70–89 | Strong single authoritative source, or several corroborating lower-tier sources. |
| 50–69 | Plausible but limited/partly dated/indirect evidence; corroboration pending. |
| < 50 | Weak, single low-tier, contested, or outdated; treat as tentative and flag. |

Confidence must be reduced when evidence is outdated, geographically mismatched, or contradicted (ROM §3, Phase 3 Validation).

---

## 6. QA-gate enforcement

This standard is checked at MREP QA **Gate 2 (Source validation)**, **Gate 3 (Evidence quality review)**, and **Gate 4 (Cross-reference verification)**. A work package cannot pass these gates if any factual claim lacks a compliant inline citation or any recommendation lacks a traceable evidence chain.
