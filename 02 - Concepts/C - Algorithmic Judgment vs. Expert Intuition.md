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
  - quantitative-trading
  - decision-making
---
## 1. Definition

**Algorithmic Judgment vs. Expert Intuition** is the finding, originating with Paul Meehl's 1954 review and replicated across roughly 200 subsequent studies, that simple statistical or actuarial formulas built from a small number of consistently-applied predictor variables match or outperform expert human judgment across a wide range of prediction tasks — combined with the identified conditions under which expert intuitive judgment, by contrast, genuinely can be trusted.

## 2. Intuition

- Mechanism (why formulas win): human judgment introduces uncontrolled inconsistency — the same expert reviewing the identical case on different days, in different moods, in a different order of presentation, or under different levels of fatigue can reach different conclusions, even when they have access to strictly *more* case information than a formula uses. A fixed formula, by construction, applies its inputs identically every time; this consistency, not superior insight into any individual case, is the primary source of its advantage. Domains where this has been documented include parole-violation prediction, psychiatric/medical prognosis, business failure prediction, and corporate bond default risk.
- Mechanism (when intuition IS trustworthy — Kahneman and Gary Klein's joint "adversarial collaboration" resolution): expert intuitive judgment can be genuinely reliable, and can outperform simple formulas, under two jointly necessary conditions: (1) the environment must be **sufficiently regular/predictable** to contain learnable, stable patterns (chess, firefighting, many forms of medical diagnosis); (2) the expert must have had **prolonged practice with rapid, unambiguous feedback** that allows genuine skill to be learned from experience (immediate, clear win/loss or right/wrong signals, not delayed or ambiguous outcomes).
- What determines which regime applies: neither the expert's confidence nor their credentials are a valid signal of which regime a given task falls into — confident-feeling expert intuition is common in both genuinely skill-supporting environments and in low-validity, irregular ones (stock picking, long-range political/economic forecasting), where the environment lacks stable learnable patterns and/or feedback is too slow, sparse, or ambiguous for genuine skill to develop, no matter how much experience the practitioner has accumulated.

## 3. Mathematical perspective (if applicable)

_(Not formalized as a single model in the source — the underlying finding is comparative predictive accuracy of simple linear/actuarial models versus expert holistic judgment across many empirical studies, not a single mathematical specification.)_

## 4. When it matters

- Directly bears on the systematic (quantitative, rules-based) vs. discretionary decision-making question central to this vault: a consistently-applied simple model built on a small number of well-chosen, validated inputs is not merely a lower-cost substitute for expert judgment — in low-validity, irregular, or noisy environments it is frequently the *more accurate* choice, independent of the model-builder's or the discretionary trader's relative sophistication.
- Provides a principled criterion for when discretionary judgment should be trusted at all within an otherwise systematic process: only where the sub-task is a sufficiently regular, learnable environment with fast, unambiguous feedback (e.g. some forms of execution timing or market-microstructure pattern recognition) — not for genuinely low-validity forecasting tasks (e.g. long-range macro or stock-picking calls), which more closely resemble the domains where formulas reliably win.
- A caution against over-trusting a live trader's or portfolio manager's self-reported confidence as a proxy for genuine skill — see [[C - Overconfidence Bias]]'s "illusion of validity" content (Kahneman's own investment-firm consulting example) for a direct, documented case of confident-feeling but statistically absent skill in exactly this low-validity domain.

## 5. Formalized By (Models)

- _(No dedicated formal Model exists yet in this vault for actuarial/formula-based prediction as a general technique; a future Model note on simple linear predictive scoring could formalize this Concept's mechanism.)_

## 6. Related Concepts

- [[C - Overconfidence Bias]] — the "illusion of validity" (confident-feeling but statistically unfounded expert judgment) documented there is the direct behavioral counterpart to this Concept's finding that expert confidence is not a valid signal of genuine predictive skill.
- [[C - Outside View (Reference Class Forecasting)]] — a related but distinct forecasting discipline: this Concept concerns whether a formula or an expert should make the prediction; Outside View concerns which reference frame (case-specific "inside" detail vs. a broader reference class) the prediction — by either a human or a formula — should be built from.

## 7. Pitfalls

- This is not a blanket claim that "algorithms always beat humans" — the source is explicit that the advantage is specific to environments where formula consistency matters more than case-specific human insight, and that genuinely skilled intuition exists and can outperform simple formulas in sufficiently regular, fast-feedback environments (see the two-condition test above).
- A formula's advantage comes from consistency, not from access to more or better information than the human judge — giving a human judge a formula's own output as an additional input ("broken-leg" exception cases aside) rather than fully replacing the human with the formula is frequently the best-performing combination in the studied literature, not pure formula-only prediction.

## 8. Minimal Example

- Paul Meehl's original review, and the roughly 200 subsequent studies it inspired across domains from parole-violation prediction to corporate bond default risk, consistently found simple statistical/actuarial formulas matching or exceeding expert clinical judgment's predictive accuracy, even when the human experts had access to more case information than the formula used. Source: [[Thinking, Fast and Slow]], Chapters 21-22.

#status/needs-review
