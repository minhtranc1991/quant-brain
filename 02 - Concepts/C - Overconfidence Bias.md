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

**Overconfidence Bias** is the systematic tendency of individuals to overestimate the accuracy of their own beliefs/forecasts and their own skill relative to others, and to underestimate the role of chance and the risks involved in their decisions.

## 2. Intuition

- Mechanism: people set probability judgments (confidence intervals) that are far too narrow relative to their actual forecasting accuracy. In Kahneman's calibration experiments, subjects asked to state a range they were 98% confident would contain a future value (e.g. the Dow Jones one month out) were wrong roughly 20% of the time rather than the expected ~2% — meaning their *stated* confidence vastly exceeded their *actual* accuracy.
- Compounding mechanisms identified in the source: (1) hindsight bias — selective memory of successful calls, combined with a tendency to attribute good outcomes to skill and bad outcomes to bad luck, sustains the illusion of predictive skill after the fact; (2) the representativeness heuristic — people substitute "does this look like a typical member of category X" for genuine probabilistic reasoning (the "Linda the bank teller" experiment), leading to systematic misjudgment of likelihood and, in investing, to chasing recently hot funds or overreacting to recent evidence; (3) illusion of control — people believe they have influence over outcomes that are in fact random (demonstrated with a rigged, non-functional control device in a lab task), which in investing manifests as false confidence in the ability to time markets or "spot" chart patterns.
- What determines the *degree* of overconfidence: the book reports that men display measurably more overconfidence than women, particularly in money matters, and that more overconfident investors trade more frequently and earn correspondingly worse net returns (Barber and Odean).

- **Enrichment — the narrative fallacy, and the mechanism behind hindsight bias ([[Thinking, Fast and Slow]]):** Kahneman names and generalizes the mechanism this note's hindsight-bias bullet already gestures at. The mind's compulsion to construct coherent, causally satisfying stories about why past outcomes occurred (e.g. attributing a company's success entirely to its CEO's specific traits and decisions) is a "narrative fallacy" — the same successful-company traits praised in retrospective business-book case studies are frequently found, on closer study, to characterize later-failing companies equally well, showing the narrative explains the outcome only because the outcome is already known. This combines with hindsight bias (systematically revising, after the fact, one's sense of how predictable an outcome "really" was) to create the illusion that past events were more understandable, and future events more predictable, than the evidence actually supports. Source: [[Thinking, Fast and Slow]], Chapter 19.
- **Enrichment — Kahneman's own field evidence: the illusion of validity among professional stock pickers ([[Thinking, Fast and Slow]]):** in a documented consulting engagement, Kahneman found the year-to-year correlation between individual stock pickers' investment results at a major investment firm was close to zero — statistically indistinguishable from a game of chance — yet the firm's own bonus and promotion decisions, and the pickers' own subjective sense of skill, proceeded as though genuine, differentiated skill were being measured and rewarded. Demonstrating this statistical fact directly to the firm's traders and executives did not change their behavior or their felt confidence. This "illusion of validity" — a strong subjective sense of judgmental skill produced by System 1's WYSIATI-driven coherent impressions (see [[F - System 1 and System 2 (Dual-Process Thinking)]]) — can survive direct confrontation with disconfirming statistical evidence, and is direct investment-industry field evidence complementing the calibration-experiment and Barber/Odean trading-frequency evidence already documented above. Source: [[Thinking, Fast and Slow]], Chapter 20.
- **Enrichment — optimism bias and competition neglect ([[Thinking, Fast and Slow]]):** entrepreneurial and business risk-taking is driven substantially by "optimism bias" — a durable, largely unlearnable overestimation of one's own odds of success relative to others attempting similar ventures. Founders routinely and correctly cite general small-business failure base rates for "businesses like theirs" while simultaneously, and without contradiction, believing their own specific venture faces much better odds ("competition neglect" — underweighting that competitors are, on average, equally skilled, equally resourced, and equally confident). This same mechanism plausibly underlies overconfident extrapolation of high earnings-growth forecasts for "story" growth stocks (see [[C - Castle in the Air Theory]] and, in plain-text form, the Value Investing strategy note's Alpha Logic). Source: [[Thinking, Fast and Slow]], Chapter 24.

## 3. Mathematical perspective (if applicable)

_(Not applicable in this source — overconfidence is documented via calibration-experiment and trading-behavior evidence, not a formal mathematical model. Its consequences for decision-making under risk are partially formalized by [[M - Prospect Theory]], though prospect theory addresses loss aversion/framing specifically rather than overconfidence itself.)_

## 4. When it matters

