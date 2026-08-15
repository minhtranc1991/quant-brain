---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - portfolio-management
  - status/needs-review
layer: execution
type: core
domain:
  - portfolio-management
  - investing
  - risk-management
---
## 1. Definition

**Portfolio Rebalancing** is the mechanism that turns a [[S - Passive Indexing]] (or any target-asset-allocation) decision into a real order: periodically buying and selling holdings to bring a portfolio's actual asset-class proportions (e.g. stocks vs. bonds) back into line with a predetermined target allocation, after market movements have caused the actual proportions to drift.

## 2. Mechanics

- If a target 60% stocks/40% bonds allocation drifts to 70%/30% after stocks outperform bonds over a period, rebalancing means selling enough stocks (or equity fund shares) and buying enough bonds to restore the 60/40 split — mechanically forcing the systematic sale of recent outperformers and purchase of recent underperformers, without requiring any forecast of which asset class will do better next.
- The source's own empirical illustration (60% Russell 3000/40% Barclays Aggregate Bond, January 1996-December 2013, rebalanced at most once per year): the annually rebalanced portfolio returned 8.41%/year at 11.55% volatility (standard deviation), versus 8.14%/year at 13.26% volatility for the never-rebalanced version of the same starting allocation — rebalancing both reduced volatility *and* modestly increased average annual return over this specific historical period, because it systematically trimmed positions after they had risen (partially avoiding subsequent reversals) and added to positions after they had fallen (partially capturing subsequent recoveries).

## 3. When it matters

- Maintaining a life-cycle-appropriate risk level over time (Chapter 14) as market movements would otherwise passively drift a portfolio's risk profile away from an investor's intended stock/bond mix.
- A disciplined, rules-based alternative to discretionary trading decisions that are vulnerable to overconfidence and loss aversion (e.g. the disposition effect of holding losers and selling winners, per the vault's behavioral-finance Concepts) — rebalancing enforces the opposite, contrarian-by-construction behavior automatically.

## 4. Parameters

- Target allocation: a predetermined stock/bond (or broader multi-asset-class) mix suited to the investor's age and risk tolerance.
- Rebalancing frequency: the source's own study used at most once per year; more frequent rebalancing was not shown to be necessary or clearly superior in the cited results.
- Applies specifically to low-cost index fund holdings in the source's own study design (taxes were explicitly not considered in the cited results, a caveat the source itself flags).

## 5. Strategy Context

- [[S - Passive Indexing]]

_(Execution → Strategy, `implements` — the inverse of the Strategy's own `executed_by` edge.)_

## 6. Pitfalls

- The source's own study explicitly did not account for taxes; rebalancing a taxable (non-tax-advantaged) account triggers capital-gains realization when trimming appreciated positions, which can materially reduce or eliminate the technique's net-of-tax benefit — a real limitation the cited results do not capture.
- Rebalancing improving *both* risk and return in the specific 1996-2013 period studied is a historical result, not a guarantee; it depends on the specific pattern of asset-class returns over that period (particularly the dot-com bust and 2008-09 crisis, both of which created exactly the kind of overshoot-then-partial-reversal pattern rebalancing is designed to exploit) and should not be read as a universal law that rebalancing always increases return.
