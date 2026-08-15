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
  - data-analysis
---
## 1. Definition

**P-Hacking** is the practice — whether deliberate or an unrecognized byproduct of ordinary flexible analysis — of exploiting undisclosed choices in data collection, exclusion, and analysis ("researcher degrees of freedom") to obtain a statistically significant result, which inflates the true false-positive rate of a research process far beyond the nominal per-test significance threshold.

## 2. Intuition

- Mechanism: the most direct form is literal multiple testing — running many formally separate significance tests and reporting only the most significant one(s). If a null hypothesis is actually true, each individual test at threshold P < 0.05 has only a 5% chance of a false positive, but running ten such tests raises the chance of at least one false "significant" result to roughly 40%; an extreme demonstration found "statistically significant" brain activity (P < 0.001) at 16 of 8,064 tested brain sites in an fMRI scan of a dead salmon, purely from the sheer number of tests performed.
- A subtler and more pervasive mechanism is "researcher degrees of freedom" (also called "the garden of forking paths" or HARKing — Hypothesizing After the Results are Known): undisclosed flexible choices made *during* data collection and analysis — when to stop collecting more data, which data points or subgroups to exclude, which of several possible outcome variables or covariates to report, how to code or bin a continuous variable — each individually defensible, but collectively multiplying the effective number of "tests" performed without this being visible in the final reported P-value. A 2012 survey found 94% of academic psychologists admitted to at least one such practice (e.g. 58% had continued collecting data after checking interim significance; 67% had failed to report all of a study's response variables).
- What determines whether flexibility is legitimate: the distinction between exploratory studies (deliberately flexible investigations intended to generate hypotheses, where such practices are appropriate) and confirmatory studies (which must follow a pre-specified, ideally pre-registered, protocol to produce a valid, interpretable P-value). The failure mode is not flexibility itself, but *presenting* an exploratory, flexibly-derived result with the evidentiary weight of a confirmatory one.

## 3. Mathematical perspective (if applicable)

For $n$ independent tests of a truly null effect at per-test significance level $\alpha$, the probability of at least one false-positive "discovery" is:

$$P(\text{at least one false positive}) = 1 - (1-\alpha)^n$$

which grows quickly with $n$ (e.g. ≈40% for $n=10$ tests at $\alpha = 0.05$). The Bonferroni correction counters this by testing each hypothesis at the stricter threshold $\alpha/n$. Publication-bias detection ("P-curve" analysis) exploits a related mathematical fact: under a true null hypothesis, P-values that happen to fall below 0.05 by chance should scatter roughly uniformly across (0, 0.05); a genuine effect instead skews these P-values toward smaller values, and a suspicious cluster of P-values just below 0.05 is itself a detectable signature of selective reporting.

## 4. When it matters

- Systematic strategy/signal research is structurally identical to the many-hypothesis-testing setting this Concept describes: testing many candidate signals, parameter combinations, or lookback windows against historical data and reporting only the profitable ones is a direct analogue of the dead-salmon multiple-testing failure, and requires the same corrections (holdout/out-of-sample testing, pre-registration of the hypothesis before testing, correction for the number of combinations tried) — this is the primary quantitative-research application of [[C - Overfitting]] and P-hacking together.
- Evaluating any published trading-strategy or factor-discovery claim: absent disclosure of how many variants, lookback periods, or universes were tried before arriving at the reported result, the stated statistical significance materially overstates the true evidentiary strength of the finding.
- Distinguishing genuinely pre-registered, out-of-sample-validated research from post-hoc rationalized ("HARKed") narratives fitted to already-known historical outcomes.

## 5. Formalized By (Models)

- [[M - Null Hypothesis Significance Testing]] — the Bonferroni correction and the broader multiple-testing/Type-I-error-inflation mathematics are formalized directly within this Model's machinery.

## 6. Related Concepts

- [[C - Overfitting]] — a closely related but distinct failure mode: Overfitting is a property of a single model adapted too closely to one dataset (a modelling/estimation problem); P-Hacking is a property of the broader research *process* — the selective search over many analyses, models, or subgroups and reporting only the favorable outcome (a reporting/inference problem). The two frequently compound (e.g. trying many overfit models and then P-hacking by reporting only the best one).
- [[C - Survivorship Bias]] — both inflate apparent success rates through selective visibility, but Survivorship Bias concerns which *entities* remain observable in a population, while P-Hacking concerns which *analyses* get reported from a single research process.

## 7. Pitfalls

- Deliberate fraud (data fabrication) is thought to be comparatively rare (roughly 2% of researchers admit to it in anonymous surveys); P-hacking via undisclosed researcher degrees of freedom is far more common and often not experienced by the researcher as dishonest — it is a subtler, structural problem requiring procedural safeguards (pre-registration, disclosure of all analyses attempted) rather than only an appeal to individual integrity.
- A P-hacked or overfit result frequently shows "regression to the null" upon replication: the Reproducibility Project's replication of 100 psychology studies found that while 97% of original studies reported statistically significant results, only 36% of replications did, and even successfully replicated effects were on average roughly half the magnitude of the original — a documented signature of this Concept operating at the level of an entire research literature, not just isolated studies.
- Absence of a "significant" result is routinely misreported as proof of "no effect" in media coverage, which is itself a distinct error (see [[M - Null Hypothesis Significance Testing]]'s Limitations) but compounds with P-hacking's opposite error to produce a generally unreliable pipeline from raw finding to public claim.

## 8. Minimal Example

- A deliberate demonstration study randomized subjects to a standard, low-carb, or low-carb-plus-chocolate diet with only 5 subjects per group, measured a large number of outcome variables, and reported (accurately, but selectively) that the chocolate group's weight loss exceeded the low-carb group's by 10% (P = 0.04) — sufficient to be published as an "outstanding manuscript" and covered internationally under headlines like "Chocolate Accelerates Weight Loss," before the authors revealed the study was a deliberate exposure of exactly this failure mode: a small sample, many measured outcomes, and only the significant one reported. Source: [[The Art of Statistics - Learning From Data]], Chapter 12.
