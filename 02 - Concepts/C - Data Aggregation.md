---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - data-analysis
  - status/needs-review
layer: concept
type: core
domain:
  - data-analysis
  - quantitative-research
  - computational-methods
---
## 1. Definition

**Data Aggregation** (split-apply-combine) is the general pattern of partitioning a dataset by one or more grouping keys, independently applying a computation to each resulting partition, and recombining the per-partition results into a single output — the framework underlying grouped summary statistics, group-relative transformations, and pivot-style reshaping alike.

## 2. Intuition

- Mechanism: rather than treating "compute the mean by category," "rank within each group," and "build a pivot table" as unrelated operations, all three are the same three-step pattern (split by key → apply a function → combine results) with a different *apply* function and a different *combine* shape. Recognizing the shared pattern is what makes grouped computation generalizable — a new grouping key type (a column, an external array, or a callable) or a new apply function (built-in, custom, or multiple simultaneous functions) plugs into the same framework rather than requiring new special-case logic.
- The aggregation-vs-transformation distinction is the key structural fork within "apply": *aggregation* reduces each group to a lower-dimensional summary (one row per group — a genuine reduction), while *transformation* returns a result aligned with the original data's shape and index (e.g. a group-relative z-score or rank, where every original row still gets a value). Conflating the two is a common source of shape-mismatch errors or accidentally losing row-level granularity the analysis still needed.
- Pivot tables and cross-tabulation are the *combine* step's reshaping choice — promoting one or more grouping dimensions into row/column labels of a 2D layout — a presentation-oriented view of the same underlying grouped computation, not a separate mechanism.

## 3. Mathematical perspective (if applicable)

_(Not applicable as a formal model — this is a computational pattern; the individual aggregation functions applied within it (mean, sum, etc.) are ordinary descriptive statistics with no additional formalism introduced by the pattern itself.)_

## 4. When it matters

- Any quantitative-research task that requires a per-group (per-asset, per-sector, per-time-bucket) statistic — e.g. computing factor exposure by sector, or a rolling per-asset volatility — is an instance of split-apply-combine.
- Deciding whether a computed result should replace each group with a single row (aggregation) or annotate every original row (transformation) has direct downstream consequences for how the result can be re-joined to the original dataset.

## 5. Formalized By (Models)

_(None yet in this vault — this is a computational-methods Concept rather than a quantitative Model.)_

## 6. Related Concepts

- [[C - Vectorized Computation]] — the "apply" step within each partition is typically itself a vectorized array operation, not a nested loop.
- [[C - Missing Data Handling]] — grouped aggregation must make an explicit choice about whether to include or exclude missing values within each group.
- [[C - Time-Series Data Alignment]] — resampling a time series to a coarser frequency is a time-indexed special case of the same split-apply-combine pattern (splitting by time bucket instead of a categorical key).

## 7. Pitfalls

- Using an aggregation where a transformation was needed (or vice versa) — the resulting shape mismatch, or the accidental loss of row-level detail, is often only caught downstream when a join or an index-alignment step fails unexpectedly.
- Silently dropping groups with missing keys without an explicit decision about whether that's the intended behavior.

## 8. Minimal Example

- Computing each asset's return z-scored *within its own sector* on a given day is a transformation (every asset keeps a row, now holding a group-relative value), whereas computing each sector's *average* return that day is an aggregation (one row per sector, the per-asset rows are gone) — same grouping key, different apply/combine outcome.

---
**Provenance:** Author Claim — [[Python for Data Analysis]], Chapter 10 (Data Aggregation and Group Operations). The quant-research framing in §4 ("factor exposure by sector," "per-asset volatility") is a Quant Interpretation extending the book's general data-analysis framing to this vault's domain, not a claim made by the source itself.
