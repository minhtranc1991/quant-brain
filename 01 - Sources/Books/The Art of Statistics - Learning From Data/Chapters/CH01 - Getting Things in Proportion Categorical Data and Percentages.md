---
artifact: chapter
source: "The Art of Statistics - Learning From Data"
source_id: the-art-of-statistics-learning-from-data
chapter_id: the-art-of-statistics-learning-from-data__ch01
chapter_number: 1
chapter_title: "Getting Things in Proportion: Categorical Data and Percentages"
extraction_status: extracted
---

# Chapter 01 — Getting Things in Proportion: Categorical Data and Percentages

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Art of Statistics - Learning From Data]]

## Summary

Introduces binary/categorical data and the communication of proportions. Uses the Bristol heart-surgery inquiry and the bacon-sandwich cancer-risk story to show how the same underlying data can be framed as relative risk, absolute risk, odds, or expected frequency, each producing a different emotional and interpretive impact — culminating in a documented case where an odds ratio of 1.18 was misreported by the press as an '18-20% increased risk', conflating relative risk with an odds ratio computed on a much higher base rate.

## Keywords

- [[C - Rare Event Risk (Fat-Tail Mispricing)]]

## Claims

### Claim 1

Claim ID: `the-art-of-statistics-learning-from-data__ch01-C001`

Fingerprint: `749557ef685f`

Text: Relative risk (e.g. an '18% increased risk') tends to convey an exaggerated impression of importance compared to absolute risk (e.g. a rise from 6 to 7 cases per 100), and communicating absolute risk or expected frequencies (e.g. 'out of 100 people...') produces more accurate audience understanding of the same underlying data.

Type: `empirical_claim`

Section: `Comparing a Pair of Proportions`

Target Node: N/A

Decision: `REVIEW`

### Claim 2

Claim ID: `the-art-of-statistics-learning-from-data__ch01-C002`

Fingerprint: `9fea3b21ad67`

Text: Odds ratios are numerically close to relative risk only when the underlying event is rare; for common events (e.g. baseline risk above roughly 20%) an odds ratio diverges substantially from the relative risk, and using an odds ratio from a scientific study as if it were a relative risk in general communication (as a 2013 statins study's press coverage did) is a documented, serious form of statistical misrepresentation.

Type: `definition`

Section: `Comparing a Pair of Proportions`

Target Node: N/A

Decision: `REVIEW`

## Notes

- **REVIEW:** Both claims are general statistical-communication principles rather than a durable, quant-specific mechanism distinct from existing vault content; no new node created for this chapter. Relevant to how risk figures (e.g. drawdown risk, tail-risk statistics) should be communicated, but this is treated as a cross-cutting methodological point rather than grounds for a new Concept.

## Completeness

- Claims extracted: 2
- Claims rejected: several (chart-type/dataviz-specific points, out of scope — largely superseded by [[Storytelling with Data]] already in the vault)
- Claim density: normal.
