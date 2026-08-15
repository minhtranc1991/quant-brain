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

**Null Hypothesis Significance Testing (NHST)** is a mathematical model that formalizes [[C - Causal Inference|evidence assessment]] against a default ("null") assumption — a procedure that computes the probability (P-value) of observing data at least as extreme as what was actually observed, assuming the null hypothesis and all other modelling assumptions are true, and combines this Fisherian evidence measure with the Neyman-Pearson framework of pre-specified Type I/Type II error control to decide whether to reject the null hypothesis.

## 2. Intuition

- Mechanism: a null hypothesis (H0) is a provisional, "innocent until proven guilty" default assumption — typically that no effect, no difference, or no association exists. A test statistic is chosen such that more extreme values indicate greater incompatibility with H0; its sampling distribution *under H0* is derived (via probability theory, permutation, or simulation), and the P-value is the probability of a result at least as extreme as the one observed, calculated under that null distribution. A conventionally small P-value (historically P < 0.05 or P < 0.01, Fisher's arbitrary but now-entrenched thresholds) is declared "statistically significant" — interpreted as evidence against H0, never as proof that H0 is false, and never as the probability that H0 itself is true.
- What determines statistical power: the Neyman-Pearson extension formalizes hypothesis testing as a decision problem with two possible errors — a Type I error (rejecting a true null hypothesis, with probability α, the "size" of the test) and a Type II error (failing to reject a false null hypothesis, with probability β; "power" = 1−β is the probability of correctly detecting a real effect of a specified size). Required sample size for a study is derived by fixing both α (e.g. 0.05) and the desired power (e.g. 80-90%) against a specific, practically important alternative hypothesis — larger effect sizes and larger samples both increase power, and there is an inescapable trade-off: loosening the significance threshold to increase power also increases the Type I error rate.
- What determines correct application: a single, pre-specified, confirmatory test with the assumptions correctly stated is well-behaved. Running many tests and reporting only the most significant one, or making flexible post-hoc analytical choices (multiple testing / "researcher degrees of freedom" — see [[C - P-Hacking]]), inflates the effective false-positive rate far beyond the nominal per-test α, even though each individual test's formula remains mathematically correct in isolation.

## 3. Mathematical perspective

$$P\text{-value} = P(T \geq t \mid H_0 \text{ true})$$

for a one-sided test with test statistic $T$ and observed value $t$ (extended to a two-sided P-value when both directions of extremity are relevant). The size of a test is:

$$\alpha = P(\text{reject } H_0 \mid H_0 \text{ true})$$

and power is:

$$1 - \beta = P(\text{reject } H_0 \mid H_1 \text{ true})$$

A 95% confidence interval and a two-sided P-value are mathematically linked: a two-sided P-value is less than 0.05 exactly when the corresponding 95% confidence interval excludes the null-hypothesis value (typically zero).

## 4. Assumptions

- The null hypothesis's sampling distribution has been correctly derived — this depends on the truth of *all* underlying modelling assumptions (independence, correct distributional form, absence of undisclosed multiple testing), not only on the null hypothesis itself; a small P-value indicates *some* assumption in the model is likely wrong, not necessarily that the substantive null hypothesis specifically is false.
- For confirmatory use, the test and its threshold should be pre-specified before seeing the data; using the same data to both explore/select a hypothesis and confirm it invalidates the stated P-value (see [[C - P-Hacking]]).

## 5. Estimation / Training Procedure

1. State a null hypothesis H0 (and, for Neyman-Pearson power calculations, an alternative hypothesis H1).
2. Choose a test statistic for which more extreme values indicate greater incompatibility with H0.
3. Derive (via probability theory, permutation, or simulation) the sampling distribution of the test statistic under H0.
4. Compute the P-value as the tail-area probability of the observed (or more extreme) statistic under that null distribution.
5. Compare to a pre-specified significance threshold α (or report the exact P-value alongside a confidence interval, now the preferred practice).

## 6. When it matters in Finance

- Assessing whether an apparent backtested strategy edge (e.g. a winning margin between two algorithms, or a factor's average return) is distinguishable from chance variation, rather than assuming any positive backtested result reflects genuine skill.
- Determining required sample size (e.g. how many independent trading periods, how many A/B-tested variants) to achieve adequate statistical power before concluding "no significant effect" actually means "no effect," rather than "underpowered study."
- Multiple-hypothesis correction (e.g. Bonferroni: divide the significance threshold by the number of tests) is directly relevant to any large-scale factor-mining or signal-search process, which is structurally identical to the "many significance tests, report only the significant ones" failure mode this Model documents — see [[C - P-Hacking]].

## 7. Based On Concepts

- [[C - Causal Inference]]

_(Model → Concept, `based_on` — NHST is one of the principal formal tools used to assess whether an observed association is distinguishable from chance, a necessary but not sufficient step toward a causal claim.)_

## 8. Related Models

- [[M - Bayesian Inference]] — a competing, and in places incompatible, statistical philosophy: Bayesian posterior probabilities and Bayes factors treat H0 and H1 symmetrically and can directly express the probability of a hypothesis given the data, which frequentist P-values explicitly cannot; the two frameworks have been in open, unresolved methodological dispute since the 1930s (Fisher vs. Neyman-Pearson vs. Bayesian schools), though in practice a pragmatic mix (Neyman-Pearson-style trial design, Fisherian P-value reporting) has become standard.
- [[M - Bootstrapping]] — an alternative, assumption-light route to a confidence interval that, for well-behaved data, produces results closely matching the classical theory-based intervals this Model derives from probability theory.

## 9. Used In Strategies

- _(No existing Strategy note in this vault currently cites NHST explicitly as its validation mechanism; cross-link when a relevant Strategy note is created or updated.)_

## 10. Limitations / Pitfalls

- A P-value is not the probability that the null hypothesis is true, and a non-significant P-value does not mean the null hypothesis has been proven — per the American Statistical Association's 2016 principles, P-values measure incompatibility between data and a model, not the model's probability of being true.
- Statistical significance is not the same as practical/economic significance: a very large sample (e.g. millions of observations) can make a tiny, practically unimportant effect statistically significant — a documented example found a 19% *relative* increase in a rare brain-tumor risk across education levels was statistically significant (over 2 million subjects) but corresponded to an absolute risk increase from roughly 5 to 6 cases per 3,000 people.
- Running many significance tests and reporting only the significant ones (multiple testing / [[C - P-Hacking]]) inflates the true false-positive rate far above the nominal per-test threshold; standard corrections include the Bonferroni method (divide α by the number of tests) or pre-registration and replication requirements.
- Repeated ("sequential") testing on accumulating data is guaranteed to eventually produce a "significant" result even under a true null hypothesis (the Law of the Iterated Logarithm) unless a dedicated sequential-testing method (e.g. the Sequential Probability Ratio Test) with appropriately adjusted thresholds is used instead of naive repeated NHST.

## 11. Minimal Example

- CERN's 2012 announcement of the Higgs boson discovery was reported as a "five-sigma" result, corresponding to a P-value below 1 in 3.5 million under the null hypothesis that the Higgs boson did not exist — illustrating both correct NHST practice (an extremely stringent threshold demanded before a landmark scientific claim) and a widespread misinterpretation in press coverage, where several major outlets incorrectly reported this P-value as "the probability the result is a statistical fluke" (a version of the fallacy this Model's Limitations section documents). Source: [[The Art of Statistics - Learning From Data]], Chapter 10.
