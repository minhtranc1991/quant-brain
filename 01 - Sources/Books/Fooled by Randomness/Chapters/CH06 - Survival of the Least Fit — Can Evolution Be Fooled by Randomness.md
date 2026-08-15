---
artifact: chapter
source: "Fooled by Randomness"
source_id: fooled-by-randomness
chapter_id: fooled-by-randomness__ch06
chapter_number: 6
chapter_title: "Survival of the Least Fit — Can Evolution Be Fooled by Randomness?"
extraction_status: extracted
---

# Chapter 06 — Survival of the Least Fit — Can Evolution Be Fooled by Randomness?

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[Fooled by Randomness]]

## Summary

Argues that a population of traders/funds observed today is a *survived* sample, not a random sample of all who started; mathematicians of probability call the property that very long sample paths come to resemble each other 'ergodicity' — over a sufficiently long horizon, a rare event that a strategy is exposed to becomes near-certain, so a surviving cohort's apparent skill is largely an artifact of the initial population's size and the horizon examined, not proof of individual skill.

## Keywords

- [[C - Ergodicity]]
- [[C - Survivorship Bias]]

## Claims

### Claim 1

Claim ID: `fooled-by-randomness__ch06-C001`

Fingerprint: `42c6b485b45f`

Text: Ergodicity means that, under certain conditions, very long sample paths come to resemble each other in their properties; extended to an infinite time horizon, an event a strategy is structurally exposed to will occur with certainty, so strategies that appear to have 'survived' a rare event merely have not yet been observed for long enough.

Type: `definition`

Section: `Chapter 6`

Target Node: [[C - Ergodicity]]

Decision: `NEW`

### Claim 2

Claim ID: `fooled-by-randomness__ch06-C002`

Fingerprint: `195fe04d0c0a`

Text: A cohort of traders/funds who show a run of good performance over a fixed observation window is best explained as a subset of the original population that avoided a rare, damaging event purely by chance (over-fitness to one lucky sample path), not as an unbiased demonstration of skill in the underlying population.

Type: `mechanism`

Section: `Chapter 6`

Target Node: [[C - Survivorship Bias]]

Decision: `EXISTING`

## Notes

- **NEW_NODE:** Ergodicity is a distinct, formal probability concept (long-run sample-path convergence / rare events becoming certain over time) not previously present in the vault, and it is the specific mechanism this book uses to explain survivorship-driven overconfidence.
- **ENRICH:** Adds a mechanism-level (ergodicity + cohort-size) explanation of survivorship bias to the existing [[C - Survivorship Bias]] note, complementing its existing empirical fund-attrition angle from [[A Random Walk Down Wall Street]].

## Completeness

- Claims extracted: 2
- Claims rejected: 0
- Claim density: normal.
