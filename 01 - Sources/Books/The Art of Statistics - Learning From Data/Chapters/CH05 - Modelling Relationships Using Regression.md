---
artifact: chapter
source: "The Art of Statistics - Learning From Data"
source_id: the-art-of-statistics-learning-from-data
chapter_id: the-art-of-statistics-learning-from-data__ch05
chapter_number: 5
chapter_title: "Modelling Relationships Using Regression"
extraction_status: extracted
---

# Chapter 05 — Modelling Relationships Using Regression

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Art of Statistics - Learning From Data]]

## Summary

Introduces the statistical model as 'observation = deterministic model + residual error', develops least-squares regression via Galton's parent/offspring height data, and identifies 'regression to the mean' (originally Galton's 'regression to mediocrity') as a distinct statistical phenomenon that is frequently misattributed to a causal intervention (speed cameras, sports team performance, the 'Sports Illustrated curse', clinical trial placebo effects). Extends to multiple regression (adjustment for confounders) and logistic regression for proportions, and closes with George Box's 'all models are wrong, some are useful' and a warning about over-trusting complex financial models (2007-2008 crisis).

## Keywords

- [[M - Regression Analysis]]
- [[C - Regression to the Mean]]

## Claims

### Claim 1

Claim ID: `the-art-of-statistics-learning-from-data__ch05-C001`

Fingerprint: `9e387703391a`

Text: A statistical model decomposes an observation into a deterministic component (a mathematical formula, e.g. a fitted regression line) plus residual error (the unexplained, unavoidable variability); least-squares regression fits the deterministic line that minimizes the sum of squared residuals, and multiple regression extends this to adjust an estimated relationship for the effect of additional explanatory variables (confounders).

Type: `definition`

Section: `Regression Lines Are Models`

Target Node: [[M - Regression Analysis]]

Decision: `NEW`

### Claim 2

Claim ID: `the-art-of-statistics-learning-from-data__ch05-C002`

Fingerprint: `0943c1737244`

Text: Regression to the mean is the tendency for an unusually extreme observation (in either direction) to be followed by a less extreme one, because part of what made the original observation extreme was chance that will not systematically repeat; this is frequently misattributed to a real causal intervention — e.g. speed cameras installed at accident 'black spots' get credit for an accident-rate decline that randomized studies show is roughly two-thirds attributable to regression to the mean alone, and the same mechanism explains apparent placebo effects in clinical trials and reversals in sports-team or fund-manager performance rankings.

Type: `mechanism`

Section: `Do speed cameras reduce accidents?`

Target Node: [[C - Regression to the Mean]]

Decision: `NEW`

### Claim 3

Claim ID: `the-art-of-statistics-learning-from-data__ch05-C003`

Fingerprint: `81a919dd6c80`

Text: George Box's aphorism 'all models are wrong, but some are useful' captures a durable modelling discipline: a statistical model is a simplified map of reality, not the territory itself, and the 2007-2008 financial crisis is attributed partly to senior decision-makers placing excessive trust in complex mortgage-risk models whose correlation assumptions (moderate, largely independent mortgage failures) broke down catastrophically once conditions changed and failures became highly correlated.

Type: `limitation`

Section: `Beyond Basic Regression Modelling`

Target Node: [[M - Regression Analysis]]

Decision: `ENRICH`

## Notes

- **NEW_NODE:** Claims 1-2 ground new nodes [[M - Regression Analysis]] (Model) and [[C - Regression to the Mean]] (Concept).
- **ENRICH:** Claim 3 is folded into [[M - Regression Analysis]]'s Limitations/Pitfalls section rather than a separate node — it is a caution about model risk, not a distinct mechanism.

## Completeness

- Claims extracted: 3
- Claims rejected: logistic-regression mechanics treated as a Related Model mention inside [[M - Regression Analysis]] rather than a separate node (avoiding over-fragmentation).
- Claim density: high.
