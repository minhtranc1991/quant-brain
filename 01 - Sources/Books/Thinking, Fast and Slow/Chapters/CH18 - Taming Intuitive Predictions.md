---
artifact: chapter
source: "Thinking, Fast and Slow"
source_id: thinking-fast-and-slow
chapter_id: thinking-fast-and-slow__ch18
chapter_number: 18
chapter_title: "Taming Intuitive Predictions"
extraction_status: extracted
---

# Chapter 18 — Taming Intuitive Predictions

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[Thinking, Fast and Slow]]

## Summary

Describes a correction procedure for intuitive predictions: start from the baseline/average outcome, estimate the intuitive prediction, estimate the correlation between the predictive evidence and the outcome, and move only that fraction of the distance from the baseline toward the intuitive prediction — formally 'regressing' the intuitive forecast itself to correct for its own overconfidence.

## Keywords

- [[C - Regression to the Mean]]

## Claims

### Claim 1

Claim ID: `thinking-fast-and-slow__ch18-C001`

Fingerprint: `c16c271614fe`

Text: Because intuitive predictions themselves generally fail to account for regression to the mean (they tend to be as extreme as the evidence they're based on, rather than tempered by how weak the evidence's predictive correlation actually is), a systematic correction procedure exists: estimate the correlation between the evidence and the outcome, then adjust the extreme intuitive prediction only that fraction of the way from the population baseline — an explicit, formulaic discipline for de-biasing forecasts that would otherwise be overconfidently extreme.

Type: `recommendation`

Section: `Taming Intuitive Predictions`

Target Node: [[C - Regression to the Mean]]

Decision: `EXISTING`

## Notes

- **[[ENRICH — same target as Ch17]]:** Adds a practical correction procedure to [[C - Regression to the Mean]]'s 'When it matters' section, complementing the diagnostic content from Ch17 with an actionable de-biasing technique directly relevant to forecast construction.

## Completeness

- Claims extracted: 1
- Claims rejected: 0
- Claim density: normal.
