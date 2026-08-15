---
artifact: chapter
source: "The Art of Statistics - Learning From Data"
source_id: the-art-of-statistics-learning-from-data
chapter_id: the-art-of-statistics-learning-from-data__ch07
chapter_number: 7
chapter_title: "How Sure Can We Be About What Is Going On? Estimates and Intervals"
extraction_status: extracted
---

# Chapter 07 — How Sure Can We Be About What Is Going On? Estimates and Intervals

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Art of Statistics - Learning From Data]]

## Summary

Introduces the distinction between a sample statistic and a population parameter, and develops bootstrapping (resampling the observed data with replacement) as a computation-based, assumption-light method for estimating the sampling distribution of a statistic and constructing uncertainty intervals ('margins of error'), applied both to a simple mean and to a regression coefficient (Galton's height data).

## Keywords

- [[M - Bootstrapping]]

## Claims

### Claim 1

Claim ID: `the-art-of-statistics-learning-from-data__ch07-C001`

Fingerprint: `9532a9f8296b`

Text: Bootstrapping estimates the sampling distribution (and hence the uncertainty) of a statistic by repeatedly resampling the observed data with replacement (the same sample size, drawn from itself) and recalculating the statistic on each resample; this requires no assumption about the mathematical shape of the underlying population distribution, and the bootstrap distribution of a statistic tends toward a symmetric, near-normal shape and narrows as the original sample size increases — an empirical, computational preview of the Central Limit Theorem.

Type: `mechanism`

Section: `Numbers of Sexual Partners`

Target Node: [[M - Bootstrapping]]

Decision: `NEW`

## Notes

- **NEW_NODE:** Grounds the new Model [[M - Bootstrapping]].

## Completeness

- Claims extracted: 1
- Claims rejected: worked numerical walk-throughs treated as the Minimal Example inside the new node rather than separate claims.
- Claim density: normal (a single, unifying idea; the rest of the chapter elaborates via worked examples).
