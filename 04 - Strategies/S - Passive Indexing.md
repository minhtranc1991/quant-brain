---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - portfolio-management
  - status/needs-review
layer: strategy
type: core
domain:
  - portfolio-management
  - investing
  - quantitative-trading
---
## 1. Objective

Capture the broad market's average return, at minimal cost and maximal tax efficiency, by holding a capitalization-weighted portfolio of essentially all securities in a broad market index, rather than attempting to select individual outperforming securities or time entry/exit.

## 2. Alpha Logic

There is deliberately no attempt at alpha (excess-return-seeking): the strategy's logic rests directly on the Efficient Market Hypothesis and the book's cumulative evidence (Chapter 7) that professional stock selection and market timing do not reliably beat a broad index net of costs, combined with a structural, unavoidable arithmetic fact — since a capitalization-weighted index *is* the market by construction, the aggregate of all active investors, before costs, must earn exactly the market return; after costs (fees, trading costs, taxes), active management as a group must, on average, underperform. Indexing therefore captures the best achievable *net* return available to the average investor without needing any correct prediction about which securities or managers will outperform.

## 3. Models Used

- [[M - Modern Portfolio Theory]]

_(Justified directly by the Efficient Market Hypothesis and Diversification Concepts as well, but per the ontology's allowed Strategy→Model/Concept-via-Model relationship, only the Model note is linked here; no single Model is the strategy's sole basis.)_

## 4. Signal

- No selection signal — the defining feature of the strategy is the *absence* of a security-selection or market-timing signal; portfolio weights are simply proportional to each constituent's market capitalization.

## 5. Entry / Exit Conditions

- **Entry:** Purchase a low-cost, broad-based, capitalization-weighted index fund/ETF (e.g. a Total Stock Market fund) and hold continuously.
- **Exit:** No discretionary exit; holdings are maintained through market cycles ("the correct holding period for the stock market is forever," per Warren Buffett as quoted in Chapter 10), with periodic [[E - Portfolio Rebalancing]] against a target asset-allocation mix (stocks vs. bonds) rather than tactical selling.

## 6. Risk Management

- Broad diversification is the primary risk-management mechanism (see [[M - Modern Portfolio Theory]]); the strategy accepts full exposure to systematic (market) risk by design, since it makes no attempt to time or avoid market downturns.
- Combined in the book's life-cycle guidance (Chapter 14) with age-appropriate stock/bond allocation and [[E - Dollar-Cost Averaging]] for building the position over time, rather than a single lump-sum entry.

## 7. Failure Modes

- Does not protect against broad market declines (a capitalization-weighted index fund falls with the market in full, e.g. the ~50% decline from March 2008 to March 2009) — the strategy's risk management operates through diversification against *idiosyncratic* risk and long holding periods, not through downside protection against *systematic* risk.
- Requires investor discipline to avoid abandoning the strategy during downturns; the book documents that mutual-fund investors as a group have historically earned several percentage points less than the funds' own reported returns specifically because of poorly timed buying and selling around market peaks and troughs (a herd-behavior-driven timing penalty).

## 8. Backtest

- Period: Multiple multi-decade comparisons in the source, e.g. 20 years to December 31, 2013.
- Results: S&P 500 Index returned 9.22%/year vs. the average actively managed equity mutual fund's 8.36%/year over that period (an 0.86 percentage-point annual index advantage); S&P's SPIVA report (2014) found over two-thirds of active managers underperformed their benchmark index over a five-year horizon, a pattern the source states holds consistently across time periods, asset classes (domestic and international, large and small cap), and even the bond market.
- Data source: Lipper, Vanguard, S&P SPIVA Report (March 2014).

## 9. Execution

- [[E - Dollar-Cost Averaging]]
- [[E - Portfolio Rebalancing]]

## 10. Related Case Studies

- _(None created in this ingestion.)_
