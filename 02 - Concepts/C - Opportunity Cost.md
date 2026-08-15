---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - status/needs-review
layer: concept
type: core
domain:
  - quantitative-trading
  - investing
  - portfolio-management
---
## 1. Definition

**Opportunity Cost** is the value of the next-best alternative forgone when a scarce resource — time, capital, labor — is committed to one use instead of another. It is not a cash outlay; it is the real cost of any choice, measured in what the choice prevents.

## 2. Intuition

- Mechanism: any resource devoted to purpose A is, at that same moment, unavailable for purpose B, C, D... Choosing A implicitly means judging A's value higher than the best of the alternatives — the true "cost" of A is that forgone best alternative, not merely A's price tag.
- The mechanism is easiest to see in isolation (a single actor with one unit of a scarce resource, e.g. Robinson Crusoe choosing between fetching water or building shelter) and gets obscured in a complex economy only because so many simultaneous alternative uses are competing for the same capital and labor at once — the price system (see [[C - Price System as Information Mechanism]]) is the mechanism that continuously reveals which alternative use is currently most valuable, so opportunity cost can be assessed without a central accounting of every possible use.
- In portfolio and capital-allocation terms: holding cash, or committing capital to one position/strategy, has an opportunity cost equal to the best return available from the next-best alternative use of that same capital — the concept underlies any capital-budgeting or position-sizing comparison, even when no cash literally changes hands.

## 3. Mathematical perspective (if applicable)

No single canonical formula; operationally, for a choice between mutually exclusive uses of the same resource with expected returns $r_A, r_B, ...$, the opportunity cost of choosing $A$ is $\max(r_B, r_C, ...)$ — the best forgone alternative, not the sum of all alternatives.

## 4. When it matters

- Capital allocation and position sizing: capital committed to one trade/strategy cannot simultaneously fund another; comparing a strategy's expected return to its opportunity cost (e.g. a risk-free rate or the next-best strategy) is the basis of any relative-value or capital-budgeting decision.
- Evaluating "free" or "already-spent" resources: sunk costs are not opportunity costs and should not enter a forward-looking decision, a common but distinct pitfall (see below).
- Underlies the economic logic behind [[C - Price System as Information Mechanism]]: prices are the mechanism by which an economy continuously reveals opportunity costs without requiring any actor to know all alternative uses directly.

## 5. Formalized By (Models)

_(none yet — no vault Model formalizes opportunity cost directly; it underlies capital-budgeting logic implicit in [[M - Modern Portfolio Theory]]'s tradeoff framing rather than being formalized as its own model)_

## 6. Related Concepts

- [[C - Price System as Information Mechanism]] — the mechanism by which a market economy reveals and continuously updates opportunity costs across many competing uses simultaneously.
- [[C - Seen vs Unseen (Broken Window Fallacy)]] — a specific failure mode of opportunity-cost reasoning: crediting a visible transaction with creating value while ignoring the unseen alternative use of the same resources it displaced.

## 7. Pitfalls

- Confusing opportunity cost with sunk cost: money or effort already spent and unrecoverable is not an opportunity cost of a forward-looking decision and should not influence it, even though it often does in practice (sunk-cost fallacy).
- Opportunity cost requires a genuine, available alternative — citing a purely hypothetical or infeasible alternative overstates the true cost of a choice.

## 8. Minimal Example

- Henry Hazlitt's Robinson Crusoe illustration: a castaway who spends the day building a fire has, by definition, not spent that same day gathering food or building shelter — every hour used for one task is an hour unavailable for every other task, so the "cost" of building the fire is measured in the most valuable alternative use of that day's labor, not in any money spent. Source: [[Economics in One Lesson]], Chapter 15.
