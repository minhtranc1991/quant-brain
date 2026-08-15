---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - behavioral-finance
layer: model
type: core
domain:
  - behavioral-finance
  - statistics
---
## 1. Definition

**Prospect Theory** is a mathematical model that formalizes [[C - Loss Aversion]] and related departures from rational expected-utility decision-making — developed by Daniel Kahneman and Amos Tversky (Kahneman won the 2002 Nobel Memorial Prize in Economic Sciences for this work) — describing how individuals actually evaluate risky choices: relative to a reference point rather than final wealth, with losses weighted more heavily than equivalent gains, and with the framing of a choice (as a gain versus a loss) materially affecting the decision made.

## 2. Intuition

- Standard financial economics (e.g. Markowitz's original MPT formulation) models decisions as maximizing expected utility of *final wealth*. Prospect theory instead models decisions as evaluated relative to a *reference point* (commonly the status quo), with a value function that is concave for gains (diminishing sensitivity — the difference between gaining $100 and $200 feels smaller than the difference between gaining $0 and $100), convex for losses (same diminishing-sensitivity logic mirrored below the reference point), and steeper for losses than for gains of the same magnitude (loss aversion).
- Direct experimental evidence for the loss-aversion asymmetry: subjects reject a fair 50/50 gamble of +$100/-$100 (expected value $0), and the positive payoff has to rise to roughly $250 (expected value +$75, a strongly favorable bet) before most subjects accept — implying losses are felt roughly 2.5x as strongly as equivalent gains.
- A further, less intuitive prediction confirmed experimentally: people are risk-*seeking*, not risk-averse, when choosing among sure losses. Given "a sure loss of $750" versus "75% chance of losing $1,000, 25% chance of losing nothing" (equal expected value), about 90% of subjects chose the gamble — the opposite of the risk-averse pattern typically found for gains. This reversal (risk-averse for gains, risk-seeking for losses) is a signature prediction that distinguishes prospect theory from standard expected-utility theory, which cannot naturally produce it without an ad hoc, separately-fitted utility curvature for losses.
- Framing effect: logically identical outcomes described in terms of "lives saved" versus "lives lost" (the Kahneman-Tversky "Asian disease" experiment) produce systematically different choices — about two-thirds choose the safe option under a "saved" framing but over three-quarters choose the risky option under an equivalent "die" framing — showing that *how* a choice is described, not only its objective payoff structure, drives the decision.

## 3. Mathematical perspective

$$v(x) = \begin{cases} x^{\alpha} & x \geq 0 \\ -\lambda(-x)^{\beta} & x < 0 \end{cases}$$

Where $x$ is a gain or loss relative to the reference point, $\alpha, \beta \in (0,1)$ produce diminishing sensitivity (concave for gains, convex for losses), and $\lambda$ (commonly estimated around 2.25, and reported narratively in the source as approximately 2.5) is the loss-aversion coefficient making the value function steeper for losses than gains. _(The book presents the empirical loss-aversion ratio and the risky-choice experiments narratively; this value-function formalization is the standard academic specification of the theory it describes, not a formula given explicitly in the source text.)_

## 4. Assumptions

- Decisions are made relative to a subjective reference point (often, but not always, the status quo or original purchase price), not relative to final absolute wealth.
- The value function's shape (loss aversion, diminishing sensitivity) is treated as a stable, general feature of human decision-making under risk, rather than a one-off experimental artifact — supported in the source by replication across driving-skill, interpersonal-skill, and financial-decision contexts.

## 5. Estimation / Training Procedure

- The loss-aversion coefficient and value-function curvature are estimated experimentally by varying gamble payoffs until subjects' choices switch (as in the +$100/-$100 vs. +$250/-$100 gamble-acceptance experiment) — a revealed-preference elicitation method rather than a statistical fit to market data in the source's presentation.

## 6. When it matters in Finance

- Directly explains the "disposition effect" (selling winners, holding losers) documented in real brokerage-account data, and household reluctance to increase retirement-plan contributions (each dollar of increased contribution is coded as a loss of current spending) — motivating auto-enrollment/"opt-out" plan design and the Thaler-Benartzi "Save More Tomorrow" program.
- Provides the theoretical basis for [[C - Loss Aversion]] as an investor-behavior Concept and for several of the book's practical "avoid these investor mistakes" recommendations (Chapter 10).

## 7. Based On Concepts

- [[C - Loss Aversion]]

_(Model → Concept `based_on` edge: prospect theory is the formal model; loss aversion is the Concept it is built to explain and quantify.)_

## 8. Related Models

- _(No other Model in this vault currently extends/depends on/specializes prospect theory.)_

## 9. Used In Strategies

- _(No Strategy note in this vault currently implements prospect theory directly; the book uses it to explain investor behavior and motivate practical discipline rules rather than as the basis for a specific tradeable strategy.)_

## 10. Limitations / Pitfalls

- Prospect theory describes *how* people actually decide, not how they *should* decide — it is a positive (descriptive), not normative, model; the book uses it to diagnose costly investor mistakes (the disposition effect, procrastination in saving), not to justify them.
- The book presents the loss-aversion ratio (~2.5x) as an empirical regularity from Kahneman-Tversky's original experiments rather than a universal constant; it should be read as an approximate, replicated order-of-magnitude finding, not a precise, context-independent parameter.

## 11. Minimal Example

- The Asian disease framing experiment: identical expected outcomes (200 of 600 people saved / 400 of 600 people die) produce opposite majority choices depending on whether the option is framed in terms of "saved" (risk-averse majority choice) or "die" (risk-seeking majority choice) — demonstrating that framing alone, holding the underlying probabilities and payoffs fixed, changes the decision. Source: [[A Random Walk Down Wall Street]], Chapter 10.
