---
artifact: chapter
source: "The Art of Statistics - Learning From Data"
source_id: the-art-of-statistics-learning-from-data
chapter_id: the-art-of-statistics-learning-from-data__ch13
chapter_number: 13
chapter_title: "How We Can Do Statistics Better"
extraction_status: extracted
---

# Chapter 13 — How We Can Do Statistics Better

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Art of Statistics - Learning From Data]]

## Summary

Prescribes remedies for the problems documented in Chapter 12: pre-registration of study protocols, distinguishing exploratory from confirmatory analysis, publication-bias detection (the 'P-curve' technique), and a ten-question checklist for assessing the trustworthiness of any statistical claim (rigor of the study, statistical uncertainty, appropriateness of the summary, reliability/bias of the source, spin, omissions, fit with other evidence, causal interpretation, relevance, and practical importance). Closes with a real-world case study of the 2017 UK election exit poll (built on the MRP methodology from Chapter 11) as an example of statistical science done well.

## Keywords

- [[C - P-Hacking]]
- [[M - Bayesian Inference]]

## Claims

### Claim 1

Claim ID: `the-art-of-statistics-learning-from-data__ch13-C001`

Fingerprint: `6cc3292d5a5a`

Text: Publication bias and selective reporting can be statistically detected via 'P-curve' analysis: if an intervention genuinely has no effect, P-values from studies testing it should scatter roughly uniformly across (0, 0.05) among the subset that happen to cross the significance threshold by chance, whereas a genuine effect produces P-values skewed toward smaller values; a cluster of P-values just below 0.05 is itself a specific, detectable signature of selective reporting or post-hoc analytic massaging.

Type: `mechanism`

Section: `Publication Bias`

Target Node: [[C - P-Hacking]]

Decision: `ENRICH`

## Notes

- **ENRICH:** Folded into [[C - P-Hacking]] as a detection technique complementing the mechanism already documented from Chapters 10 and 12.
- **REVIEW:** The ten-question trustworthiness checklist is valuable practitioner guidance but is a synthesis/checklist rather than a single atomic, durable claim suited to a Concept/Model node — not extracted as a separate node; noted here for completeness.

## Completeness

- Claims extracted: 1
- Claims rejected: ten-question checklist (methodological synthesis, not a discrete claim) and the 2017 exit-poll case study (treated as a Minimal Example inside [[M - Bayesian Inference]]).
- Claim density: normal.
