---
artifact: chapter
source: "The Art of Statistics - Learning From Data"
source_id: the-art-of-statistics-learning-from-data
chapter_id: the-art-of-statistics-learning-from-data__ch10
chapter_number: 10
chapter_title: "Answering Questions and Claiming Discoveries"
extraction_status: extracted
---

# Chapter 10 — Answering Questions and Claiming Discoveries

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Art of Statistics - Learning From Data]]

## Summary

Formalizes null hypothesis significance testing (NHST): null hypotheses, P-values, statistical significance thresholds (Fisher's P<0.05/0.01 convention), Neyman-Pearson Type I/Type II errors and statistical power, and worked examples (Arbuthnot's sex-ratio test, arm-crossing/chi-squared test, the Higgs boson discovery, the Shipman murder-detection sequential test). Documents the multiple-testing problem (illustrated by a dead salmon showing a 'statistically significant' brain response) and the American Statistical Association's six principles on correct P-value interpretation, including the common misreading of a P-value as the probability the null hypothesis is true, and the distinction between statistical and practical significance.

## Keywords

- [[M - Null Hypothesis Significance Testing]]
- [[C - P-Hacking]]

## Claims

### Claim 1

Claim ID: `the-art-of-statistics-learning-from-data__ch10-C001`

Fingerprint: `7767f9bb72c1`

Text: A P-value is the probability, assuming the null hypothesis (and all other modelling assumptions) is true, of observing a result at least as extreme as the one actually observed; it is a measure of the incompatibility between the data and the null hypothesis, not the probability that the null hypothesis itself is true, and a large (non-significant) P-value does not mean the null hypothesis has been proven — Ronald Fisher: 'the null hypothesis is never proved or established, but is possibly disproved'.

Type: `definition`

Section: `What Is a 'Hypothesis'?`

Target Node: [[M - Null Hypothesis Significance Testing]]

Decision: `NEW`

### Claim 2

Claim ID: `the-art-of-statistics-learning-from-data__ch10-C002`

Fingerprint: `26d909643702`

Text: Neyman-Pearson theory formalizes hypothesis testing as a decision problem with two error types: a Type I error (rejecting a true null hypothesis, size alpha, conventionally 0.05) and a Type II error (failing to reject a false null hypothesis, related to power = 1-beta, the probability of correctly detecting a true effect); required sample size for a study is derived by fixing both alpha and the desired power against a specified, practically important alternative hypothesis.

Type: `framework`

Section: `Neyman-Pearson Theory`

Target Node: [[M - Null Hypothesis Significance Testing]]

Decision: `NEW`

### Claim 3

Claim ID: `the-art-of-statistics-learning-from-data__ch10-C003`

Fingerprint: `cb354dc3b848`

Text: Running many significance tests and reporting only the most significant result (multiple testing) sharply inflates the false-positive rate beyond the nominal per-test threshold (e.g. ten tests of a truly useless intervention at P<0.05 each have roughly a 40% chance of producing at least one false 'significant' result), a problem demonstrated by an fMRI study finding 'statistically significant' brain activity in a dead salmon; standard corrections include the Bonferroni correction (dividing the significance threshold by the number of tests) and pre-registration/replication requirements, and the same inflation arises from undisclosed 'researcher degrees of freedom' (flexible, post-hoc analytic choices) even without literally running formally separate tests.

Type: `mechanism`

Section: `The Danger of Carrying Out Many Significance Tests`

Target Node: [[C - P-Hacking]]

Decision: `NEW`

## Notes

- **NEW_NODE:** Claims 1-2 ground the new Model [[M - Null Hypothesis Significance Testing]]; claim 3 grounds the new Concept [[C - P-Hacking]].

## Completeness

- Claims extracted: 3
- Claims rejected: worked examples (Arbuthnot, Higgs boson, Shipman) treated as Minimal Examples/context inside the synthesized notes rather than separate claims; statistical-vs-practical-significance point folded into [[M - Null Hypothesis Significance Testing]]'s Pitfalls.
- Claim density: high (a core chapter).
