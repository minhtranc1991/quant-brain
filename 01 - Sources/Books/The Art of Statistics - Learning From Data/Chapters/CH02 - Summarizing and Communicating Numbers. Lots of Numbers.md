---
artifact: chapter
source: "The Art of Statistics - Learning From Data"
source_id: the-art-of-statistics-learning-from-data
chapter_id: the-art-of-statistics-learning-from-data__ch02
chapter_number: 2
chapter_title: "Summarizing and Communicating Numbers. Lots of Numbers"
extraction_status: extracted
---

# Chapter 02 — Summarizing and Communicating Numbers. Lots of Numbers

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Art of Statistics - Learning From Data]]

## Summary

Covers summary statistics (mean/median/mode, range/IQR/standard deviation), data distributions, and correlation (Pearson vs. Spearman). Demonstrates via a 915-person jelly-bean-guessing experiment that skewed distributions make the mean an unreliable summary and that robust measures (median, IQR) are preferable when a distribution has a long tail (e.g. income, sexual-partner counts, jelly-bean guesses).

## Keywords

- [[C - Random Walk Hypothesis]]

## Claims

### Claim 1

Claim ID: `the-art-of-statistics-learning-from-data__ch02-C001`

Fingerprint: `befdbb8040eb`

Text: For data distributions with a long right-hand tail (skewed distributions), the mean is disproportionately influenced by extreme values and can be a materially misleading summary statistic; the median and inter-quartile range are 'robust measures' that are far less sensitive to outliers and extreme values in such distributions.

Type: `definition`

Section: `Describing the Spread of a Data Distribution`

Target Node: N/A

Decision: `REVIEW`

### Claim 2

Claim ID: `the-art-of-statistics-learning-from-data__ch02-C002`

Fingerprint: `8d543bb2cadf`

Text: Pearson correlation measures closeness to a straight-line (linear) relationship, while Spearman's rank correlation measures closeness to any consistently increasing or decreasing (monotonic, not necessarily linear) relationship; the two can differ substantially on the same data (e.g. 0.59 vs. 0.85 in a child-heart-surgery volume/survival dataset), and a Pearson correlation near zero does not imply the absence of a relationship (per the 'Datasaurus' family of counter-examples).

Type: `definition`

Section: `Describing Relationships Between Variables`

Target Node: N/A

Decision: `REVIEW`

## Notes

- **REVIEW:** Robust-statistics and correlation-measure-choice points are useful methodological hygiene for quant work (e.g. return distributions are typically fat-tailed/skewed) but do not rise to a new, atomic, durable Concept distinct from statistical technique already implicit in existing vault Models (e.g. [[M - Modern Portfolio Theory]]'s use of correlation). No new node created for this chapter.

## Completeness

- Claims extracted: 2
- Claims rejected: dataviz-specific chart-choice guidance (chart types, infographics) — out of scope, overlaps [[Storytelling with Data]].
- Claim density: normal.
