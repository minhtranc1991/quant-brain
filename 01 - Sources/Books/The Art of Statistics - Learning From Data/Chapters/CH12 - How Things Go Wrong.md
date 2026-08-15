---
artifact: chapter
source: "The Art of Statistics - Learning From Data"
source_id: the-art-of-statistics-learning-from-data
chapter_id: the-art-of-statistics-learning-from-data__ch12
chapter_number: 12
chapter_title: "How Things Go Wrong"
extraction_status: extracted
---

# Chapter 12 — How Things Go Wrong

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Art of Statistics - Learning From Data]]

## Summary

Examines the reproducibility crisis in science (only 36% of 100 psychology-study replications reproduced statistically significant results), documents specific failure modes (spreadsheet errors, e.g. Reinhart-Rogoff; miscoded risk models, e.g. AXA Rosenberg's $242M fine; deliberate fraud), and formalizes 'questionable research practices' (QRPs) / 'researcher degrees of freedom' / 'the garden of forking paths' — undisclosed flexible analytic choices (when to stop collecting data, what to exclude, what to adjust for) that inflate false-positive rates even without formal multiple testing, illustrated by a deliberately absurd but 'statistically significant' Beatles-song-makes-you-younger demonstration study, and by Daryl Bem's 2011 ESP (precognition) paper.

## Keywords

- [[C - P-Hacking]]

## Claims

### Claim 1

Claim ID: `the-art-of-statistics-learning-from-data__ch12-C001`

Fingerprint: `585a773325ac`

Text: 'Questionable research practices' (P-hacking) — undisclosed flexible choices made during data collection and analysis (e.g. deciding when to stop collecting data based on interim significance, selectively excluding data, trying multiple outcome variables or subgroups and reporting only the significant one, or 'HARKing': hypothesizing after results are known) — inflate the false-positive rate of a study without requiring literal, formally separate multiple tests; a 2012 survey found 94% of academic psychologists admitted to at least one such practice, and the distinction between exploratory studies (where such flexibility is legitimate) and confirmatory studies (which require a pre-registered, fixed protocol) is the key discipline for avoiding this failure mode.

Type: `mechanism`

Section: `'Questionable Research Practices'`

Target Node: [[C - P-Hacking]]

Decision: `ENRICH`

## Notes

- **ENRICH:** Folded into [[C - P-Hacking]] (created from Chapter 10) as the natural continuation of the same mechanism — 'researcher degrees of freedom' is the undisclosed-analytic-flexibility route to the same false-discovery-rate inflation that formal multiple testing produces mechanically.

## Completeness

- Claims extracted: 1
- Claims rejected: the specific fraud/error case studies (Reinhart-Rogoff, AXA Rosenberg, Cyril Burt) treated as Minimal Examples inside [[C - P-Hacking]] rather than separate claims.
- Claim density: normal (mostly narrative case studies illustrating one core mechanism already captured).
