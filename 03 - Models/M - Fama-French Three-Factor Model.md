---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - portfolio-management
  - status/needs-review
layer: model
type: core
domain:
  - portfolio-management
  - quantitative-trading
  - risk-management
  - factor-investing
---
## 1. Definition

**Fama-French Three-Factor Model** is a mathematical model that formalizes [[C - Diversification]]'s implication for expected return using empirically-derived firm-characteristic factors — developed by Eugene Fama and Kenneth French — extending [[M - Capital Asset Pricing Model]]'s single beta factor with two additional risk factors: **size** (measured by total equity market capitalization) and **value** (measured by the ratio of market price to book value), on the premise that beta alone leaves a substantial, systematically explainable portion of the cross-section of stock returns unaccounted for.

## 2. Intuition

- Empirical starting point: Fama and French found that sorting stocks by market capitalization and by price-to-book ratio produces large, persistent differences in average returns that a single-beta CAPM cannot explain — smaller firms and firms with low price-to-book ratios ("value" stocks) have historically earned higher average returns than CAPM beta alone predicts.
- Two competing explanations for *why* size and value predict returns, both presented and left genuinely contested (not resolved) by the source: (1) **risk-based** — smaller firms may have more difficulty surviving recessions (higher sensitivity to GDP fluctuations = additional systematic risk not captured by beta), and low-price-to-book firms may be signaling genuine financial distress (the book's concrete example: major U.S. banks trading below book value in early 2009 were under real, not merely apparent, bankruptcy/nationalization risk); (2) **behavioral/mispricing-based** — investors may be overconfident about high-growth ("glamour"/growth) companies' prospects and systematically overpay for them, so low-P/E, low-P/BV stocks are simply underpriced rather than riskier. The book's position is that the risk-based explanation is more defensible in general, but explicitly notes "even those who would argue that low-market-to-book-value stocks provide higher returns because of investor irrationality find the Fama-French risk factors useful" empirically regardless of which causal story one accepts.
- What determines which explanation is more plausible in a given period is presented as an open, case-dependent question — the book does not claim to resolve it, only to show the empirical size/value factors are useful descriptively either way.

## 3. Mathematical perspective

$$E(R_i) - R_f = \beta_i\,(E(R_m) - R_f) + s_i\,\text{SMB} + h_i\,\text{HML}$$

Where:
- $\beta_i$ — market beta, as in CAPM
- $\text{SMB}$ ("Small Minus Big") — the size factor: the historical return premium of small-cap over large-cap stocks
- $\text{HML}$ ("High Minus Low") — the value factor: the historical return premium of high book-to-market (value) over low book-to-market (growth) stocks
- $s_i, h_i$ — the security's sensitivities (loadings) to the size and value factors respectively

_(The book presents the three risk factors — beta, size, value — narratively rather than deriving this regression equation explicitly; SMB/HML notation is the standard academic formalization of the factors it describes.)_

## 4. Assumptions

- Market capitalization and price-to-book ratio are adequate, stable proxies for the additional systematic risks they are meant to capture (financial-distress/recession-sensitivity risk) — an assumption directly disputed by the behavioral/mispricing alternative explanation.
- Historical size and value premiums are estimable and (to some degree) persistent into the future — an assumption the book's own real-money "smart beta" fund-performance evidence (Chapter 11) finds only partially supported.

## 5. Estimation / Training Procedure

- Size and value factor loadings are estimated via regression of a security's historical excess returns against the market excess return, SMB, and HML factor return series (standard Fama-French three-factor regression); the book does not walk through this regression mechanically but references the underlying decile-sort methodology (e.g. sorting all stocks into deciles by beta, or by market capitalization, and comparing average decile returns) as the empirical basis for the factors.

## 6. When it matters in Finance

- The empirical basis for value-tilted and size-tilted [[C - Smart Beta]] strategies, including [[S - Value Investing]] and the funds discussed in Chapter 11 (DFA's value/size funds, RAFI's Fundamental Index).
- Used as a standard tool to assess whether a portfolio's apparent outperformance ("alpha") is genuine skill or simply exposure to known size/value risk factors — the book applies exactly this test to RAFI's fund performance and finds its measured alpha becomes statistically zero once size and value exposure are controlled for.

## 7. Based On Concepts

- [[C - Diversification]]

## 8. Related Models

- [[M - Capital Asset Pricing Model]] — the Fama-French model directly extends CAPM's single-factor beta framework with two additional empirical factors.
- [[M - Arbitrage Pricing Theory]] — a related multi-factor extension of CAPM using macroeconomic rather than firm-characteristic factors; the book notes further extensions (momentum, liquidity, "quality" factors) have also been proposed by other analysts beyond the original three factors.

## 9. Used In Strategies

- [[S - Value Investing]] — directly built on the Fama-French value (HML) factor.

## 10. Limitations / Pitfalls

- Whether size and value factors represent genuine priced risk or exploitable mispricing remains disputed in the source itself, not resolved.
- Real-money fund/ETF performance following value and size tilts has been considerably weaker and more inconsistent across periods than the original academic decile-sort studies (Chapter 11's own performance-chart evidence), suggesting the factor premiums may be partly period-specific or eroded by implementation costs and popularity-driven crowding.

## 11. Minimal Example

- Applying the Fama-French three-factor regression to the RAFI Fundamental Index ETF's returns (which tilts toward value and size) finds its measured "alpha" (excess return beyond what beta, size, and value exposure would predict) is statistically zero — its apparent seven-year outperformance is fully explained by its factor tilts, not by any additional skill or genuine mispricing capture. Source: [[A Random Walk Down Wall Street]], Chapters 9, 11.
