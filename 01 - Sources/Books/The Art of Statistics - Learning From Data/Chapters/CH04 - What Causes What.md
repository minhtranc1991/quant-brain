---
artifact: chapter
source: "The Art of Statistics - Learning From Data"
source_id: the-art-of-statistics-learning-from-data
chapter_id: the-art-of-statistics-learning-from-data__ch04
chapter_number: 4
chapter_title: "What Causes What?"
extraction_status: extracted
---

# Chapter 04 — What Causes What?

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Art of Statistics - Learning From Data]]

## Summary

Distinguishes correlation from causation and lays out the randomized controlled trial (RCT) as the gold-standard mechanism for establishing causation (controls, random allocation, intention-to-treat, blinding, equal treatment, systematic review/meta-analysis). Covers confounding, Simpson's paradox, reverse causation, and the Bradford Hill criteria for judging causation from observational data when randomization is impossible.

## Keywords

- [[C - Causal Inference]]

## Claims

### Claim 1

Claim ID: `the-art-of-statistics-learning-from-data__ch04-C001`

Fingerprint: `d8735c0d577b`

Text: A statistical association between two variables (correlation) does not by itself establish that one causes the other; in the statistical sense, X causes Y means that intervening to force X to occur changes the proportion of times Y occurs, and inferring this with confidence generally requires either a randomized controlled trial or, absent randomization, a structured argument from observational data (e.g. the Bradford Hill criteria: effect size, temporal proximity, dose-response, plausible mechanism, replication).

Type: `definition`

Section: `'Correlation Does Not Imply Causation'`

Target Node: [[C - Causal Inference]]

Decision: `NEW`

### Claim 2

Claim ID: `the-art-of-statistics-learning-from-data__ch04-C002`

Fingerprint: `2c33043c7728`

Text: A properly designed randomized controlled trial requires: a control group, random allocation of treatment, analysis by intention-to-treat (counting participants in the group to which they were randomized regardless of actual compliance), blinding of participants and assessors where possible, equal treatment of both groups outside the intervention itself, complete follow-up, and replication across multiple independent studies (systematic review/meta-analysis) before a causal claim is considered robust.

Type: `framework`

Section: `Do statins reduce heart attacks and strokes?`

Target Node: [[C - Causal Inference]]

Decision: `NEW`

### Claim 3

Claim ID: `the-art-of-statistics-learning-from-data__ch04-C003`

Fingerprint: `d5fc5ea272d4`

Text: Confounding — a third variable influencing both the apparent cause and effect — can produce spurious correlations (e.g. ice cream sales and drownings both driven by warm weather) or, when adjusted for incorrectly, produce Simpson's paradox, in which an association reverses direction once a confounding factor is taken into account (e.g. Cambridge admissions being higher for men overall in 1996 despite being higher for women in every individual subject, because women disproportionately applied to more competitive subjects).

Type: `definition`

Section: `What Can We Do When We Observe an Association?`

Target Node: [[C - Causal Inference]]

Decision: `NEW`

## Notes

- **NEW_NODE:** All three claims ground the new Concept [[C - Causal Inference]].

## Completeness

- Claims extracted: 3
- Claims rejected: several illustrative case studies (brain tumours, Waitrose house prices, old men's ears) used only as supporting examples within the synthesized note.
- Claim density: high.
