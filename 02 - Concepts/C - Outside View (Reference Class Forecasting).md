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
  - risk-management
---
## 1. Definition

**Outside View (Reference Class Forecasting)** is a forecasting discipline that constructs an estimate by treating the case at hand as one instance of a broader reference class of similar past cases and using that class's actual historical outcome distribution as the starting forecast — contrasted with the "inside view," which forecasts by focusing on the specific case's unique details and constructing a plausible scenario for it.

## 2. Intuition

- Mechanism: the inside view is System 1's default mode — it constructs the most coherent, plausible-feeling scenario for the specific case's unique circumstances (per [[F - System 1 and System 2 (Dual-Process Thinking)]]'s WYSIATI mechanism), and that constructed scenario is almost always more optimistic than the actual base-rate outcome distribution of similar past cases, because the scenario-builder cannot fully imagine every way an unfamiliar future could go wrong. The outside view corrects this by deliberately identifying an appropriate reference class of similar past cases first, anchoring the forecast on that class's actual track record, and adjusting only modestly for genuinely diagnostic case-specific information.
- The inside view's characteristic failure mode is the **planning fallacy** — plans and forecasts unrealistically close to best-case scenarios (project timelines, budgets, strategy-capacity or return expectations) — which persists even among forecasters who correctly cite the general failure-rate base rate for "projects/ventures like this one" while exempting their own specific case from it (see [[C - Overconfidence Bias]]'s optimism-bias/competition-neglect content).
- What determines the outside view's usefulness: it requires a genuinely comparable, well-populated reference class to exist and be correctly identified — an outside view built from a poorly-matched or too-narrow reference class can be as misleading as an unconstrained inside view, so reference-class selection is itself a judgment call that can be done well or badly.

## 3. Mathematical perspective (if applicable)

_(Not formalized as a single model in the source — described as a forecasting procedure: identify a reference class, obtain its outcome distribution as a baseline, then adjust the baseline only by the strength of genuinely diagnostic case-specific evidence, similar in spirit to Bayesian base-rate anchoring; see [[M - Bayesian Inference]] for the formal base-rate mechanism this procedure operationalizes.)_

## 4. When it matters

- Directly applicable to quantitative research and strategy development: estimating a new strategy's expected live performance, capacity, or drawdown risk from the reference class of similarly-structured strategies' actual historical live (not backtested) results is an outside-view discipline that corrects for the inside-view optimism a backtest-focused, case-specific narrative tends to produce.
- Project and timeline estimation for research/infrastructure work: estimating how long a model-development or infrastructure project will actually take from the reference class of "how long similar past projects here actually took," rather than from a scenario built around this project's specific plan, is the direct antidote to the planning fallacy.
- Complements, rather than duplicates, [[C - Algorithmic Judgment vs. Expert Intuition]]: that Concept concerns *who* (formula vs. expert) should make a prediction; the outside view concerns *which reference frame* the prediction — whether made by a human or a formula — should be anchored to.

## 5. Formalized By (Models)

- _(No dedicated formal Model exists yet in this vault; reference-class base-rate anchoring is conceptually related to prior-distribution construction in [[M - Bayesian Inference]] but is not formalized as its own model here.)_

## 6. Related Concepts

- [[C - Overconfidence Bias]] — the planning fallacy and optimism bias documented there (entrepreneurial overconfidence, competition neglect) are the inside view's characteristic symptom; the outside view is the source's own prescribed corrective procedure.
- [[C - Algorithmic Judgment vs. Expert Intuition]] — a related but distinct forecasting-discipline question (who predicts, vs. what reference frame the prediction uses); see When it matters above.

## 7. Pitfalls

- Choosing a reference class is itself a judgment call — too broad a class dilutes genuinely relevant case-specific information; too narrow a class (or one selected to match a desired conclusion) can reintroduce the same overconfidence the outside view is meant to correct.
- The outside view is a *starting point* correction, not a replacement for all case-specific analysis — the source explicitly recommends adjusting the reference-class baseline using genuinely diagnostic case-specific evidence, not ignoring case-specific information entirely.

## 8. Minimal Example

- A team planning a new curriculum-development project, when asked directly, estimated 2 years to completion; when a team member with experience judging similar past curriculum projects was asked how long comparable past projects (the reference class) had actually taken, the honest reference-class-based answer was that roughly 40% of similar past teams never finished at all, and those that did took 7-10 years — the eventual actual completion time was 8 years, far closer to the outside-view reference-class estimate than to the team's own inside-view plan. Source: [[Thinking, Fast and Slow]], Chapter 23.

#status/needs-review
