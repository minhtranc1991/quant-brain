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

**Regression to the Mean** is the statistical tendency for an unusually extreme observation (either high or low) to be followed by a less extreme one, because part of what produced the original extreme value was chance/luck that does not systematically repeat — distinct from, and frequently confused with, the time-series concept of "mean reversion" (a data-generating process reverting to a long-run level) and with a genuine causal effect of any intervention that happened to coincide with the reversion. No dedicated "Mean Reversion" Concept note yet exists in this vault; the distinction is documented here as plain-text guidance for whoever creates one.

## 2. Intuition

- Mechanism: any extreme observation is a mixture of a persistent, "true" underlying level plus a chance component. Because the chance component is, by definition, not expected to repeat in the same direction next time, a repeat measurement tends to land closer to the underlying average than the original extreme reading did — purely as a statistical consequence of how the extreme value was selected (i.e. selected *because* it was extreme), not because of any active corrective force. Galton first observed this with parent/offspring heights ("regression to mediocrity": tall fathers have sons who are, on average, shorter than themselves, and short fathers have taller sons) and it generalizes to any repeated or before/after measurement of a noisy quantity.
- What determines the size of the effect: the proportion of the original extreme value's deviation that was due to chance rather than a persistent underlying level. When chance dominates (e.g. small sample sizes, highly noisy measurements, closely matched competitors), regression to the mean is large; when the underlying signal dominates and the noise component is small, it is minimal.
- The critical practical trap is misattributing the resulting reversion to an intervention that happened to be applied at the extreme moment: speed cameras installed at accident "black spots" (chosen precisely because of a recent extreme accident count) get credited for a subsequent decline that randomized studies show is roughly two-thirds attributable to regression to the mean alone; the same mechanism explains apparent clinical-trial placebo effects (patients enrolled while symptoms are at their worst tend to improve regardless of treatment), the "Sports Illustrated cover curse," and fund managers who are promoted or given bonuses after a lucky run of good years and subsequently "revert."

## 3. Mathematical perspective (if applicable)

For a regression of a repeated measurement $y$ on an initial extreme measurement $x$, the expected reversion is governed by the correlation $r$ between the two measurements: the predicted $y$ for a given $x$ moves only a fraction $r$ of the way from the mean to $x$ (in standardized units), not the full distance — the lower $r$ (the noisier the relationship between the two occasions), the greater the expected regression to the mean.

## 4. When it matters

- Evaluating any "before vs. after" claim about a trading-system change, a risk-control intervention, or a manager/strategy replacement that was triggered specifically because performance had just been unusually bad (or unusually good) — the observed subsequent reversion may be substantially or entirely a statistical artifact rather than evidence the change worked.
- Interpreting rankings and league tables that fluctuate year to year (e.g. fund performance rankings, factor-strategy leaderboards): top and bottom performers in one period tend to move toward the middle in the next period even with zero genuine change in skill or process, purely from noise in the ranking measure.
- Distinguishing this phenomenon from genuine [[C - Mean Reversion]] in a price or spread series, which is a property of the data-generating process itself (e.g. a stationary process reverting to a long-run level), not an artifact of how an extreme observation was selected for follow-up.

## 5. Formalized By (Models)

- [[M - Regression Analysis]] — the correlation/gradient of a fitted regression line directly determines the magnitude of the expected regression-to-the-mean effect between two correlated, repeated measurements.

## 6. Related Concepts

- "Mean reversion" (time-series concept, no dedicated Concept note yet in this vault) — a **false friend** in plain-text terms only: mean reversion describes a property of a time series' data-generating process (the series itself tends back toward a long-run level over time); Regression to the Mean describes a statistical artifact of selecting an extreme observation for follow-up measurement. The two can co-occur and are easy to conflate, but a series can exhibit one without the other.
- [[C - Overconfidence Bias]] — misattributing a regression-to-the-mean reversion to a manager's or trader's skillful corrective action can feed overconfident narratives about causal control that is not actually present.
- [[C - Survivorship Bias]] — both are selection-driven statistical artifacts, but survivorship bias concerns which entities remain observable in a sample, while regression to the mean concerns how a *specific* extreme observation is expected to evolve on remeasurement.

## 7. Pitfalls

- Do not conclude "no real change occurred" just because regression to the mean is present — genuine effects and regression to the mean can and often do coexist; the correct response is to isolate the intervention's effect using a proper control group (e.g. a randomized trial of speed-camera placement), not to assume the entire observed change is either 100% real or 100% artifact.
- A correlation between initial ranking and subsequent ranking change that is strongly negative (e.g. −0.60, observed for PISA international education rankings between 2003 and 2012) can be almost entirely explained by regression to the mean alone (theory predicts −0.71 under pure chance) — a documented case where an apparently meaningful trend largely dissolves under this lens.

## 8. Minimal Example

- UK speed cameras are typically installed at locations with a recent spike in accidents; accident rates at these locations subsequently fall, and randomized evaluation studies estimate that roughly two-thirds of this apparent benefit is attributable to regression to the mean rather than a genuine causal effect of the cameras — illustrating why before/after comparisons at a site selected *because* it was extreme are systematically biased toward showing "improvement" regardless of any real intervention effect. Source: [[The Art of Statistics - Learning From Data]], Chapter 5.
