---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - quantitative-trading
  - status/needs-review
layer: concept
type: core
domain:
  - quantitative-trading
  - investing
  - market-microstructure
---
## 1. Definition

**Efficient Market Hypothesis (EMH)** is the claim that a security's market price already incorporates all available information relevant to its value, so that no investor can systematically earn above-average risk-adjusted returns using that information. It has three nested forms: **weak** (prices reflect all information in past prices — see [[C - Random Walk Hypothesis]]), **semi-strong** (prices reflect all *public* information, so fundamental analysis of public data cannot yield an edge), and **strong** (prices reflect *all* information, including private/inside information).

## 2. Intuition

- EMH does not claim prices are "correct" in the sense of matching true intrinsic value at every moment — it claims prices react so quickly to new (unpredictable) information that no one can trade fast enough to profit from the adjustment. Since real news arrives randomly, price *changes* are random even though prices themselves may be systematically wrong at any given instant; the two claims (unpredictable changes vs. correct levels) are logically distinct, and EMH is fundamentally about the former.
- Mechanism: many participants continuously search for mispriced securities; whichever mispricing they find, their own buying/selling pressure eliminates it. The stronger and more numerous the searchers, the faster mispricings vanish — this is why EMH is a *degree* claim (closer to a "frictionless ideal," per Andrew Lo's analogy to engine efficiency) rather than an all-or-nothing one.
- Competing view (see [[C - Limits to Arbitrage]] and [[C - Herd Behavior]]): behavioral finance argues that (1) many investors are not fully rational and their errors are *correlated* rather than random/canceling, and (2) arbitrage — the mechanism supposed to correct mispricing — is itself risky and constrained, so mispricing can persist longer than a rational trader can remain solvent. Malkiel's own synthesis (Ch. 11) is that markets are not *perfectly* efficient but come "very close to the EMH ideal," and that documented anomalies are more often explained as compensation for risk than as free, reliably exploitable inefficiency — a position he holds while explicitly acknowledging the behavioral counter-evidence rather than dismissing it.

## 3. Mathematical perspective (if applicable)

No single canonical formula; operationally tested via the CAPM/factor-model residual: an asset's realized excess return $R_i - R_f$ should equal its risk-adjusted expected return (e.g. $\beta_i(R_m - R_f)$ under [[M - Capital Asset Pricing Model]]) plus a mean-zero, unpredictable error. Systematic (persistently nonzero, forecastable) "alpha" in that residual across many managers/funds is evidence against EMH in its tested form.

## 4. When it matters

- Justifies index/passive investing as a default: if consistently identifying mispriced securities net of costs is not reliably possible, capturing the market return at minimal cost dominates most active strategies for most investors.
- Frames the debate over "smart beta" (see [[C - Smart Beta]]) and behavioral-finance-motivated strategies as a live empirical question — is a documented pattern exploitable mispricing, or priced risk?

## 5. Formalized By (Models)

- [[M - Capital Asset Pricing Model]] — a specific model of how risk (not information) should determine expected return under an efficient-market premise.
- [[M - Fama-French Three-Factor Model]] — extends the risk-based explanation for return patterns that might otherwise look like EMH violations.

## 6. Related Concepts

- [[C - Random Walk Hypothesis]] — the weak form of EMH restricted to past-price information.
- [[C - Limits to Arbitrage]] — the behavioral-finance mechanism explaining why EMH can fail to hold exactly even with some rational, well-capitalized traders present.
- [[C - Survivorship Bias]] — a measurement artifact that can make active management appear more successful than EMH would predict if not corrected for.

## 7. Pitfalls

- EMH is often misquoted as "prices always reflect true value" or "prices move randomly and erratically" — Malkiel explicitly rejects both misreadings: prices move unpredictably *because* the market reacts efficiently to real (random) news, not because the market is careless or arbitrary.
- Empirical tests of EMH are joint tests of market efficiency *and* whatever risk/pricing model is used to define "abnormal" return — a documented "anomaly" may reflect a mis-specified risk model (e.g. an incomplete beta) rather than a true inefficiency. This is the same joint-hypothesis issue that motivates APT and Fama-French as alternative risk models.

## 8. Minimal Example

- Malkiel and Cragg's study surveying 19 major Wall Street firms' one-year and five-year earnings forecasts for a large sample of S&P 500 companies found the forecasts performed no better than naive extrapolation of past trends, and for five-year horizons sometimes worse — evidence that skilled, well-resourced professional analysts could not reliably out-forecast a simple no-information baseline, consistent with semi-strong EMH. Source: [[A Random Walk Down Wall Street]], Chapter 7.
