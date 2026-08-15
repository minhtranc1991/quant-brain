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
  - factor-investing
---
## 1. Objective

Earn a return premium by holding stocks exhibiting positive relative price strength over the trailing period (typically the preceding 12 months, excluding the most recent month), on the premise that short-horizon price trends exhibit statistically detectable, if weak, continuation.

## 2. Alpha Logic

Two explanations offered by the source: (1) **behavioral** — a psychological feedback mechanism (Robert Shiller's account) in which investors observe rising prices and are drawn in via a "bandwagon effect," imparting a degree of self-reinforcing momentum (the same herding mechanism described in the source's behavioral-finance chapter); (2) **information-diffusion-based** — investors adjust their expectations only gradually to new information (especially earnings surprises), so prices respond to news with a lag rather than instantaneously, producing short-horizon return continuation as the market "catches up" to the news over time. Momentum coexists, at longer horizons, with the opposite pattern (return reversal/mean reversion) — the two are not contradictory once horizon is specified: momentum at short horizons, reversion at longer ones.

## 3. Models Used

- _(No formal risk-pricing Model in this vault currently incorporates a momentum factor; the book notes some analysts have proposed adding a momentum factor to the [[M - Fama-French Three-Factor Model]], but this vault has not yet created a four/five-factor extension note.)_

## 4. Signal

- Relative strength ranking: stocks whose trailing ~12-month return (excluding the most recent month, to filter out short-term reversal noise) is high relative to the broad market are ranked as positive-momentum candidates.

## 5. Entry / Exit Conditions

- **Entry:** Hold a diversified basket tilted toward stocks with strong recent relative price performance (the source's real-money example: the AQR Momentum Fund, ticker AMOMX).
- **Exit:** Periodic re-ranking and rebalancing as trailing-return rankings change; no discretionary stop-based exit specified in the source.

## 6. Risk Management

- Position sizing: implemented as a diversified basket (fund/ETF-level), not individual concentrated bets, similar to other "smart beta" factor strategies' implementation style.
- The source's own simulation (a 13-year study of buying stocks with the worst prior 3-5-year returns) found statistically strong evidence of return reversal at that longer horizon, but *no* corresponding improvement in the subsequent absolute return of the "reversal" group relative to the comparison group — i.e. reversal was statistically real but not translatable into a profitable contrarian trading edge, a caution that applies symmetrically to over-relying on momentum persistence at any single horizon.

## 7. Failure Modes

- Momentum findings are described as "not uniform across studies" and "quite a bit weaker in some periods than in others" — the effect is not presented as dependable in every market regime.
- Real-money implementation (AMOMX, since 2009) had, as of the book's data through mid-2014, failed to produce excess returns over either the Russell 1000 capitalization-weighted or Russell 1000 Growth benchmark ETFs, despite momentum's stronger academic backtest record relative to low-volatility strategies.

## 8. Backtest

- Period: AQR Momentum Fund (AMOMX), July 2009 through first half of 2014 (real-money, not simulated).
- Results: Momentum average annual return 19.54% vs. Russell 1000 benchmark 19.99% over the same period — the momentum strategy *underperformed* its capitalization-weighted benchmark in this specific real-money sample, contrary to the more favorable academic literature on momentum.
- Data source: Morningstar.

## 9. Execution

- _(No dedicated Execution note in this vault yet for momentum-strategy trading mechanics.)_

## 10. Related Case Studies

- _(None created in this ingestion.)_
