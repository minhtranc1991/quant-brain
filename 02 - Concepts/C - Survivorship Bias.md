---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - statistics
  - status/needs-review
layer: concept
type: core
domain:
  - statistics
  - investing
  - quantitative-trading
---
## 1. Definition

**Survivorship Bias** is the distortion that arises when a performance sample includes only entities (funds, companies, strategies) that have survived to the measurement date, systematically excluding those that failed, were merged away, or were discontinued — inflating the apparent average performance of the surviving group relative to the true population that originally existed.

## 2. Intuition

- Mechanism, as the book documents specifically for mutual funds: poorly performing funds are commercially embarrassing, so fund management complexes tend to merge or close them rather than let their track records stand — quietly removing the worst performers from any dataset built from currently-existing funds. A performance study using only funds that exist *today* therefore systematically overstates how well the *average* fund (including the ones that no longer exist) actually performed.
- What determines the *magnitude* of the bias: the longer the look-back period and the higher the attrition rate in the population, the larger the distortion. The book's own illustration is stark: of 358 equity mutual funds that existed in 1970, only 84 (about 23%) still existed in 2013; a performance study restricted to those 84 survivors is measuring a highly selected, above-average-quality subset, not the original population.
- The bias runs in one consistent direction (inflating apparent average performance), which makes it a a systematic rather than random source of error — a key reason the book treats even survivorship-bias-*adjusted* studies as still probably somewhat generous to active management, and treats studies that ignore the bias entirely as materially overstating how many funds "beat the market."

## 3. Mathematical perspective (if applicable)

_(Not applicable — the book demonstrates the effect through a direct empirical count (358 funds in 1970 vs. 84 surviving to 2013) rather than a formal statistical correction model.)_

## 4. When it matters

- Any comparison of active fund/strategy performance against a benchmark index must account for survivorship bias, or the comparison will overstate how many managers/strategies "beat the market" and by how much.
- Directly relevant to evaluating claims made for [[C - Smart Beta]] strategies and any backtested trading strategy: a backtest run only on securities/funds that exist today implicitly excludes failures, inflating apparent historical performance.

## 5. Formalized By (Models)

- _(No dedicated formal survivorship-bias-correction Model exists yet in this vault.)_

## 6. Related Concepts

- [[C - Efficient Market Hypothesis]] — survivorship bias is one of the measurement artifacts that can make active management appear to outperform a genuinely efficient market when it does not, once corrected for.

## 7. Pitfalls

- Survivorship bias affects not only fund-level studies but any backtest built on a security universe defined "as of today" (e.g. today's S&P 500 constituents) rather than the universe that actually existed at each historical point in time.

## 8. Minimal Example

- Of the 358 equity mutual funds in existence in 1970, only 84 could be tracked through 2013 (274 had been merged away or closed); even measuring only those 84 survivors — already a favorably biased sample — very few beat the market index by 2 percentage points or more, illustrating both the presence of survivorship bias and the difficulty of beating the market even after the bias inflates the apparent success rate. Source: [[A Random Walk Down Wall Street]], Chapter 7.
