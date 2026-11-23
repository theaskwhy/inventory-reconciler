---
name: inventory-reconciler
description: Compare a frozen, independently reviewed dataset with a separate read-only canonical catalog. Use to produce candidate matches, conflicts, likely duplicates, and unmatched coverage leads for human review without changing source records.
---

# Inventory Reconciler

Compare two deliberately separate datasets after the research copy has been frozen and independently reviewed. Produce a review-only candidate ledger. Never write into either source, merge records, publish findings as accepted facts, or authorize downstream updates.

## Entry conditions

Require actual row-level data for both sources, source/version metadata, a verified frozen checksum or equivalent revision for each, an independent review result for the researched source, and explicit authorization to compare those specific versions. Confirm rights and permitted use for both datasets. If a prerequisite is missing, report `HOLD` or `NOT_RUN` and identify what is unavailable. Do not use the canonical catalog as a substitute for independent research.

## Prepare a safe comparison

Capture source identifiers, revisions or dates, actual row counts, hashes where available, and verification state. Work on copies or read-only snapshots. Understand the entity grain and map schemas in a separate derived view while preserving original IDs, values, and provenance. Keep parent entities, legal records, branches, sites, products, and other entity types distinct when their identities differ.

Use [references/matching-contract.md](references/matching-contract.md) to set comparison keys and classifications before reviewing candidates. Prefer exact, well-supported identifiers and combinations of independent evidence. A shared name, address, domain, category, or parent brand alone may be only a lead. Never auto-merge fuzzy or ambiguous records.

## Classify candidates

Assign one disposition per researched record:

- `MATCHED`: one strong candidate with corroborating identity evidence; still pending human acceptance.
- `NEW_CANDIDATE`: no supported counterpart in the supplied catalog snapshot; not proof that the record is current or eligible for use.
- `CONFLICTING`: a plausible counterpart has material differences that need source review.
- `DUPLICATE_CANDIDATE`: multiple plausible counterparts or likely repeated records need human resolution.
- `REVIEW_REQUIRED`: evidence is partial, ambiguous, stale, or schema mapping is incomplete.

Record candidate count, match signals, confidence, original IDs, source revisions, conflict fields, evidence, and `review_status=PENDING`. An unmatched catalog record is only a coverage-review lead; absence from the research source does not prove it is closed or invalid. Keep original and proposed values side by side.

## Verify and report

Independently check material or high-risk disagreements against suitable primary sources. Record exact evidence and dates; mark unavailable checks `NOT_RUN`. Recompute all reported totals from input rows. Produce a candidate ledger, run manifest, concise summary, unresolved duplicates/conflicts, and a non-destructive reviewer handoff. Clearly label tool output as mechanical candidate generation, not proof of real-world identity.

All candidates remain pending. Do not create merge commands, destructive updates, production imports, or accepted/published states. Downstream use requires separate factual review, rights review, and explicit owner acceptance under the project's controls.