- Explains why individual investors trade more than is optimal (a disciplined, rules-based rebalancing schedule is presented in the source as an alternative to discretionary trading) and why growth-stock overvaluation can arise from overconfident extrapolation of high earnings-growth forecasts (linking to [[C - Castle in the Air Theory]]).
- A key input to the book's practical "Avoid Overtrading" lesson (Chapter 10).

## 5. Formalized By (Models)

- _(No dedicated formal overconfidence Model exists yet in this vault.)_

## 6. Related Concepts

- [[C - Herd Behavior]] — a separate but co-occurring source of investor irrationality identified alongside overconfidence.
- [[C - Loss Aversion]] — the other major Kahneman-Tversky-derived bias covered in the same chapter.
- [[C - Random Walk Hypothesis]] — overconfidence in the ability to detect patterns is precisely what the coin-toss chart experiment (Ch. 6) is designed to expose as illusory.
- [[F - System 1 and System 2 (Dual-Process Thinking)]] — the WYSIATI mechanism (coherent impressions built from whatever limited evidence is available, insensitive to its quality/quantity) is the structural root of the illusion of validity and narrative fallacy documented above.
- [[C - Algorithmic Judgment vs. Expert Intuition]] — the illusion-of-validity finding (confident-feeling but statistically absent skill) is the direct behavioral counterpart to that Concept's finding that expert confidence is not a valid signal of genuine predictive skill.
- [[C - Anchoring]] — a related but distinct System-1-driven judgment bias; see that note for the mechanism.

## 7. Pitfalls

- Overconfidence is not limited to unsophisticated investors — the book's driving-skill and interpersonal-skill self-ranking experiments (Peters and Waterman's *In Search of Excellence* survey, where 100% of respondents ranked themselves in the top half for getting along with others) show the bias is close to universal, not a marker of naivety alone.

## 8. Minimal Example

- Barber and Odean's study of ~66,000 households (1991-96) found the average household earned 16.4% annually versus the market's 17.9%, while the households that traded *most* actively earned only 11.4% — direct evidence linking overconfidence-driven overtrading to worse net investment outcomes. Source: [[A Random Walk Down Wall Street]], Chapter 10.
- **Enrichment — a cognitive-style predictor of forecasting overconfidence ([[The Signal and the Noise]]):** political scientist Philip Tetlock's multi-year study of expert political forecasters (published as *Expert Political Judgment*, 2005) found experts performed close to chance overall (roughly 15% of events they called impossible occurred; roughly 25% of events they called certain sure things failed to occur) — but a specific cognitive-style distinction predicted individual accuracy. "Hedgehog"-style experts (committed to one totalizing framework, resistant to revising it when new evidence arrived, and more frequently cited in media) forecast substantially worse than "fox"-style experts (multidisciplinary, adaptive, self-critical, comfortable with uncertainty and dissenting evidence) — media prominence itself was inversely correlated with forecasting accuracy. This adds a specific, testable predictor of *which* forecasters are more overconfident, complementing the general mechanisms (hindsight bias, representativeness, illusion of control) already documented above. Source: [[The Signal and the Noise]], Chapter 2.
- **Enrichment — false precision as a distinct overconfidence signature ([[The Signal and the Noise]]):** credit ratings agencies' pre-2008 CDO default models expressed default probabilities to two decimal places (e.g. 0.12%) despite modeling a genuinely novel, poorly understood instrument — conflating *uncertainty* (risk that cannot be reliably measured, per economist Frank Knight's 1921 distinction) with *risk* (a quantifiable, known probability). Precision is not the same as accuracy: a highly precise-looking estimate can still be wildly wrong, and the appearance of quantitative rigor can itself become a distinct driver of unwarranted confidence, both for the forecaster and for those relying on the forecast. See [[CS - 2008 Financial Crisis - Ratings Agencies' Model Failure]]. Source: [[The Signal and the Noise]], Chapter 1.
- **Enrichment — herding as a distinct, incentive-driven (not purely cognitive) source of poor forecasts ([[The Signal and the Noise]]):** professional macroeconomic forecasters exhibit a systematic herding/anchoring bias distinct from simple overconfidence: individual career risk is minimized by forecasting close to consensus and close to a simple extrapolation of the recent trend, even when a forecaster privately believes the true outlook differs — a rational individual response to career incentives that nonetheless degrades the collective informativeness of published forecasts. Source: [[The Signal and the Noise]], Chapter 6.
- **Enrichment — Kahneman's own field evidence, and the theory's originator's account ([[Thinking, Fast and Slow]]):** see the illusion-of-validity, narrative-fallacy, and optimism-bias/competition-neglect content added to the Intuition section above, all sourced from the same author whose research the "representativeness heuristic" and "illusion of control" mechanisms already cited in this note originate from.

#status/needs-review
