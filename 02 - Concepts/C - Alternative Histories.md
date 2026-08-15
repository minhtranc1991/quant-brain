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
  - quantitative-trading
  - investing
---
## 1. Definition

**Alternative Histories** is the principle that a decision, strategy, or track record cannot be judged solely by the single outcome it happened to produce — it must be judged against the full range of counterfactual outcomes ("substitute courses of events") that could plausibly have occurred given the same process and the same level of risk taken.

## 2. Intuition

- Mechanism: any process with a random component generates a *distribution* of possible outcomes, of which only one is ever observed. Two decisions that produced identical realized outcomes can have taken on very different amounts of risk — e.g. $10 million earned playing Russian roulette (one bullet in six chambers) and $10 million earned through years of low-risk professional work are not equivalent, even though standard accounting records them identically, because the *dependence on luck* embedded in each path differs sharply.
- What determines whether the distinction matters in practice: the shorter the track record and the higher the variance/tail-risk of the process generating it, the more a single realized outcome can diverge from what the underlying process's typical or expected outcome actually looks like — and the more essential it becomes to reason about the unobserved alternative histories rather than the one that happened.
- Corollary emphasized by the book: evaluating success only by the observed outcome, without asking how many of the plausible alternative histories would have ended badly, systematically overrates decisions/strategies that happened to avoid a low-probability, high-impact failure.

## 3. Mathematical perspective (if applicable)

_(Not formalized with an explicit model in the source; illustrated with a Monte Carlo / Russian-roulette thought experiment — generating many simulated outcome paths from the same underlying process as a metaphor for the set of alternative histories.)_

## 4. When it matters

- Evaluating a trader's, fund's, or strategy's track record: a short run of good performance is weak evidence of skill if the strategy carries meaningful tail risk that simply has not yet been realized.
- Backtesting: a backtest reports one realized path over historical data; it says little about the strategy's risk unless the range of plausible alternative paths (e.g. via resampling/Monte Carlo) is also considered.
- Decision quality vs. outcome quality generally: a good decision can have a bad outcome (and vice versa) purely by chance — process quality and outcome quality are correlated but not identical.

## 5. Formalized By (Models)

- _(No dedicated formal Model exists yet in this vault; Monte Carlo simulation is described in the source as the practical tool for approximating a distribution of alternative histories, but no vault Model note currently formalizes it.)_

## 6. Related Concepts

- [[C - Survivorship Bias]] — a specific case of ignoring alternative histories: judging a *surviving* population's quality without considering the failed/discontinued members that represent the population's other alternative histories.
- [[C - Ergodicity]] — explains why, over a sufficiently long horizon, a strategy's exposure to a given alternative history (a rare event) approaches certainty rather than remaining merely possible.
- [[C - Rare Event Risk (Fat-Tail Mispricing)]] — the market-pricing implication of taking alternative histories seriously: if rare, damaging alternative histories are underweighted by other market participants, the instruments that pay off in those histories tend to be underpriced.

## 7. Pitfalls

- It is tempting to reconstruct "alternative histories" after the fact in a self-serving way (e.g. attributing a loss to bad luck but a gain to skill); the concept is meant to be applied symmetrically and prospectively (before the outcome is known), not as a post-hoc excuse.
- Taken to an extreme, obsessing over hypothetical alternative histories while ignoring the history that actually occurred is its own failure mode — the source explicitly warns against this over-correction.

## 8. Minimal Example

- Two traders each show +15% returns over one year. Trader A ran a diversified, moderate-volatility book; Trader B was short deep out-of-the-money options on a low-probability tail event that did not occur that year. Both realized the same outcome, but the range of alternative histories for Trader B includes catastrophic loss scenarios that Trader A's book does not — the one-year track record alone cannot distinguish them. Source: [[Fooled by Randomness]], Chapters 2–3.
