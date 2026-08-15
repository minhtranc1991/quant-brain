---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - quantitative-trading
layer: strategy
type: core
domain:
  - quantitative-trading
  - factor-investing
  - risk-management
---
## 1. Objective

Earn a return premium (or a market-like return at lower realized risk, potentially levered up to match the market's volatility) by holding stocks with low measured beta/volatility, exploiting the empirically flat relationship between [[M - Capital Asset Pricing Model]] beta and realized return documented in Chapter 9.

## 2. Alpha Logic

If beta and realized return really are unrelated (as Fama and French's 1992 decile study found), then a low-beta portfolio should earn a return similar to the market's while carrying materially less volatility — and that low-beta portfolio can then be leveraged (bought partly on margin) back up to a beta of roughly 1, in principle capturing the market's return at the market's risk level while starting from a more favorable risk-return ratio than an unlevered high-beta portfolio would offer. This is sometimes called a "betting against beta" strategy. The logic depends entirely on the empirical CAPM anomaly holding; it is not a separate, independently-motivated theory of return.

## 3. Models Used

- [[M - Capital Asset Pricing Model]]

## 4. Signal

- Rank stocks by trailing beta (or realized volatility) and go long the lowest-volatility decile; optionally apply margin leverage to restore market-level portfolio beta.

## 5. Entry / Exit Conditions

- **Entry:** Hold a diversified basket of the lowest-measured-volatility stocks in a benchmark universe (source's example: the SPDR/PowerShares S&P 500 Low Volatility ETF, ticker SPLV, holds the 100 least-volatile stocks in the S&P 500).
- **Exit:** Periodic re-ranking/rebalancing as measured volatility rankings change.

## 6. Risk Management

- Position sizing: the leveraged variant explicitly doubles both return *and* volatility relative to the underlying low-beta basket — the source's own illustration: a $100 position split $50 equity/$50 margin borrowing, with a 10% underlying move producing a 20% move in the investor's equity stake (symmetric on the downside).
- The source flags that low-volatility strategies are typically *not* sector-diversified — they concentrate heavily in defensive sectors (SPLV held nearly one-third of its portfolio in utility stocks alone, without adjusting for this concentration), meaning "low volatility" at the individual-stock level does not translate into low concentration risk at the portfolio level.

## 7. Failure Modes

- All three low-volatility ETFs the source examines (LGLV, SPLV, USMV) had, as of the book's data through Q1 2014, failed to outperform their capitalization-weighted benchmarks in real-money terms, despite the strategy's theoretical motivation from a genuine, well-documented CAPM anomaly.
- Sector concentration (heavy utility/pharmaceutical weighting) exposes the strategy to sector-specific risk factors (e.g. interest-rate sensitivity for utilities) not captured by the "low volatility" label itself.

## 8. Backtest

- Period: iShares MSCI USA Minimum Volatility ETF (USMV) and comparable low-volatility ETFs, May 2011 through Q1 2014 (real-money, not simulated).
- Results: Low-Volatility average annual return 14.59% vs. Russell 1000 benchmark 15.29% over the same period — underperformed its capitalization-weighted benchmark in this real-money sample.
- Data source: Morningstar.

## 9. Execution

- _(No dedicated Execution note in this vault yet for low-volatility/margin-leverage trading mechanics.)_

## 10. Related Case Studies

- _(None created in this ingestion.)_
