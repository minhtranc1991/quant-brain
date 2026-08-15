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

**Bayesian Inference** is a mathematical model that formalizes [[C - Causal Inference|belief updating under evidence]] — a framework in which probability expresses not only aleatory uncertainty (future randomness) but also epistemic uncertainty (personal ignorance about a fixed but unknown fact), and in which Bayes' theorem provides the formal mechanism for revising a prior probability into a posterior probability in light of new evidence.

## 2. Intuition

- Mechanism: Bayesian inference starts from a prior distribution — the current state of belief about an unknown quantity or hypothesis, based on background knowledge before seeing the new evidence — and combines it with the likelihood (the probability of the observed evidence under each candidate value of the unknown quantity) to produce a posterior distribution, the updated belief after incorporating the evidence. In odds form, this reduces to a strikingly simple rule: posterior odds = prior odds × likelihood ratio, where the likelihood ratio expresses how many times more likely the observed evidence is under one hypothesis than under a competing one. Independent pieces of evidence combine by simply multiplying their likelihood ratios together.
- What determines the practical stakes: when the prior probability of a hypothesis is very low, even a strong piece of evidence (a large likelihood ratio) may leave the posterior probability still modest — this is the resolution to several classic counter-intuitive probability puzzles (e.g. why the majority of positive results from a "95% accurate" screening test for a rare condition are false positives: the low prior prevalence dominates the calculation). This same base-rate-sensitivity is the core mechanism behind the "prosecutor's fallacy" documented in [[C - Probability Blindness]].
- What distinguishes it from the classical/frequentist approach ([[M - Null Hypothesis Significance Testing]]): Bayesian probability can be attached directly to a hypothesis itself (e.g. "there is an 85% probability the Higgs boson exists"), which frequentist statistics explicitly disallows (a P-value is a probability about data given a hypothesis, never a probability about the hypothesis itself). This power comes at the cost of requiring an explicit prior distribution, which is the single most contested element of Bayesian analysis — when the prior arises from a genuine physical randomization process (e.g. Bayes' own "billiard table" thought experiment) it is largely uncontroversial; when it must instead be constructed from subjective judgement or historical data, reasonable analysts can disagree, and a sensitivity analysis across plausible alternative priors is standard practice.

## 3. Mathematical perspective

$$\text{posterior odds} = \text{prior odds} \times \text{likelihood ratio}$$

or equivalently, via Bayes' theorem for a continuous parameter $\theta$ given data $x$:

$$p(\theta \mid x) = \frac{p(x \mid \theta)\, p(\theta)}{p(x)}$$

where the likelihood ratio comparing two hypotheses $H_0$ and $H_1$ given evidence $x$ is:

$$LR = \frac{p(x \mid H_0)}{p(x \mid H_1)}$$

Where:
- $p(\theta)$ — the prior distribution (belief before observing $x$)
- $p(x \mid \theta)$ — the likelihood (probability of the observed data under each value of $\theta$)
- $p(\theta \mid x)$ — the posterior distribution (updated belief after observing $x$)

## 4. Assumptions

- A prior distribution must be specified for any unknown parameter or hypothesis; the resulting posterior is only as credible as this prior, and a genuinely "objective" or assumption-free prior does not generally exist — sensitivity to plausible alternative priors should be checked and reported.
- Evidence used to update sequentially (posterior becomes the new prior for the next piece of evidence) is treated as conditionally independent given the hypothesis, unless a more elaborate joint model is used.

## 5. Estimation / Training Procedure

1. Specify a prior distribution for the unknown quantity/hypothesis (from physical randomization, historical data, or explicit subjective judgement — with a documented sensitivity analysis across alternatives).
2. Specify the likelihood — the probability of the observed data under each candidate value of the unknown quantity.
3. Combine via Bayes' theorem to obtain the posterior distribution.
4. For hierarchical/multi-level problems (many related sub-populations, e.g. geographic areas or asset clusters), assume the sub-population parameters are themselves drawn from a shared prior distribution, which pools information across sub-populations and "shrinks" noisy individual estimates toward a common mean — this is the mechanism behind multi-level regression and post-stratification (MRP), used to derive reliable local estimates (e.g. election forecasts by constituency) from sparse, non-representative data.

## 6. When it matters in Finance

- Updating a model's parameter estimates (e.g. a factor's expected return, a regime probability) as new data arrives, in a principled way that formally incorporates prior structural knowledge rather than treating each new dataset in isolation.
- Hierarchical/shrinkage estimation is directly applicable to any setting with many related but individually noisy sub-groups — e.g. estimating expected returns or risk parameters across many small sub-sectors, strategies, or geographies with limited data each, where pooling toward a shared prior produces materially more reliable estimates than treating each sub-group in isolation.
- Likelihood-ratio-style reasoning underlies signal-combination frameworks that weigh multiple independent pieces of evidence (e.g. combining several weak, independent trading signals) via multiplicative updating rather than naive averaging.

## 7. Based On Concepts

- [[C - Causal Inference]]

