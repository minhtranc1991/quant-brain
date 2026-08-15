---
artifact: chapter
source: "A Random Walk Down Wall Street"
source_id: a-random-walk-down-wall-street
chapter_id: a-random-walk-down-wall-street__ch09
chapter_number: 9
chapter_title: "Reaping Reward by Increasing Risk"
extraction_status: extracted
---

# Chapter 09 — Reaping Reward by Increasing Risk

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[A Random Walk Down Wall Street]]

## Summary

Introduces beta as a measure of a security's systematic (market, non-diversifiable) risk and the Capital-Asset Pricing Model (CAPM, Sharpe/Lintner/Black), which asserts that only systematic risk commands a return premium because unsystematic (firm-specific) risk can be diversified away. Reviews Fama and French's 1992 finding that realized returns show essentially no relationship to beta over 1963-90, presents counterarguments (measurement error in the 'market' proxy; time-varying/conditional betas restore some support), and introduces two multi-factor alternatives: Arbitrage Pricing Theory (APT, Stephen Ross), which adds macro risk factors (national income, interest rates, inflation) beyond beta, and the Fama-French Three-Factor Model, which adds firm size and price-to-book value as empirical risk proxies alongside beta.

## Keywords

- [[M - Capital Asset Pricing Model]]
- [[M - Fama-French Three-Factor Model]]
- [[M - Arbitrage Pricing Theory]]

## Claims

### Claim 1

Claim ID: `a-random-walk-down-wall-street__ch09-C001`

Fingerprint: `5ba7bfb944c3`

Text: A security's total risk (return variance) decomposes into systematic risk (beta, the tendency to move with the overall market, which cannot be eliminated by diversification) and unsystematic risk (firm-specific factors, which diversification can largely eliminate); the Capital-Asset Pricing Model holds that only systematic risk should command a risk premium, so expected return is a linear function of beta: Rate of Return = Risk-free Rate + Beta x (Market Return - Risk-free Rate).

Type: `theoretical_claim`

Section: `The Capital-Asset Pricing Model (CAPM)`

Target Node: [[M - Capital Asset Pricing Model]]

Decision: `NEW`

### Claim 2

Claim ID: `a-random-walk-down-wall-street__ch09-C002`

Fingerprint: `83fac1a0c1b6`

Text: Fama and French (1992) sorted all traded stocks into deciles by beta over 1963-90 and found essentially no relationship between decile beta and realized decile return, casting doubt on beta as a sufficient single predictor of long-run returns; Malkiel argues this evidence does not fully invalidate CAPM because the true 'market' portfolio (including human capital, bonds, real estate, etc.) is unmeasurable and betas vary cyclically, and cites Jagannathan and Wang finding stronger CAPM support once these are accounted for.

Type: `empirical_claim`

Section: `Let's Look at the Record / An Appraisal of the Evidence`

Target Node: [[M - Capital Asset Pricing Model]]

Decision: `EXISTING`

### Claim 3

Claim ID: `a-random-walk-down-wall-street__ch09-C003`

Fingerprint: `b65cbd795b31`

Text: Arbitrage Pricing Theory (Stephen Ross) generalizes CAPM's single-factor (beta) risk model to multiple systematic risk factors -- e.g. sensitivity to changes in national income, interest rates, and inflation -- on the premise that beta alone (a single stock index's co-movement) is too crude a proxy to capture all nondiversifiable risk.

Type: `theoretical_claim`

Section: `The Quant Quest for Better Measures of Risk: Arbitrage Pricing Theory`

Target Node: [[M - Arbitrage Pricing Theory]]

Decision: `NEW`

### Claim 4

Claim ID: `a-random-walk-down-wall-street__ch09-C004`

Fingerprint: `663b66e4776a`

Text: The Fama-French Three-Factor Model adds two empirical risk factors to beta: firm size (measured by market capitalization, smaller firms treated as riskier) and value (measured by the ratio of market price to book value, low price-to-book treated as a sign of financial distress/risk); it is debated whether these factors measure genuine priced risk or capture investor irrationality/mispricing instead.

Type: `theoretical_claim`

Section: `The Fama-French Three-Factor Model`

Target Node: [[M - Fama-French Three-Factor Model]]

Decision: `NEW`

## Notes

- **NEW_NODE:** CAPM, Arbitrage Pricing Theory, and the Fama-French Three-Factor Model are three distinct risk-pricing Models, each with a materially different mechanism (single beta vs. macro multi-factor vs. empirical size/value factors) -- created as separate notes per the New Knowledge Test rather than merged, with `extends`/`depends_on` cross-links (CAPM -> APT/Fama-French) in the Related Models sections.

## Completeness

- Claims extracted: 4
- Claims rejected: 0
- Claim density: normal
