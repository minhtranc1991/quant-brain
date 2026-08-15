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

**Regression Analysis** is a mathematical model that formalizes [[C - Causal Inference]]-adjacent relationships between variables — a formula that decomposes an observed outcome into a deterministic component (a fitted line/curve as a function of one or more explanatory variables) plus residual error, estimated by minimizing the sum of squared residuals (ordinary least squares) or an analogous criterion for non-continuous outcomes (logistic/Poisson regression).

## 2. Intuition

- Mechanism: `observation = deterministic model + residual error`. Given paired data (e.g. fathers' and sons' heights), the least-squares line is the straight line through the data that minimizes the sum of squared vertical distances (residuals) between each observed point and the line. The line's gradient (regression coefficient) says how much the outcome variable is expected to change, on average, for a one-unit difference in the explanatory variable — this is a statement about *association*, not automatically about *causation* (see [[C - Causal Inference]]) unless the explanatory variable was itself randomized or a full causal-inference argument has been made separately.
- Multiple regression extends the same logic to several explanatory variables simultaneously, which serves two related purposes: (1) building a joint predictive formula, and (2) *adjustment* — isolating the association between one variable of interest and the outcome while holding other, potentially confounding variables constant. Different types of outcome variable require a different regression form: linear regression for continuous outcomes, logistic regression for proportions/binary outcomes (constrained to stay between 0% and 100%, unlike a naively extrapolated linear fit), and Poisson/Cox regression for counts and survival times respectively.
- What determines the interpretation of a coefficient: whether the design was experimental (randomized) or observational. In an RCT, the coefficient on the randomized variable can be given a causal interpretation because random allocation balances confounders. In observational data, the same coefficient is only a conditional association — "the expected change in Y associated with a one-unit difference in X, holding the other included variables constant" — and remains vulnerable to unmeasured (lurking) confounders no matter how many observed variables are included.

## 3. Mathematical perspective

$$\hat{y} = b_0 + b_1 x$$

Where the least-squares gradient $b_1 = r \cdot \frac{s_y}{s_x}$ (Pearson correlation $r$ times the ratio of the standard deviations of $y$ and $x$), and the intercept $b_0 = \bar{y} - b_1\bar{x}$. For multiple explanatory variables:

$$\hat{y} = b_0 + b_1 x_1 + b_2 x_2 + \dots + b_p x_p$$

fitted by minimizing the residual sum of squares $\sum_i (y_i - \hat{y}_i)^2$. For a proportion outcome, logistic regression instead models the log-odds as linear in the explanatory variables:

$$\log\left(\frac{\hat{p}}{1-\hat{p}}\right) = b_0 + b_1 x_1 + \dots + b_p x_p$$

so that $b_1$ is interpreted as a log(odds ratio) rather than a direct change in probability.

Where:
- $\hat{y}$ — predicted value of the dependent (response) variable
- $x_1 \dots x_p$ — independent (explanatory) variables
- $b_1 \dots b_p$ — regression coefficients (the association between each explanatory variable and the outcome, adjusted for the others)

## 4. Assumptions

- The deterministic component is correctly specified (e.g. genuinely linear in the chosen variables, or an appropriate non-linear/logistic/Poisson form for the outcome type).
- Residual errors are the "signal and the noise" split — treated as unavoidable, unexplained variability rather than as an error to be eliminated.
- Any causal interpretation of a coefficient additionally requires either randomization of the explanatory variable of interest, or a full observational causal-inference argument (see [[C - Causal Inference]]) — regression fitting alone never establishes causation.

## 5. Estimation / Training Procedure

- Ordinary least squares (OLS): choose coefficients minimizing the residual sum of squares; has a closed-form solution for linear regression.
- Logistic/Poisson/Cox regression: fit by maximum likelihood rather than least squares, since the outcome is not a continuous, unbounded quantity.
- Model complexity/variable selection can be regularized (e.g. LASSO, which simultaneously estimates coefficients and can shrink some to exactly zero) to control overfitting when there are many candidate explanatory variables — see [[C - Overfitting]].

## 6. When it matters in Finance

- Factor-model estimation (e.g. estimating a security's loadings on systematic risk factors) is a direct application of multiple linear regression.
- Adjusting a naive backtested-strategy return for known risk exposures (adjustment/stratification) before attributing outperformance to genuine skill.
- Any claim that a variable "predicts" or "explains" returns should specify the regression form (linear/logistic/other) appropriate to the outcome and disclose whether the relationship is being interpreted causally or purely associatively.

## 7. Based On Concepts

- [[C - Causal Inference]]

_(Model → Concept, `based_on` — regression is the primary computational tool used within the broader discipline of causal inference and confounder adjustment.)_

## 8. Related Models

- [[M - Capital Asset Pricing Model]] — CAPM's beta is itself estimated via a simple linear regression of security returns on market returns, a direct financial application of this Model.
- [[M - Fama-French Three-Factor Model]] — a multiple-regression extension of CAPM with additional explanatory factors.

## 9. Used In Strategies

- _(No existing Strategy note in this vault currently cites regression analysis explicitly as its estimation mechanism; cross-link when a relevant Strategy note is created or updated.)_

## 10. Limitations / Pitfalls

- A fitted regression line is a simplified "map," not the underlying reality — George Box: "all models are wrong, some are useful." The 2007-2008 financial crisis is attributed in part to excessive trust placed in complex mortgage-risk regression models whose correlation assumptions (moderate, largely independent default risk) broke down once conditions changed and defaults became highly correlated — a caution against treating a fitted model's outputs as more reliable than its underlying assumptions warrant.
- Naive linear extrapolation outside the observed data range can produce nonsensical predictions (e.g. a linear fit to survival-rate-vs-volume data can imply survival rates above 100%); logistic regression's bounded form exists specifically to avoid this failure mode for proportion outcomes.
- A regression coefficient's statistical significance is not the same as its practical importance — a very large sample can make a tiny, practically unimportant coefficient statistically significant (see [[M - Null Hypothesis Significance Testing]]).

## 11. Minimal Example

- Galton's 1886 study of parent and adult-offspring heights: the least-squares regression of sons' heights on fathers' heights had a gradient of 0.45 (not 1), meaning tall fathers tend to have sons who are shorter than themselves and short fathers tend to have taller sons — a genuine statistical phenomenon ("regression to mediocrity," now [[C - Regression to the Mean]]), not evidence that height is not substantially heritable. Source: [[The Art of Statistics - Learning From Data]], Chapter 5.
