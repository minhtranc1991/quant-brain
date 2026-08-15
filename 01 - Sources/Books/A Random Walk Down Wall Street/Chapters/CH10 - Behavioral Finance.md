---
artifact: chapter
source: "A Random Walk Down Wall Street"
source_id: a-random-walk-down-wall-street
chapter_id: a-random-walk-down-wall-street__ch10
chapter_number: 10
chapter_title: "Behavioral Finance"
extraction_status: extracted
---

# Chapter 10 — Behavioral Finance

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[A Random Walk Down Wall Street]]

## Summary

Surveys the behavioral-finance critique of EMH, grounded in Kahneman and Tversky's work. Four systematic sources of investor irrationality are covered in depth: overconfidence (miscalibrated confidence intervals, illusion of control, the representativeness heuristic), biased judgments, herding (Asch conformity experiments, social/word-of-mouth contagion, mutual-fund manager herding), and loss aversion (Kahneman-Tversky prospect theory: losses feel roughly 2.5x as painful as equivalent gains feel pleasurable, producing the disposition effect of holding losers and selling winners, and framing effects). The chapter also covers the 'limits to arbitrage' argument -- why rational arbitrageurs cannot reliably correct mispricing (noise-trader risk, short-selling constraints, absence of perfect substitutes, as in the Royal Dutch/Shell 'Siamese twin' anomaly) -- and closes with practical behavioral lessons for investors (avoid herding, avoid overtrading, sell losers not winners, distrust IPOs/hot tips/foolproof schemes).

## Keywords

- [[M - Prospect Theory]]
- [[C - Overconfidence Bias]]
- [[C - Herd Behavior]]
- [[C - Loss Aversion]]
- [[C - Limits to Arbitrage]]

## Claims

### Claim 1

Claim ID: `a-random-walk-down-wall-street__ch10-C001`

Fingerprint: `a7e4e755b901`

Text: Investors are systematically overconfident: in calibration experiments where subjects set 98%-confidence intervals for future values (e.g. the Dow Jones one month out), actual outcomes fall outside the stated range roughly 20% of the time rather than the expected 2%, and this overconfidence is measurably stronger in men than women and correlates with higher trading frequency and worse net returns.

Type: `empirical_claim`

Section: `Overconfidence`

Target Node: [[C - Overconfidence Bias]]

Decision: `NEW`

### Claim 2

Claim ID: `a-random-walk-down-wall-street__ch10-C002`

Fingerprint: `c544aaf449f8`

Text: Herding is the tendency for investors' decisions to be systematically correlated rather than independent, driven by social proof and word-of-mouth contagion (documented experimentally in Asch's conformity experiments and empirically in mutual-fund managers clustering into the same stocks by geography); herding produces self-reinforcing bubbles because errors of irrational investors reinforce rather than cancel each other out.

Type: `mechanism`

Section: `Herding`

Target Node: [[C - Herd Behavior]]

Decision: `EXISTING`

### Claim 3

Claim ID: `a-random-walk-down-wall-street__ch10-C003`

Fingerprint: `ed5507bfb0f9`

Text: Prospect theory (Kahneman-Tversky) replaces expected-utility-over-final-wealth with a value function defined over gains and losses relative to a reference point; losses are roughly 2.5x as psychologically painful as equivalent gains are pleasurable (loss aversion), and the same objective outcome produces different choices depending on whether it is framed as a gain or a loss (framing effect); the theory also predicts risk-seeking behavior when choosing among sure losses versus a gamble with the same expected value.

Type: `theoretical_claim`

Section: `Loss Aversion`

Target Node: [[M - Prospect Theory]]

Decision: `NEW`

### Claim 4

Claim ID: `a-random-walk-down-wall-street__ch10-C004`

Fingerprint: `572da0a63bab`

Text: Loss aversion produces a 'disposition effect' -- a documented tendency for investors to sell winning positions (to realize pride/lock in a win) and hold losing positions (to avoid realizing regret/admitting a mistake) -- which is tax-inefficient and contrary to the rational prescription of realizing losses for tax purposes.

Type: `empirical_claim`

Section: `Pride and Regret`

Target Node: [[C - Loss Aversion]]

Decision: `NEW`

### Claim 5

Claim ID: `a-random-walk-down-wall-street__ch10-C005`

Fingerprint: `23ed5f379ea4`

Text: Arbitrage cannot be relied on to fully correct mispricing caused by irrational investors because real-world arbitrage is risky and constrained: a mispriced security may have no perfect substitute to hedge against (as with Royal Dutch/Shell trading at a persistent premium/discount to their contractual 1.5:1 profit-split ratio), short selling may be technically impossible or capital-constrained (as with Long-Term Capital Management), and 'overpriced' securities can become more overpriced before correcting, so 'the market can remain irrational longer than the arbitrageur can remain solvent.'

Type: `theoretical_claim`

Section: `The Limits to Arbitrage`

Target Node: [[C - Limits to Arbitrage]]

Decision: `NEW`

## Notes

- **NEW_NODE:** Overconfidence Bias, Loss Aversion, and Limits to Arbitrage are new Concepts; Prospect Theory is created as a Model (it has a formal mathematical value function, not just a qualitative description) rather than a Concept. Herd Behavior enriches the Concept already created in Chapter 2 from the historical-bubble material -- same mechanism, deepened here with the psychological/experimental evidence.

## Completeness

- Claims extracted: 5
- Claims rejected: 0
- Claim density: normal
