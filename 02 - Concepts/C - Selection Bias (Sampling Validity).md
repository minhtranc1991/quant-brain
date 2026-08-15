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

**Selection Bias (Sampling Validity)** is the systematic distortion that arises when the process by which data is observed, collected, or retained is not representative of the target population a conclusion is meant to generalize to — so that inference drawn from the observed sample no longer reliably describes the population of actual interest.

## 2. Intuition

- Mechanism: generalizing from data to a claim about the world is a chain — raw data → sample → study population → target population — and each link can silently fail. Measurement/reporting bias corrupts the data-to-sample step (e.g. self-reported figures skewed by social-acceptability bias). Non-random or non-representative recruitment corrupts the sample-to-study-population step (e.g. low-response-rate telephone polls, self-selected online surveys). A restricted or unrepresentative study design corrupts the study-population-to-target-population step (e.g. a drug trial conducted only on adult men, later prescribed to women and children "off-label").
- What determines the size of the distortion: how far the *actual* selection mechanism departs from random sampling, and how strongly the excluded/underrepresented group differs from the included group on the outcome of interest. A well-designed random sample (Gallup's "stir the soup before tasting it" analogy) minimizes this; a convenience sample, a low-response survey, or a "we have all the data that exists" administrative dataset (which can still be a biased slice of a broader phenomenon — e.g. police-recorded crime systematically undercounting unreported offenses) does not.
- Selection bias is a distinct failure mode from measurement bias or genuine population heterogeneity: the data may be recorded perfectly accurately, and the sample may even be very large, and the conclusion can still be wrong purely because of *who* or *what* ended up in the sample. Large sample size does not protect against selection bias — a huge but non-random sample (e.g. thousands of self-selected telephone-poll respondents) can be less reliable than a small, genuinely random one.

## 3. Mathematical perspective (if applicable)

_(Not formalized as a single equation in the source — selection bias is a structural/design property of how data was generated, not a parameter to estimate directly. It is diagnosed by examining response rates, recruitment mechanisms, and comparing sample demographics against known population benchmarks.)_

## 4. When it matters

- Backtesting trading strategies: a security universe defined "as of today" silently excludes delisted, bankrupt, or merged-away companies — a specific, well-known instance of this general failure mode (see [[C - Survivorship Bias]] below).
- Survey-based sentiment or positioning data (e.g. investor surveys, analyst consensus panels): response rates below 20% and self-selected online panels are a documented source of unreliable estimates — the 2015 and 2017 UK general election polling failures were traced to non-representative telephone-poll sampling.
- Any research pipeline that only analyzes "all the data we have" (administrative records, exchange feeds, order-book snapshots) still needs to ask whether that observed dataset is itself a selected slice of the underlying phenomenon of interest, not merely whether the sample is "big."

## 5. Formalized By (Models)

- _(No dedicated formal correction Model exists yet in this vault; correction techniques are context-specific — e.g. reweighting, multi-level regression and post-stratification. See [[M - Bayesian Inference]] for one modern statistical response to non-representative sampling.)_

## 6. Related Concepts

- [[C - Survivorship Bias]] — a specific, well-documented special case of selection bias in which failed/discontinued entities are systematically excluded from a retrospective sample (e.g. mutual funds that closed, delisted stocks), inflating the apparent quality of the surviving population.
- [[C - Alternative Histories]] — related but distinct: Alternative Histories concerns failing to consider the counterfactual paths a single observed history did *not* take; Selection Bias concerns the observed *sample itself* being an unrepresentative slice of the population, prior to any question of counterfactual reasoning.
- [[C - Overconfidence Bias]] — selection bias in self-selected or convenience samples can manufacture spurious "signal" that then feeds overconfident conclusions about a strategy or effect.

## 7. Pitfalls

- Selection bias is not fixed by collecting more data through the same biased mechanism — a larger non-random sample converges to a precise estimate of the *wrong* quantity, not a less precise estimate of the right one.
- "We have all the data" (e.g. a complete administrative record, an exchange's full order-book history) is not automatically free of selection bias — the recording/reporting mechanism itself (what gets logged, what gets reported, what survives to be archived) can still be a selected slice of the true underlying phenomenon.
- Internal validity (does the sample represent the study population it was drawn from) and external validity (does the study population represent the broader target population of interest) are separate questions — a study can be internally rigorous (e.g. a well-randomized trial) yet fail to generalize externally (e.g. results only established in adult men).

## 8. Minimal Example

- The UK National Survey of Sexual Attitudes and Lifestyles (Natsal-3) achieved a well-organized ~66% response rate from a random household sample and is treated as a broadly reliable data source; by contrast, opinion polls before the June 2017 UK general election, run mainly via telephone with 10-20% response rates concentrated on landline households, showed variability across polls far exceeding their claimed statistical margins of error — a signature of uncorrected selection bias in the sampling mechanism, not merely random sampling noise. Source: [[The Art of Statistics - Learning From Data]], Chapter 3.
