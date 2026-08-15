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
  - data-quality
---
## 1. Definition

**Missing Data Handling** is the disciplined process of identifying invalid or absent observations (including domain-specific sentinel values that stand in for a true null) and deliberately choosing how to treat them — via removal, imputation, or explicit flagging — before those observations reach any downstream statistical or computational step.

## 2. Intuition

- Mechanism: real-world datasets frequently encode "missing" not as a native null but as a domain-specific sentinel (e.g. a placeholder numeric code, an empty string, or an implausible out-of-range value). If that sentinel isn't explicitly recognized and standardized first, every downstream computation (a mean, a regression, a backtest) silently treats invalid data as valid — the error is not visible at the point it's introduced, only in a distorted final result.
- What determines the right treatment: there is no universally correct choice among dropping the incomplete record, imputing with a statistic (mean, forward-fill), or using a domain-specific mapping. The trade-off is between data loss (dropping) and introduced bias (imputing with an assumption that may not hold) — which one dominates depends on the missingness mechanism (is the value missing at random, or missing in a way correlated with the outcome itself?), how much data would be lost, and how much distortion the downstream analysis can tolerate.
- A structurally similar judgment applies to duplicate records and outliers: both are cases where raw data cannot be used as-is, and the correct treatment is again context-dependent rather than a fixed rule.

## 3. Mathematical perspective (if applicable)

_(Not applicable as presented in the source — the book treats this as a pragmatic data-preparation discipline, not a formal statistical missing-data model such as MCAR/MAR/MNAR; a future source treating missingness mechanisms formally could enrich this note or motivate a separate Model note.)_

## 4. When it matters

- Any empirical or quantitative-research pipeline where the raw data was not collected under laboratory conditions — e.g. price/volume series with gaps, survey data, or any dataset merged from multiple sources with inconsistent conventions for representing "no value."
- Before any statistic (mean, correlation, regression coefficient) is computed from a dataset with any missingness — an unhandled sentinel value can silently and severely distort such a statistic.

## 5. Formalized By (Models)

_(None yet in this vault.)_

## 6. Related Concepts

- [[C - Survivorship Bias]] — a related but distinct failure mode: survivorship bias is about which *entities* are missing from a sample (funds/companies that no longer exist), whereas Missing Data Handling is about missing *observations* within an otherwise-included entity's record; both distort a statistic if left unaddressed, but the corrective action differs (adjust the sampling frame vs. clean the record).
- [[C - Data Aggregation]] — aggregation functions must decide (explicitly, via a `dropna`-style choice) whether to include or exclude missing values within each group, an application of this same judgment.

## 7. Pitfalls

- Assuming a numeric placeholder (e.g. -999) is a valid observation because it "looks like a number" — this is the single most common source of silently corrupted downstream statistics.
- Defaulting to always dropping incomplete records without considering whether the missingness itself is informative (e.g. non-random missingness correlated with the outcome), which can bias the remaining sample rather than merely shrinking it.

## 8. Minimal Example

- A dataset that uses `-999` to represent "not measured" for a price field: converting `-999` to a proper missing-value marker before computing a portfolio's average price is required, or that placeholder will silently pull the computed average far below the actual price level.

---
**Provenance:** Author Claim — [[Python for Data Analysis]], Chapter 7 (Data Cleaning and Preparation). The comparison to [[C - Survivorship Bias]] in §6 is an AI Interpretation connecting this book's data-preparation discipline to an existing vault Concept, not a claim made by either source.
