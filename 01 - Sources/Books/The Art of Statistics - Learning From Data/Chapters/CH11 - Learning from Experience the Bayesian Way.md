---
artifact: chapter
source: "The Art of Statistics - Learning From Data"
source_id: the-art-of-statistics-learning-from-data
chapter_id: the-art-of-statistics-learning-from-data__ch11
chapter_number: 11
chapter_title: "Learning from Experience the Bayesian Way"
extraction_status: extracted
---

# Chapter 11 — Learning from Experience the Bayesian Way

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Art of Statistics - Learning From Data]]

## Summary

Introduces Bayesian inference: probability as an expression of epistemic uncertainty (personal ignorance about a fixed but unknown fact), Bayes' theorem (posterior odds = prior odds x likelihood ratio), and its application to forensic/legal reasoning (likelihood ratios, the Richard III skeleton identification), scientific hypothesis testing (Bayes factors), and modern election forecasting via multi-level regression and post-stratification (MRP), which pools sparse, non-random polling data across many small demographic/geographic cells using a shared (hierarchical) prior distribution.

## Keywords

- [[M - Bayesian Inference]]

## Claims

### Claim 1

Claim ID: `the-art-of-statistics-learning-from-data__ch11-C001`

Fingerprint: `73d00b6ecb43`

Text: Bayes' theorem provides a formal mechanism for updating beliefs in light of new evidence: posterior odds for a hypothesis equal the prior odds (belief before the evidence) multiplied by the likelihood ratio (how much more likely the evidence is under one hypothesis versus a competing one); independent pieces of evidence combine by multiplying their likelihood ratios, and Bayesian probability treats epistemic uncertainty (about fixed, unknown facts) using the same formal machinery as aleatory uncertainty (about future random events) — a stance that remains philosophically and practically contested against frequentist statistics, in an unresolved methodological dispute dating to the 1930s Fisher vs. Neyman-Pearson vs. Bayesian schools.

Type: `framework`

Section: `What Is the Bayesian Approach?`

Target Node: [[M - Bayesian Inference]]

Decision: `NEW`

### Claim 2

Claim ID: `the-art-of-statistics-learning-from-data__ch11-C002`

Fingerprint: `cec84ed48ff8`

Text: Hierarchical (multi-level) Bayesian modelling allows sparse or non-random data to be pooled across many small subgroups by assuming their underlying parameters are drawn from a shared prior distribution, producing 'shrinkage' of noisy individual-group estimates toward a common mean; multi-level regression and post-stratification (MRP) applies this to election forecasting from non-representative online panels and correctly predicted the outcome in 50 of 51 US states in the 2016 election and the 2017 UK hung-parliament result that traditional polling methods missed.

Type: `empirical_claim`

Section: `How can we better analyse pre-election polls?`

Target Node: [[M - Bayesian Inference]]

Decision: `ENRICH`

## Notes

- **NEW_NODE:** Grounds the new Model [[M - Bayesian Inference]] (claim 1 = core mechanism, claim 2 folded into the same note's Estimation/When-it-matters sections rather than a separate node).

## Completeness

- Claims extracted: 2
- Claims rejected: the three-coin/doping/billiard-table worked examples treated as the Minimal Example inside [[M - Bayesian Inference]].
- Claim density: high.
