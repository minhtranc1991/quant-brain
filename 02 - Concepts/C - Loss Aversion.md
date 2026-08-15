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

## 7. Pitfalls

- Loss aversion is often conflated with simple risk aversion; they are distinct — prospect theory (and the "sure loss vs. gamble" experiment, where ~90% of subjects chose a risky gamble over a sure loss of identical expected value) shows people can be *risk-seeking* in the domain of losses, which plain risk aversion cannot explain.
- A "paper loss" (an unrealized decline in a held position) is economically identical to a realized loss for decision-making purposes (the decision to keep holding is equivalent to a fresh decision to buy at the current price), but loss aversion makes investors treat the two very differently.

## 8. Minimal Example

- The disposition effect study of 10,000 discount-brokerage clients (Barber and Odean) found a clear, statistically pronounced tendency to sell winning stocks and hold losing stocks — the empirical signature of loss aversion in real trading behavior. Source: [[A Random Walk Down Wall Street]], Chapter 10.
