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
---
## 1. Definition

**Capital Asset Pricing Model (CAPM)** is a mathematical model that formalizes [[C - Diversification]]'s implication for expected return — developed by William Sharpe, John Lintner, and Fischer Black (Sharpe won the Nobel Prize in 1990) — asserting that only a security's *systematic* (non-diversifiable, market-correlated) risk, measured by beta, should command a return premium, because *unsystematic* (firm-specific) risk can be eliminated through diversification and therefore is not compensated.

## 2. Intuition

- Mechanism: total risk (variance) decomposes into systematic risk (co-movement with the overall market — cannot be diversified away because it reflects broad economic forces affecting nearly all stocks) and unsystematic risk (firm-specific events — a strike, a product discovery, a fraud — that diversification largely washes out once a portfolio holds ~30-60 securities). Since rational, diversified investors can eliminate unsystematic risk at no cost, the market should not pay them extra for bearing it; only the systematic component, beta, should be priced.
- Proof sketch given in the source: consider two 60-stock portfolios (Group I, Group II), both with average beta 1 but Group I's individual stocks carrying much higher unsystematic risk than Group II's. Once diversified across 60 names, unsystematic risk in both groups washes out, leaving both portfolios with essentially identical total risk (since beta is equal) — so if Group I's stocks offered higher return for their (illusory, in a diversified context) higher individual risk, rational investors would bid up Group I and sell Group II until returns equalized at the level implied by beta alone. This is the equilibrium argument for why only beta should be priced.
- Competing view / empirical challenge, presented directly and not resolved: Fama and French (1992) sorted stocks into beta deciles over 1963-90 and found essentially *no* relationship between decile beta and realized return — a major empirical crack in CAPM. Malkiel's counter-arguments (not a rebuttal so much as reasons for caution before discarding CAPM): (1) the true "market" portfolio (which should include bonds, real estate, human capital, and non-U.S. assets) is unmeasurable, and Jagannathan and Wang found CAPM support strengthens substantially once human capital and cyclically time-varying betas are incorporated; (2) even a flat beta-return line would still make beta a *useful* investment tool (buy low-beta stocks for market-like returns at lower risk, or lever them up) — so the finding undermines CAPM as a complete theory without making beta worthless as a risk-management input. The book's own synthesis (Chapter 9's "Summing Up") is that no single risk measure — beta included — fully captures the variety of systematic influences on stock returns, motivating [[M - Arbitrage Pricing Theory]] and [[M - Fama-French Three-Factor Model]] as multi-factor alternatives rather than replacements.

## 3. Mathematical perspective

$$E(R_i) = R_f + \beta_i\,(E(R_m) - R_f)$$

Where:
- $E(R_i)$ — expected return of security or portfolio $i$
- $R_f$ — risk-free rate of interest
- $\beta_i$ — the security's systematic risk, i.e. the covariance of its returns with the market's returns, scaled by the market's own variance: $\beta_i = \text{COV}(R_i, R_m) / \sigma_m^2$
- $E(R_m)$ — expected return of the overall market portfolio (by definition, $\beta_{market} = 1$)

The market's risk premium is $E(R_m) - R_f$; a stock's own risk premium is that market premium scaled by its beta.

## 4. Assumptions

- The "market" can be adequately proxied by a broad index (e.g. S&P 500 or Total Stock Market) — an assumption Richard Roll's critique directly challenges, since the true market portfolio in theory includes all risky assets, including non-traded ones like human capital.
- Investors hold diversified portfolios (30-60+ securities), so that unsystematic risk is genuinely eliminated in practice, not merely in principle.
- Beta, estimated from historical price co-movement, is a stable and forward-looking measure of a security's systematic risk — an assumption the book notes is imperfect, since betas for individual stocks are not stable over time and are sensitive to the choice of market proxy.

## 5. Estimation / Training Procedure

- Beta is estimated as the slope coefficient of a regression of a security's historical returns against the historical returns of a chosen market index (equivalently, $\text{COV}(R_i,R_m)/\sigma_m^2$); commercial beta estimates (Merrill Lynch, Value Line, Morningstar in the book's era) are produced this way from historical price data.

## 6. When it matters in Finance

- Used to evaluate portfolio manager performance via "alpha" (realized return in excess of what beta/CAPM would predict) — a usage the book notes remains widespread even among practitioners skeptical of CAPM as a complete theory.
- Directly motivates the low-volatility/"betting against beta" [[S - Low-Volatility Investing]] strategy: if the beta-return relationship really is flat, a levered low-beta portfolio could in principle match the market's beta and return at similar realized volatility.

## 7. Based On Concepts

- [[C - Diversification]]

## 8. Related Models

- [[M - Modern Portfolio Theory]] — CAPM's systematic/unsystematic risk decomposition builds directly on MPT's variance-based risk framework and diversification mechanics.
- [[M - Arbitrage Pricing Theory]] — generalizes CAPM's single beta factor to multiple systematic macro risk factors, motivated by the empirical weakness of beta alone.
- [[M - Fama-French Three-Factor Model]] — adds empirical size and value factors to beta as additional priced-risk proxies.

## 9. Used In Strategies

- [[S - Low-Volatility Investing]] — directly built on CAPM's beta concept and its empirically flat beta-return relationship.

## 10. Limitations / Pitfalls

- Fama and French (1992) found essentially no empirical relationship between beta decile and realized return over 1963-90 — the model's central empirical prediction has not held up cleanly over long historical periods.
- Beta estimates are highly sensitive to the choice of market proxy and are not stable over time for individual securities, per Richard Roll's critique.
- A single-factor model (beta only) may be too crude to capture all systematic risk influences on returns (interest rates, inflation, national income) — the direct motivation for APT and Fama-French as multi-factor extensions.

## 11. Minimal Example

- Illustration from the source: with a risk-free rate of 10% and expected market return of 15%, a portfolio that is half risk-free asset and half market portfolio (beta = 0.5) has expected return $0.10 + 0.5(0.15-0.10) = 12.5\%$; a portfolio levered to beta = 1.5 (borrowing to hold 1.5x the market) has expected return $1.5(0.15) - 0.5(0.10) = 17.5\%$ — both consistent with the CAPM formula. Source: [[A Random Walk Down Wall Street]], Chapter 9.
