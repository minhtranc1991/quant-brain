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
  - statistics
---
## 1. Definition

**Modern Portfolio Theory (MPT)** is a mathematical model that formalizes [[C - Diversification]] — developed by Harry Markowitz (1950s, Nobel Prize 1990), it defines investment risk as the variance/standard deviation of portfolio returns and shows how combining securities whose returns are not perfectly correlated can reduce a portfolio's total risk below the weighted-average risk of its individual holdings, for any given level of expected return.

## 2. Intuition

- MPT reframes portfolio construction as a risk-reduction optimization problem rather than a security-by-security "which stock is best" problem: the relevant question shifts from "how risky is this security alone?" to "how does this security's risk interact with the rest of the portfolio's risk, via its covariance with the other holdings?" A volatile security can lower portfolio risk if its returns are weakly or negatively correlated with the rest of the portfolio.
- Numerical illustration (from the source): an umbrella manufacturer and a resort business each individually swing between +50% and -25% depending on the weather, and are risky in isolation; combined 50/50, since their fortunes are exactly opposite, the investor earns a guaranteed 12.5% in every season — total risk elimination in this idealized perfect-negative-correlation case. Realistically, most securities move somewhat together (positive but imperfect correlation), so diversification reduces but does not eliminate risk.
- What determines how much risk reduction is achievable: the correlation coefficient between the assets being combined. The book's own reference table: correlation +1.0 → no risk reduction possible; +0.5 → moderate reduction; 0 → considerable reduction; -0.5 → most risk eliminated; -1.0 → all risk eliminated. This single relationship is MPT's central practical takeaway: even *positive but imperfect* correlation (the realistic case for most stocks) still yields meaningful risk reduction — negative correlation is not required, just correlation below +1.

## 3. Mathematical perspective

$$\sigma_p^2 = \sum_i w_i^2 \sigma_i^2 + \sum_i \sum_{j \neq i} w_i w_j \, \text{COV}_{ij}$$

Where:
- $\sigma_p^2$ — portfolio return variance (risk)
- $w_i$ — portfolio weight of asset $i$
- $\sigma_i^2$ — variance of asset $i$'s returns
- $\text{COV}_{ij}$ — covariance between assets $i$ and $j$'s returns; for the two-asset case, $\text{COV}_{UR} = \sum_s p_s(U_s - \bar U)(R_s - \bar R)$ summed over economic states $s$.

For two assets, this simplifies to $\sigma_p^2 = w_1^2\sigma_1^2 + w_2^2\sigma_2^2 + 2w_1w_2\,\text{COV}_{12}$, making explicit that portfolio variance is strictly less than the weighted-average of individual variances whenever $\text{COV}_{12} < \sigma_1\sigma_2$ (i.e. correlation below +1).

## 4. Assumptions

- Investors are risk-averse: for a given expected return, they prefer lower variance; for a given variance, they prefer higher expected return (the book's characterization: "all investors are like my wife — they are risk-averse").
- Risk is adequately captured by return variance/standard deviation — an assumption the book itself flags as imperfect (only *downside* dispersion arguably constitutes true "risk," but variance is treated as a workable proxy given that well-diversified portfolio returns are roughly symmetric in practice).
- Historical covariances/correlations are usable estimates of future covariances/correlations, an assumption that is explicitly shown to be imperfect during systemic crises, when correlations tend to rise.

## 5. Estimation / Training Procedure

- Portfolio weights are chosen, in principle, via quadratic programming over the historically estimated covariance matrix of candidate assets to minimize portfolio variance for each target level of expected return (tracing out the "efficient frontier"); the book explicitly does not walk through this optimization mathematically, presenting only the underlying two-asset covariance logic and its empirical implications (the ~50-stock domestic diversification threshold, the ~17% historically risk-minimizing international allocation).

## 6. When it matters in Finance

- Directly informs how many holdings are needed to capture most attainable diversification benefit (empirically, ~50 well-diversified U.S. stocks), and how much international allocation historically minimized total portfolio risk (~17% in the book's own calculation over 1970-2013).
- The conceptual foundation for [[M - Capital Asset Pricing Model]], which builds directly on MPT's systematic/unsystematic risk decomposition.

## 7. Based On Concepts

- [[C - Diversification]]

## 8. Related Models

- [[M - Capital Asset Pricing Model]] — extends MPT by asking which *portion* of a security's risk (as defined by MPT) is compensated with extra expected return, given that diversification can eliminate the unsystematic portion.

## 9. Used In Strategies

- [[S - Passive Indexing]] — broad-based index funds are, in effect, an application of MPT's insight that a maximally diversified portfolio captures the market's risk-return tradeoff at minimal unsystematic risk.

## 10. Limitations / Pitfalls

- Diversification benefit within a single asset class (e.g. U.S. equities) diminishes sharply after roughly 50 well-chosen holdings.
- Correlations between asset classes are not stable — they tend to rise specifically during systemic crises (2007-09 is the book's own example), reducing diversification's protective value exactly when it would be most valuable, though correlations remaining below +1 still provided some benefit even then.
- Variance/standard deviation treats upside and downside dispersion symmetrically, which is a simplification the book acknowledges is imperfect, justified mainly by the empirical near-symmetry of well-diversified portfolio return distributions.

## 11. Minimal Example

- Ibbotson Associates' 1926-2013 data: small-company stocks, common stocks, long-term bonds, and Treasury bills show a consistent ordering where higher average historical return is paired with higher return standard deviation, consistent with MPT's risk-reward tradeoff framework, even though MPT's specific contribution is about *combining* assets rather than this single-asset-class ranking. Source: [[A Random Walk Down Wall Street]], Chapter 8.
