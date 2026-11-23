# Matching contract

Agree on entity granularity, safe identifiers, weak signals, conflict fields, and candidate dispositions before comparing records. Keep the contract with the run so later reviewers know what counted as a match.

## Candidate evidence

- Strong signals may include a stable official identifier, or an independently supported legal identity combined with a specific matching location or other entity-level evidence.
- Weak signals include a shared display name, broad organization domain, parent brand, address, category, or geographic area. Use these to find candidates, not to assert equivalence.
- Multiple plausible records remain ambiguous. Preserve them all for review; do not choose the first result.
- Material differences in status, ownership, location, identity, or authorization create a conflict requiring evidence review.

Choose normalization rules narrowly and record them. Preserve source strings and IDs; normalized keys are derived comparison aids only. Avoid matching on generated identifiers from unrelated systems.

## Required ledger fields

Include the research record ID, candidate catalog record ID(s), classification, candidate count, matching signals, conflict fields, confidence, review status, source revision/hash for both sides, evidence references, and reviewer notes. Keep `PENDING` until a human reviewer accepts or rejects the proposed relationship.

## Interpretation limits

No match in a supplied snapshot does not prove the researched entity is real, current, complete, or eligible for publication. No researched counterpart does not establish closure or invalidity of a catalog record. A script can normalize keys and count candidates; it cannot verify identity, rights, source freshness, or authorization.
