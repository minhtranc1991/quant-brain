---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - statistics
  - status/needs-review
layer: model
type: core
domain:
  - statistics
  - quantitative-trading
---
## 1. Definition

**Bootstrapping** is a mathematical model that formalizes [[C - Selection Bias (Sampling Validity)|sampling variability]] estimation without assuming a mathematical shape for the underlying population — a computational procedure that repeatedly resamples the observed data with replacement to build an empirical sampling distribution for any statistic of interest, from which uncertainty intervals ("margins of error") can be read off directly.

## 2. Intuition

- Mechanism: since the population an original sample was drawn from is unknown and unavailable, bootstrapping treats the sample itself as the best available stand-in for the population, and repeatedly draws new samples of the same size *from the sample*, sampling with replacement (so the same data-point can be selected more than once in a given resample, and some original points may not be selected at all). Recomputing the statistic of interest (e.g. a mean, a regression gradient) on each of these "bootstrap resamples" — typically 1,000 or more — produces an empirical distribution of that statistic that approximates its true sampling distribution.
- What this buys you: the bootstrap distribution of most statistics becomes symmetric and approximately normal even when the underlying data distribution is highly skewed, and it narrows as the original sample size grows — an empirical preview of the [[C - Central Limit Theorem]] obtained purely by resampling, with no probability-theory derivation required. A 95% uncertainty interval is simply the range containing the central 95% of the bootstrap resample statistics.
- What determines when to use it versus classical formula-based methods: bootstrapping is assumption-light (no need to assume normality or derive a formula for the statistic's standard error) and works for arbitrarily complex statistics (e.g. a regression coefficient, a ratio of two estimates) where a closed-form variance formula may not exist or may be impractical to derive; but it is computationally "clumsy" for very large datasets (e.g. bootstrapping a 100,000-person survey) where a convenient closed-form theoretical formula (see [[M - Null Hypothesis Significance Testing]]'s confidence-interval machinery) achieves essentially the same answer far more cheaply.

## 3. Mathematical perspective

Given an observed sample $x_1, x_2, \dots, x_n$, a bootstrap resample $x_1^*, x_2^*, \dots, x_n^*$ is drawn by sampling $n$ values with replacement from $\{x_1, \dots, x_n\}$. Repeating this $B$ times (e.g. $B = 1{,}000$) and computing a statistic $\hat{\theta}^*_b$ on each resample produces an empirical approximation to the sampling distribution of $\hat{\theta}$:

$$\{\hat{\theta}^*_1, \hat{\theta}^*_2, \dots, \hat{\theta}^*_B\} \approx \text{sampling distribution of } \hat{\theta}$$

A 95% bootstrap uncertainty interval is the 2.5th to 97.5th percentile of this empirical distribution.

Where:
- $n$ — original sample size (held fixed across all resamples)
- $B$ — number of bootstrap resamples (more resamples reduce Monte Carlo noise in the interval estimate, at the cost of more computation)

## 4. Assumptions

- The observed sample is itself a reasonably representative draw from the population of interest (bootstrapping cannot correct for [[C - Selection Bias (Sampling Validity)]] in how the original sample was obtained — it only characterizes sampling variability given the sample as-is).
- The statistic of interest is reasonably well-behaved under resampling (most standard summary statistics and regression coefficients qualify; some statistics, e.g. extreme-value estimators, are known to bootstrap poorly).

## 5. Estimation / Training Procedure

1. Draw $B$ resamples of size $n$, with replacement, from the original data.
2. Compute the statistic of interest on each resample.
3. Use the resulting empirical distribution directly for uncertainty intervals, or as a diagnostic check against a classical formula-based interval.

## 6. When it matters in Finance

- Estimating the uncertainty of a backtested strategy's performance statistics (e.g. Sharpe ratio, drawdown, hit rate) without assuming returns are normally distributed — directly relevant given fat-tailed, non-normal return distributions.
- Constructing confidence intervals for a fitted regression coefficient (e.g. a factor loading) when the underlying data distribution is not well-approximated by a standard theoretical form.
- Providing an assumption-light cross-check against closed-form confidence intervals derived from [[M - Null Hypothesis Significance Testing]]'s theoretical machinery, particularly useful when sample sizes are moderate and normality is uncertain.

## 7. Based On Concepts

- [[C - Central Limit Theorem]]

_(Model → Concept, `based_on` — the empirical convergence of bootstrap resample statistics toward a symmetric, near-normal distribution as sample size grows is a direct, computational manifestation of the Central Limit Theorem.)_

## 8. Related Models

- [[M - Null Hypothesis Significance Testing]] — bootstrapping and classical theory-based confidence intervals are two independent routes to the same kind of uncertainty interval, and tend to converge closely for large, well-behaved samples (a documented direct comparison found near-identical exact and bootstrap 95% intervals for the same regression gradient).

## 9. Used In Strategies

- _(No existing Strategy note in this vault currently cites bootstrapping explicitly as its uncertainty-estimation mechanism; cross-link when a relevant Strategy note is created or updated.)_

## 10. Limitations / Pitfalls

- Bootstrapping characterizes sampling variability given the observed sample; it cannot detect or correct systematic (non-sampling) bias in how the data was originally collected, such as selection bias or measurement error.
- Not computationally practical for extremely large datasets where a closed-form theoretical formula is available and sufficiently accurate — bootstrapping's comparative advantage is for complex statistics and non-normal/small-to-moderate samples, not as a universal default.

## 11. Minimal Example

- Bootstrapping Galton's 433 mother/daughter height pairs (resampling with replacement, refitting the least-squares regression line 1,000 times) produced a 95% interval for the regression gradient of 0.22 to 0.44 — very close to the classical theory-based 95% interval of 0.23 to 0.42 for the same coefficient, demonstrating the two methods' convergence on a moderately-sized, well-behaved dataset. Source: [[The Art of Statistics - Learning From Data]], Chapter 7.