_(Model → Concept, `based_on` — Bayesian inference is one of the two principal competing statistical philosophies, alongside frequentist NHST, for weighing evidence toward or against a causal or associational hypothesis.)_

## 8. Related Models

- [[M - Null Hypothesis Significance Testing]] — a competing statistical philosophy, in unresolved methodological tension since the 1930s; the two are used pragmatically together in modern practice (e.g. Neyman-Pearson-style trial design combined with Fisherian P-value reporting) rather than one having definitively superseded the other.
- [[M - Bootstrapping]] — like Bayesian inference, an alternative to purely formula-derived frequentist confidence intervals, though built on a different (resampling-based, not belief-updating) logic.

## 9. Used In Strategies

- _(No existing Strategy note in this vault currently cites Bayesian inference explicitly as its estimation mechanism; cross-link when a relevant Strategy note is created or updated.)_

## 10. Limitations / Pitfalls

- The choice of prior distribution is the most contested element of any Bayesian analysis; a poorly justified or undisclosed prior can smuggle in unwarranted conclusions, which is why likelihood ratios (rather than full posterior probabilities requiring a prior) are the form of Bayesian evidence permitted in many legal systems, and why combining multiple likelihood ratios by simple multiplication is in some jurisdictions restricted to expert testimony rather than formal court procedure.
- **Enrichment — the primary *cognitive* failure mode: representativeness overriding base rates ([[Thinking, Fast and Slow]]):** even statistically trained subjects routinely fail to apply Bayesian base-rate updating intuitively. In the "Tom W" experiment, subjects rank a candidate's likely field of graduate study almost entirely by resemblance to a stereotype, largely ignoring the true relative base-rate enrollment across fields (the prior). In the related "Linda" experiment, subjects judge a conjunction of two stereotype-fitting details ("bank teller and feminist activist") as *more* probable than either detail alone — the "conjunction fallacy," a violation of elementary probability logic (a conjunction cannot exceed either of its constituent probabilities), driven by the added detail's better stereotype-fit ("representativeness") overriding both the base rate and the logical constraint. This shows representativeness/similarity judgments and true probabilistic (base-rate-respecting) reasoning are computed by different, competing processes, with representativeness frequently winning. Source: [[Thinking, Fast and Slow]], Chapters 14-15.
- **Enrichment — causal framing vs. statistical framing of identical base-rate information ([[Thinking, Fast and Slow]]):** purely statistical, population-level base rates ("bare statistics") are systematically underweighted in individual-case judgment unless reframed as a causal or stereotype-relevant claim, in which case the same information is instead over-applied as an indiscriminate stereotype — statistical facts and causal narratives about a specific case are processed by different cognitive routes, and only causally-framed information reliably updates individual-case judgment in practice. This is a distinct, compounding pitfall alongside representativeness/base-rate neglect above: it is not only that base rates are ignored, but that *how* a base rate is presented (as an abstract statistic vs. as a causal story) determines whether it is used at all. Source: [[Thinking, Fast and Slow]], Chapter 16.
- Bayesian hierarchical/shrinkage methods (e.g. MRP) are not a universal fix for non-representative data: if survey or sample respondents within a given sub-group are systematically unrepresentative of that sub-group (not merely sparse), no amount of statistical pooling across sub-groups corrects for that within-group bias.
- Bayes factors (the Bayesian analogue of a P-value for comparing two hypotheses) still require prior distributions over the parameters of each hypothesis, and different reasonable prior choices can materially change the resulting Bayes factor — the appearance of the same rigor as a P-value does not eliminate this judgment-dependence.

## 11. Minimal Example

- Multi-level regression and post-stratification (MRP), a hierarchical Bayesian technique, correctly predicted the winner in 50 of 51 US states in the 2016 presidential election from interviews with only 9,485 voters (missing only Michigan), and correctly forecast a 2017 UK hung parliament when traditional polling methods failed — both results achieved by pooling sparse, non-randomly-sampled data across many small demographic/geographic cells using a shared prior distribution rather than treating each cell's estimate in isolation. Source: [[The Art of Statistics - Learning From Data]], Chapter 11.
- **A second worked example — practical, applied Bayesian reasoning outside survey estimation:** professional sports bettor Haralabos Voulgaris placed an $80,000 bet (his entire savings) on the 1999-2000 Los Angeles Lakers to win the NBA championship at a time when the Vegas market-implied probability was 13%. Voulgaris's own estimate, built from many small, individually weak, independent pieces of contextual evidence (team injury recovery, coaching adjustments, a misleadingly small sample of early-season losses) rather than one decisive signal, was roughly 25% — enough of a divergence from the market price to justify a bet with a theoretical expected profit of $70,000. Silver frames this as the practical essence of Bayesian reasoning: treating the future as a continuously updated probability distribution rather than a binary prediction, and explicitly distinguishing *finding* a pattern (easy, and already priced in by other market participants if it is obvious) from correctly *judging* whether a given pattern is durable signal or a sample-specific artifact likely to regress — the actual source of a repeatable forecasting edge. Source: [[The Signal and the Noise]], Chapter 8 ("Less and Less and Less Wrong").
