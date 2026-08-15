---
artifact: chapter
source: "A Random Walk Down Wall Street"
source_id: a-random-walk-down-wall-street
chapter_id: a-random-walk-down-wall-street__ch08
chapter_number: 8
chapter_title: "A New Walking Shoe: Modern Portfolio Theory"
extraction_status: extracted
---

# Chapter 08 — A New Walking Shoe: Modern Portfolio Theory

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[A Random Walk Down Wall Street]]

## Summary

Introduces Harry Markowitz's modern portfolio theory (MPT): risk is defined as the variance/standard deviation of returns, and diversifying across imperfectly correlated securities can reduce a portfolio's total risk below the risk of its average holding, without necessarily sacrificing expected return. Uses a two-business island economy (resort vs. umbrella manufacturer) to show that even without negative correlation, diversification benefits exist as long as correlation is below +1. Empirically documents that ~50 well-diversified U.S. stocks captures most attainable domestic diversification benefit, and that adding a modest allocation (historically ~17%) of international stocks reduced portfolio risk further because non-U.S. and U.S. equity returns are not perfectly correlated, even though correlations have risen with globalization.

## Keywords

- [[M - Modern Portfolio Theory]]
- [[C - Diversification]]

## Claims

### Claim 1

Claim ID: `a-random-walk-down-wall-street__ch08-C001`

Fingerprint: `926e40a7baad`

Text: Financial risk is generally defined as the variance or standard deviation of a security's or portfolio's returns around its expected value; for reasonably symmetric return distributions, about two-thirds of returns fall within one standard deviation of the mean and 95% within two standard deviations.

Type: `definition`

Section: `Defining Risk: The Dispersion of Returns`

Target Node: [[M - Modern Portfolio Theory]]

Decision: `NEW`

### Claim 2

Claim ID: `a-random-walk-down-wall-street__ch08-C002`

Fingerprint: `be17203d28a2`

Text: A portfolio's risk can be lower than the weighted-average risk of its individual holdings whenever those holdings are not perfectly positively correlated (correlation coefficient < +1); the lower the correlation between two securities' returns, the greater the risk reduction from combining them, and a correlation of exactly -1 can in principle eliminate portfolio risk entirely.

Type: `mechanism`

Section: `Reducing Risk: Modern Portfolio Theory (MPT)`

Target Node: [[M - Modern Portfolio Theory]]

Decision: `NEW`

### Claim 3

Claim ID: `a-random-walk-down-wall-street__ch08-C003`

Fingerprint: `f37fcc66a142`

Text: Long-run historical data (Ibbotson Associates, 1926-2013) show that asset classes with higher average returns (small-company stocks > common stocks > long-term bonds > Treasury bills) also exhibit higher return variability/standard deviation, consistent with a general risk-reward tradeoff.

Type: `empirical_claim`

Section: `Documenting Risk: A Long-Run Study`

Target Node: [[M - Modern Portfolio Theory]]

Decision: `EXISTING`

## Notes

- **NEW_NODE:** Modern Portfolio Theory (mathematical model of risk/diversification) and Diversification (the underlying Concept it formalizes) are both new to the vault.

## Completeness

- Claims extracted: 3
- Claims rejected: 0
- Claim density: normal
