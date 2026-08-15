---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - behavioral-finance
layer: concept
type: core
domain:
  - behavioral-finance
  - investing
---
## 1. Definition

**Loss Aversion** is the empirical finding that losses are felt as more painful than equivalent-sized gains are felt as pleasurable — Kahneman and Tversky's experiments estimate the ratio at roughly 2.5:1 — such that decisions are driven more by avoiding losses than by pursuing equally-sized gains. It is the core behavioral input to [[M - Prospect Theory]].

## 2. Intuition

- Mechanism: value is assessed relative to a reference point (typically the status quo or purchase price), and the value function is steeper for losses than for gains of the same magnitude. A fair coin-flip gamble (50% chance of +$100, 50% chance of -$100, expected value $0) is rejected by most people; Kahneman and Tversky found the positive payoff had to rise to roughly $250 (expected value +$75) before most subjects would accept the bet — direct evidence of the asymmetric weighting of losses versus gains.
- A key behavioral consequence in investing: the "disposition effect" — investors tend to sell winning positions (to lock in the pleasure of being "right") and hold losing positions (to avoid the pain of realizing a loss and admitting a mistake), even though this is tax-inefficient (short-term gains are taxed at higher rates, and realized losses can offset other gains) and contrary to the rational prescription. The book documents this directly in a large brokerage-account study (Barber and Odean).
- Loss aversion interacts with framing: when the *same* underlying outcome is presented as a loss rather than a gain, choices change — e.g. subjects are risk-averse for a "200 of 600 saved" framing but risk-seeking for the logically identical "400 of 600 will die" framing (Kahneman-Tversky's Asian disease experiment). This shows the effect is triggered by how a decision is described, not solely by its objective structure.

- **Enrichment — negativity dominance, the broader basis for loss aversion ([[Thinking, Fast and Slow]]):** loss aversion is one specific instance of a more general "negativity dominance" feature of the mind. Across many independent lines of evidence (faster facial-threat recognition than facial-pleasure recognition, negotiation research, marital-relationship-quality studies finding good interactions must outnumber bad ones roughly five-to-one to sustain relationship satisfaction), bad events and information are registered faster, weighted more heavily, and harder to reverse in effect than good events of comparable magnitude — implying the asymmetry in financial loss aversion is not a narrow economic quirk but an expression of a broad, evolutionarily-plausible cognitive design feature. Source: [[Thinking, Fast and Slow]], Chapter 28.
- **Enrichment — mental accounting and the sunk-cost fallacy, reinforcing the disposition effect ([[Thinking, Fast and Slow]]):** mental accounting — tracking money in separate, non-fungible psychological "accounts" rather than as a single fungible pool (e.g. treating gambling winnings, or "house money" from an earlier win, as more disposable than equivalent salary income) — produces the sunk-cost fallacy (continuing a losing course of action partly to avoid the finality of closing that account at a realized loss) and reinforces the disposition effect documented below: a paper loss can be held indefinitely partly because realizing it means closing (and finalizing the regret of) that specific mental account, not only because of the loss's raw financial magnitude. Source: [[Thinking, Fast and Slow]], Chapter 32.

## 3. Mathematical perspective (if applicable)

$$v(x) = \begin{cases} x^{\alpha} & x \geq 0 \\ -\lambda(-x)^{\beta} & x < 0 \end{cases}, \quad \lambda \approx 2.25$$

The prospect-theory value function $v(x)$ (Kahneman-Tversky's original specification) is concave for gains, convex for losses, and steeper for losses by a loss-aversion coefficient $\lambda$ (the book's narrative estimate of "2.5x" is a rounded description of this coefficient; the canonical academic estimate is closer to 2.25). See [[M - Prospect Theory]] for the full model.

## 4. When it matters

- Explains why investors refuse to enroll in retirement savings plans that reduce take-home pay (each dollar of increased contribution is felt as a loss of current spending), motivating "opt-out" auto-enrollment and the Thaler-Benartzi "Save More Tomorrow" plan design (Chapter 10).
- Explains sellers' reluctance to sell homes or stocks at a loss even when holding is not the rational choice, both in equities and in residential real estate.

## 5. Formalized By (Models)

- [[M - Prospect Theory]] — the formal mathematical model in which loss aversion is one component (alongside probability weighting and reference-dependence).

## 6. Related Concepts

- [[C - Overconfidence Bias]] — a separate but co-occurring source of investor irrationality covered in the same chapter.
- [[C - Limits to Arbitrage]] — loss-averse, regret-avoiding behavior is one of the behavioral inputs that can sustain mispricing which rational arbitrage does not fully correct.
- [[C - Endowment Effect]] — a distinct, separately-named behavioral prediction of loss aversion (the willingness-to-accept/willingness-to-pay valuation gap for an owned good), classically treated apart from the disposition effect though both derive from the same underlying value-function asymmetry.

## 7. Pitfalls

- Loss aversion is often conflated with simple risk aversion; they are distinct — prospect theory (and the "sure loss vs. gamble" experiment, where ~90% of subjects chose a risky gamble over a sure loss of identical expected value) shows people can be *risk-seeking* in the domain of losses, which plain risk aversion cannot explain.
- A "paper loss" (an unrealized decline in a held position) is economically identical to a realized loss for decision-making purposes (the decision to keep holding is equivalent to a fresh decision to buy at the current price), but loss aversion makes investors treat the two very differently.

## 8. Minimal Example

- The disposition effect study of 10,000 discount-brokerage clients (Barber and Odean) found a clear, statistically pronounced tendency to sell winning stocks and hold losing stocks — the empirical signature of loss aversion in real trading behavior. Source: [[A Random Walk Down Wall Street]], Chapter 10.
- **Enrichment — the theory's originator's own account ([[Thinking, Fast and Slow]]):** Kahneman and Tversky's rejected-fair-gamble experiment (subjects require the gain side of a 50/50 bet to rise to roughly $250 against a $100 loss before accepting) is the same finding this note's Intuition section already documents, now grounded directly in the originating source rather than only in Malkiel's secondhand summary. Source: [[Thinking, Fast and Slow]], Chapter 26.

#status/needs-review
