---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - quantitative-trading
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

- Competing view (empirical, not merely behavioral): in "The Superinvestors of Graham-and-Doddsville" (an essay by Warren Buffett, given as Appendix 1 of [[The Intelligent Investor]]), a cohort of investors — Buffett himself, Walter Schloss, Tom Knapp, Bill Ruane, Charlie Munger, and others — independently learned and applied a common, identifiable intellectual framework (Graham-and-Dodd value investing: buying below [[C - Intrinsic Value]] with a [[C - Margin of Safety]]) and collectively produced long-term track records of market-beating returns. Buffett frames this directly as a rebuttal to the claim that persistent outperformance implies nothing beyond a "large enough coin-flipping population" producing lucky winners by chance: what distinguishes this group, in his argument, is that their outperformance traces to a shared, replicable method rather than to unrelated, independently-lucky strategies. A standard counter-caution applies even to this framing: the sample is small and was assembled retrospectively around already-known successes, so ordinary survivorship-bias concerns are not fully resolved by the "common intellectual source" argument alone — it strengthens the case against pure-chance explanations without settling the debate outright.

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
- **Enrichment — a complementary mechanism explanation, prediction markets as Bayesian consensus ([[The Signal and the Noise]]):** Nate Silver frames prediction markets (e.g. Intrade) and the stock market itself as a real-world, decentralized implementation of Bayesian consensus-formation — a continuously updating market price aggregates many participants' individually weakly-informative private forecasts into a single consensus probability, functioning as a practical alternative to each participant individually revising their belief through direct debate. Silver notes the historical/intellectual connection between Adam Smith's invisible hand and Bayesian updating (Smith and Thomas Bayes were contemporaries, both influenced by David Hume), framing market efficiency as an emergent, wisdom-of-crowds consequence of many individually fallible forecasts rather than any single participant's superior accuracy — while cautioning that a market built from fallible individual forecasters is itself a fallible, not perfect, aggregate forecaster ("a market that makes perfect predictions is a logical impossibility"). This is a complementary framing to the arbitrage-based mechanism already documented above from Malkiel: arbitrage explains why mispricings *close*, while the Bayesian-consensus framing explains why the *aggregate* price is informative in the first place. Source: [[The Signal and the Noise]], Chapter 11 ("If You Can't Beat 'Em...").

#status/needs-review
