---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - behavioral-finance
  - status/needs-review
layer: concept
type: core
domain:
  - behavioral-finance
  - investing
---
## 1. Definition

**Endowment Effect** is the empirical finding that once an individual owns a good, the minimum price they demand to give it up (willingness-to-accept, WTA) is substantially higher than the maximum price they would have paid to acquire the identical good beforehand (willingness-to-pay, WTP) — mere ownership inflates a good's subjective value.

## 2. Intuition

- Mechanism: the effect is a direct behavioral prediction of [[C - Loss Aversion]] — once a good is owned, the reference point shifts to include it, so giving it up is coded as a *loss* (felt strongly, per loss aversion's asymmetric weighting) rather than as the foregone *gain* of simply not having acquired it in the first place. Because losses are felt more intensely than equivalent gains, the same object is valued more highly once it is owned.
- Classic demonstration (the "mug experiment"): randomly assign half of a group a mug, then ask owners the minimum price they would sell it for and non-owners the maximum price they would pay for an identical mug — owners' median selling price is typically roughly double non-owners' median buying price for the physically identical object, even though standard economic theory (with no income effects at this scale) predicts the two prices should coincide.
- What determines whether the effect appears: it is specifically absent for goods held purely for exchange or resale — a trader's inventory held explicitly to sell, or cash itself — because no reference-point attachment to that specific unit develops when the good was never intended to be "kept." The effect is strongest for goods acquired for use or held with some sense of personal ownership, not for goods that are functionally interchangeable tokens of value from the outset.

## 3. Mathematical perspective (if applicable)

_(Not formalized separately from [[M - Prospect Theory]]'s value function — the WTA/WTP gap is a direct consequence of that function's loss-aversion coefficient $\lambda$: the same unit of "giving up the mug," evaluated on the steeper loss branch of the value function, requires a larger price to offset it than the equivalent "acquiring the mug," evaluated on the shallower gain branch.)_

## 4. When it matters

- Explains investors' documented reluctance to sell an inherited or long-held position even when a fresh, unbiased analysis would not choose to buy that same position today — ownership itself, not current fundamentals, inflates the position's subjective value (a distinct mechanism from, but frequently compounding with, the disposition effect documented in [[C - Loss Aversion]]).
- A caution for portfolio-construction and rebalancing discipline: a rules-based rebalancing process that evaluates each holding on the same footing as a potential new purchase (rather than granting incumbency an automatic status-quo advantage) is one structural way to counteract the endowment effect.
- Relevant to negotiation and market-making: a market-maker or counterparty's minimum acceptable sale price for an owned position is not a neutral estimate of fair value — it is inflated by the endowment effect relative to what an equally-informed non-owner would pay for the same asset.

## 5. Formalized By (Models)

- [[M - Prospect Theory]] — the endowment effect is a direct behavioral prediction of the value function's loss-aversion coefficient (see Mathematical perspective above).

## 6. Related Concepts

- [[C - Loss Aversion]] — the endowment effect is one specific behavioral prediction of loss aversion (the WTA/WTP asymmetry), classically treated in the literature as a distinct, separately-named effect from the disposition effect, though both derive from the same underlying mechanism.

## 7. Pitfalls

- The endowment effect is not universal to all owned goods — it does not reliably appear for goods held purely for exchange/resale (cash, trading inventory held explicitly to sell), so it should not be assumed to apply uniformly across every kind of asset ownership.
- It is easy to conflate the endowment effect with simple status-quo bias (general inertia/preference for the current state) or with the disposition effect (reluctance to realize a loss); the endowment effect specifically concerns the WTA/WTP valuation gap for an owned good, independent of whether that good has gained or lost value since acquisition.

## 8. Minimal Example

- In the canonical mug experiment, owners of a randomly-assigned mug set a median selling price roughly twice the median buying price non-owners were willing to pay for the identical mug — a gap not predicted by standard rational-choice theory, which assumes WTA and WTP should coincide for a good with no meaningful income effect at that price scale. Source: [[Thinking, Fast and Slow]], Chapter 27.

#status/needs-review
