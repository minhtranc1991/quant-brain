---
artifact: chapter
source: "The Art of Statistics - Learning From Data"
source_id: the-art-of-statistics-learning-from-data
chapter_id: the-art-of-statistics-learning-from-data__ch09
chapter_number: 9
chapter_title: "Putting Probability and Statistics Together"
extraction_status: extracted
---

# Chapter 09 — Putting Probability and Statistics Together

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Art of Statistics - Learning From Data]]

## Summary

Develops the sampling distribution of a statistic (e.g. a sample proportion), the Central Limit Theorem (the sampling distribution of a mean/statistic tends toward a normal distribution as sample size grows, largely regardless of the underlying population distribution's shape), and the formal construction and correct interpretation of a confidence interval, distinguishing this from the Bayesian interpretation and from the common misreading of a 95% confidence interval as '95% probability the true value is in this specific interval'.

## Keywords

- [[C - Central Limit Theorem]]

## Claims

### Claim 1

Claim ID: `the-art-of-statistics-learning-from-data__ch09-C001`

Fingerprint: `9230b8ad4e2c`

Text: The Central Limit Theorem states that the sampling distribution of a sample mean (or many other summary statistics) tends toward a normal distribution as sample size increases, regardless of the shape of the population distribution the individual observations are drawn from — this is why sample means from skewed underlying populations (e.g. income, sexual-partner counts) still produce symmetric, near-normal sampling distributions for large enough samples, and it underlies the standard construction of confidence intervals and hypothesis tests.

Type: `theoretical_claim`

Section: `The Central Limit Theorem`

Target Node: [[C - Central Limit Theorem]]

Decision: `NEW`

### Claim 2

Claim ID: `the-art-of-statistics-learning-from-data__ch09-C002`

Fingerprint: `68771c8861b6`

Text: A 95% confidence interval is the result of a procedure that, if repeated indefinitely under its assumptions, would contain the true population parameter in 95% of repetitions; it is a statement about the reliability of the procedure across repeated sampling, not a 95% probability that the true value lies in this specific, already-computed interval — that latter, more intuitive-sounding interpretation is a frequentist/Bayesian confusion and is only strictly valid under a Bayesian formulation of the same interval.

Type: `definition`

Section: `How Does This Theory Help Us Work Out the Accuracy of Our Estimates?`

Target Node: [[C - Central Limit Theorem]]

Decision: `ENRICH`

## Notes

- **NEW_NODE:** Grounds new Concept [[C - Central Limit Theorem]].
- **ENRICH:** Second claim (confidence-interval interpretation) folded into the same note as directly related content rather than a separate node, and cross-referenced from [[M - Null Hypothesis Significance Testing]].

## Completeness

- Claims extracted: 2
- Claims rejected: worked homicide-rate/unemployment examples treated as Minimal Examples inside the synthesized notes.
- Claim density: high (a genuinely foundational chapter).
