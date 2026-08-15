---
artifact: chapter
source: "Fooled by Randomness"
source_id: fooled-by-randomness
chapter_id: fooled-by-randomness__ch07
chapter_number: 7
chapter_title: "Skewness and Asymmetry"
extraction_status: extracted
---

# Chapter 07 — Skewness and Asymmetry

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[Fooled by Randomness]]

## Summary

States Taleb's own trading approach as 'skewed bets': favoring a large number of small, bounded losses against a small number of large, effectively unbounded gains, achieved concretely by buying (rather than selling) out-of-the-money options — on the argument that rare events are systematically mispriced (underpriced) relative to their true probability and impact.

## Keywords

- [[C - Rare Event Risk (Fat-Tail Mispricing)]]
- [[S - Asymmetric Rare-Event Betting]]

## Claims

### Claim 1

Claim ID: `fooled-by-randomness__ch07-C001`

Fingerprint: `7a218f737e69`

Text: Rare events are not fairly valued by markets, and the rarer the event, the more it tends to be undervalued in price; this creates a persistent opportunity to structure a portfolio around frequent small losses and infrequent, large, disproportionate payoffs rather than the reverse.

Type: `theoretical_claim`

Section: `Chapter 7`

Target Node: [[C - Rare Event Risk (Fat-Tail Mispricing)]]

Decision: `NEW`

### Claim 2

Claim ID: `fooled-by-randomness__ch07-C002`

Fingerprint: `68eefaad215a`

Text: Buying out-of-the-money options is a concrete way to implement a skewed-bet approach: the buyer risks only the (small) premium paid and bets that a rare, large move will occur, while the seller of the same option collects steady premium income but is exposed to the rare event's full downside; the author describes himself as a habitual option buyer rather than seller for this reason.

Type: `strategy_implication`

Section: `Chapter 7`

Target Node: [[S - Asymmetric Rare-Event Betting]]

Decision: `NEW`

## Notes

- **NEW_NODE:** Rare-event mispricing is the book's central, quant-relevant thesis and is genuinely distinct from existing vault concepts (Loss Aversion/Overconfidence Bias describe misjudgment, not a pricing opportunity).
- **NEW_NODE:** The book describes a concrete, actionable approach (buy OTM options; accept frequent small losses for rare large gains) with enough content (objective, alpha logic, position mechanics, risk profile) to justify a Strategy note, though the book provides no formal backtest — flagged as a limitation in the Strategy note itself.

## Completeness

- Claims extracted: 2
- Claims rejected: 0
- Claim density: high.
