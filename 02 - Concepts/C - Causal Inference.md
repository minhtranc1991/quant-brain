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
---
## 1. Definition

**Causal Inference** is the disciplined process of establishing that intervening on one variable (X) systematically changes the distribution of outcomes of another variable (Y), as distinct from merely observing that X and Y vary together (correlation) — formalized through randomized controlled trials where possible, and through structured argument (e.g. Bradford Hill criteria) and confounder adjustment when randomization is impossible.

## 2. Intuition

- Mechanism: correlation between X and Y can arise from X causing Y, Y causing X (reverse causation), a third variable Z causing both (confounding), or pure coincidence in a large search space (spurious correlation). Causal inference is the set of design and analytical tools for ruling out the non-causal explanations. The most decisive tool is the randomized controlled trial (RCT): by randomly allocating a treatment, all confounders — known and unknown — are balanced between groups on average, so any subsequent difference in outcome can only plausibly be attributed to the treatment or chance, not to a lurking factor.
- What determines which mechanism applies: when randomization is feasible (e.g. clinical trials, A/B tests, agricultural experiments), an RCT is the gold standard and requires: a control group, random allocation, intention-to-treat analysis (analyzing participants by the group they were assigned to, not the group they actually complied with), blinding of participants and assessors, equal treatment of all groups outside the intervention, complete follow-up, and — critically — replication across multiple independent trials (systematic review/meta-analysis) rather than reliance on a single study. When randomization is infeasible or unethical (e.g. studying the effect of smoking, socioeconomic status, or a market-structure change), causal claims from observational data require adjusting for known confounders (stratification/regression) and applying structured criteria such as Bradford Hill's: effect size too large to be explained by plausible confounding, correct temporal ordering, dose-response relationship, a plausible mechanism, and replication across independent studies.
- A specific and important observational trap is Simpson's Paradox: an association can *reverse direction* once a confounding factor is properly accounted for (e.g. an admissions dataset showing a higher overall acceptance rate for one group, while every individual subject shows the opposite pattern, because the group disproportionately applied to more competitive subjects). This shows that naive aggregate correlations can actively mislead in the presence of unaddressed confounding, not merely fail to be informative.

## 3. Mathematical perspective (if applicable)

$$\text{observation} = \text{deterministic model} + \text{residual error}$$

Multiple regression adjusts an estimated relationship for confounders by including them as additional explanatory variables (see [[M - Regression Analysis]]); the Bradford Hill criteria are a structured, non-formulaic checklist rather than a single equation.

## 4. When it matters

- Distinguishing a genuine causal driver of returns (e.g. a real risk premium or structural market inefficiency) from a confounded or reverse-causal correlation (e.g. a factor that merely proxies for a period-specific macro regime, or a "liquidity causes returns" claim that is actually "high-quality assets attract both liquidity and returns").
- Evaluating any claim that a policy, product feature, or trading-system change "caused" an observed change in outcome (e.g. before/after comparisons around a venue's fee-structure change) — before/after comparisons alone cannot rule out regression to the mean or a confounded macro shift; see [[C - Regression to the Mean]].
- Assessing observational research (most quantitative-finance and economics empirical work is observational, not experimental) — Bradford Hill-style reasoning, not raw correlation, is the appropriate standard for provisional causal claims.

## 5. Formalized By (Models)

- [[M - Regression Analysis]] — multiple regression is the standard tool for adjusting an estimated association for observed confounders in observational causal-inference work.

## 6. Related Concepts

- [[C - Regression to the Mean]] — a specific statistical mechanism that is frequently mistaken for a genuine causal effect in before/after comparisons (e.g. crediting an intervention for a decline that would have reverted anyway).
- [[C - Selection Bias (Sampling Validity)]] — a distinct threat to valid inference (concerning who/what ends up in the observed sample) that compounds with confounding as a source of misleading observational conclusions.
- [[C - Efficient Market Hypothesis]] — claims that a specific informational or structural factor "causes" abnormal returns must be evaluated against the same causal-inference discipline (ruling out confounding, selection, and reverse causation) before being accepted as evidence against market efficiency.

## 7. Pitfalls

- "Correlation does not imply causation" is necessary but not sufficient guidance — the harder and more useful discipline is knowing *which* structured method (RCT design, confounder adjustment, Bradford Hill reasoning) is appropriate given what randomization is actually feasible.
- Reverse causation is easy to overlook: a documented example is a widely reported claim that proximity to a premium supermarket chain "adds" tens of thousands of pounds to nearby house prices, when the more plausible direction is that the chain deliberately opens stores in already-wealthier areas.
- Adjusting for a confounder in a regression can only correct for *observed and measured* confounders; unmeasured ("lurking") factors remain a threat to any observational causal claim, which is precisely why randomization is preferred whenever ethically and practically feasible.

## 8. Minimal Example

- The UK Heart Protection Study randomly allocated over 20,000 people to a statin or a placebo and found a 27% relative reduction in heart attacks (P ≈ 1 in 3 million) under intention-to-treat analysis; this randomized design is what allows the reduction to be attributed to the statin itself rather than to who chose to take it, in contrast with purely observational studies of statin users versus non-users, which would be vulnerable to confounding by health-consciousness or baseline risk. Source: [[The Art of Statistics - Learning From Data]], Chapter 4.
