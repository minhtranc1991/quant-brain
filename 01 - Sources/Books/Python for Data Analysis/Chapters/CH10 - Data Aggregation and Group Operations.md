---
artifact: chapter
source: "Python for Data Analysis"
source_id: python-for-data-analysis
chapter_id: python-for-data-analysis__ch10
chapter_number: 10
chapter_title: "Data Aggregation and Group Operations"
extraction_status: extracted
---

# Chapter 10 — Data Aggregation and Group Operations

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[Python for Data Analysis]]

## Summary

Develops the split-apply-combine pattern as the general framework behind grouped computation: partition data by one or more grouping keys (columns, external arrays, or a callable), independently apply a computation to each partition, and recombine the results. Covers flexible grouping-key types, multiple simultaneous aggregation functions via `.agg()`, the distinction between aggregation (reduces dimensionality) and transformation (returns a result aligned to the original index/shape, e.g. group-relative normalization or ranking), and pivot tables/cross-tabulation as a reshaping of grouped results into a row/column layout.

## Keywords

- [[C - Data Aggregation]]

## Claims

### Claim 1

Claim ID: `python-for-data-analysis__ch10-C001`

Fingerprint: `baf37df24755`

Text: Split-apply-combine is the general pattern underlying grouped computation: partition data by one or more grouping keys, apply a computation independently to each partition, then recombine the results — a framework that generalizes across simple aggregations, custom functions, and multi-key grouping alike, rather than being a set of unrelated per-function behaviors.

Type: `theoretical_claim`

Section: `Data Aggregation and Group Operations`

Target Node: [[C - Data Aggregation]]

Decision: `NEW`

### Claim 2

Claim ID: `python-for-data-analysis__ch10-C002`

Fingerprint: `c8a2fb30f056`

Text: Aggregation and transformation are a meaningful distinction within grouped computation: aggregation reduces each group to a lower-dimensional summary (e.g. one row per group), while transformation returns a result aligned with the original data's shape and index (e.g. a group-relative z-score or rank) — conflating the two leads to shape-mismatch errors or accidentally discarding row-level granularity that the analysis still needed.

Type: `theoretical_claim`

Section: `Data Aggregation and Group Operations`

Target Node: [[C - Data Aggregation]]

Decision: `NEW`

## Notes

- Existing-node-first check: searched `02 - Concepts/` for Data Aggregation / GroupBy / Split-Apply-Combine; none found. Created as NEW_NODE.
- Pivot tables/cross-tabulation treated as a reshaping/presentation layer over the same split-apply-combine principle, not a separate claim.

## Completeness

- Claims extracted: 2
- Claims rejected: 0
- Claim density: normal.
