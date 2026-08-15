---
artifact: chapter
source: "Thinking, Fast and Slow"
source_id: thinking-fast-and-slow
chapter_id: thinking-fast-and-slow__ch10
chapter_number: 10
chapter_title: "The Law of Small Numbers"
extraction_status: extracted
---

# Chapter 10 — The Law of Small Numbers

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[Thinking, Fast and Slow]]

## Summary

Shows that people (including trained researchers) systematically underestimate how much small samples vary by chance, over-interpreting small-sample extremes (e.g. the county-level kidney-cancer-rate study, where both the highest and lowest rates cluster in the same sparsely-populated counties) as meaningful signal rather than sampling noise.

## Keywords

- [[C - Central Limit Theorem]]

## Claims

### Claim 1

Claim ID: `thinking-fast-and-slow__ch10-C001`

Fingerprint: `1ff41f82e675`

Text: Intuitive judgment systematically underweights how much small samples vary by chance alone (the 'Law of Small Numbers') — people, including trained researchers, expect even a small sample to closely resemble the population it was drawn from, and consequently over-interpret small-sample extremes (in either direction) as meaningful signal rather than as expected statistical noise; the same underlying counties can simultaneously show both the highest and lowest rates of a rare outcome purely because sparse populations produce more variable sample statistics.

Type: `empirical_claim`

Section: `The Law of Small Numbers`

Target Node: [[C - Central Limit Theorem]]

Decision: `EXISTING`

## Notes

- **[[ENRICH]]:** Extends [[C - Central Limit Theorem]]'s Pitfalls section — the CLT note already documents that small/skewed samples converge slowly to the normal approximation; this claim adds the complementary cognitive-bias angle (that people's *intuitions* about small-sample variability are miscalibrated, not just that the formal approximation is less reliable).

## Completeness

- Claims extracted: 1
- Claims rejected: 0
- Claim density: normal.
