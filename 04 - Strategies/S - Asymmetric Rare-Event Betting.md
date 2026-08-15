---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - quantitative-trading
  - status/needs-review
layer: strategy
type: core
domain:
  - quantitative-trading
  - investing
---
## 1. Objective

Structure a portfolio to accept a high frequency of small, bounded losses in exchange for a low-frequency chance of a large, effectively unbounded gain — the opposite payoff shape from strategies that harvest steady, small gains at the risk of a rare, large loss. Described in the source as "skewed bets."

## 2. Alpha Logic

The edge does not come from forecasting direction; it comes from the claim that rare, high-impact events are systematically underpriced by the market (Concept: "Rare Event Risk (Fat-Tail Mispricing)"), driven in part by most participants extrapolating from rare-event-free historical samples (Concept: "Ergodicity") and by a general psychological/institutional preference for smooth, steady returns over the discomfort of frequent small losses (Concept: "Loss Aversion"). If rare events are underpriced, then structurally positioning to profit from them (rather than selling exposure to them for steady income) has a positive expected value even though it loses money most of the time.

_(Note: per `schema/ontology.md` §3, Strategy → Concept is not an allowed core-layer link — the Concepts underlying this Strategy's alpha logic are referenced by name in prose above, not as wikilinks. The formal Concept-layer treatment of "Rare Event Risk (Fat-Tail Mispricing)", "Ergodicity", and "Loss Aversion" lives in `02 - Concepts/`.)_

## 3. Models Used

- _(No dedicated formal pricing/positioning Model exists yet in this vault for this Strategy; the "Rare Event Risk (Fat-Tail Mispricing)" and "Ergodicity" Concepts provide the conceptual basis but are not yet formalized as a Model.)_

## 4. Signal

- No technical/quantitative entry signal is specified in the source; the position is structural/persistent rather than signal-triggered.
- Selection criterion described qualitatively: favor instruments/positions whose payoff is small and bounded in the common case and large (a substantial multiple of the amount risked) in the rare case — concretely, buying out-of-the-money options rather than selling them.

## 5. Entry / Exit Conditions

- **Entry:** Persistently hold (or continually roll) positions with a small, bounded cost in the base case and a large, asymmetric payoff in the rare case — e.g. buying out-of-the-money options across multiple instruments/markets rather than concentrating on forecasting any single rare event.
- **Exit:** The source does not specify a formal exit rule; a position either expires as a small loss (the common case) or is realized as a large gain when the rare event occurs.

## 6. Risk Management

- Position sizing: not formally specified in the source; the described approach relies on sizing each individual bet small enough that a long sequence of small losses is financially and psychologically sustainable while awaiting a rare payoff.
- Stop-loss / max drawdown: not applicable in the conventional sense — the strategy is designed so the maximum loss per position is bounded and known in advance (e.g. the premium paid for a purchased option), rather than controlled via a stop-loss rule.

## 7. Failure Modes

- Capital/psychological exhaustion: a long run of small losses before any rare payoff can exhaust capital or conviction even if the underlying rare-event-mispricing thesis is correct — the strategy can fail on implementation grounds without the thesis being wrong.
- Mispricing thesis failure: if rare events are not, in fact, persistently underpriced (e.g. option premia already reflect true tail probability), the strategy has a structurally negative expected value, since it loses small amounts with high frequency by construction.
- No formal risk framework: because the source provides no backtest, position-sizing rule, or portfolio-level construction, this Strategy note describes an approach, not a fully specified systematic strategy — see Limitations below.

## 8. Backtest

- Period: _(Not provided — the source's account is anecdotal, describing the author's personal trading career rather than a defined backtest.)_
- Results: _(Not provided in the source.)_
- Data source: _(Not applicable.)_
- **Limitation:** This Strategy note is derived from the source's narrative description of its author's approach, not from a documented, replicable backtest. Treat the "alpha logic" as a stated thesis with anecdotal support, not as empirically validated performance.

## 9. Execution

- _(No dedicated Execution note exists yet in this vault for options-buying execution mechanics; the source's description — buying out-of-the-money options and accepting time decay as the small recurring cost — implies an options-market execution context not yet covered by [[E - Dollar-Cost Averaging]] or [[E - Portfolio Rebalancing]].)_

## 10. Related Case Studies

- _(None extracted from this source; the source references the 1987 stock market crash as a rare event relevant to this approach, but does not develop it into a documented Case Study within the extracted text.)_
