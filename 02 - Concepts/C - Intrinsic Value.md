---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - status/needs-review
layer: concept
type: core
domain:
  - quantitative-trading
  - investing
---
## 1. Definition

**Intrinsic Value** is the value of a security justified by the underlying business's assets, earnings, dividends, and definite prospects — as distinct from its fluctuating quoted market price. Graham introduces the concept in *The Intelligent Investor* (Ch. 11) as the anchor against which both [[C - Margin of Safety]] and the [[C - Mr. Market]] discipline are defined.

## 2. Intuition

- Intrinsic value is deliberately not a single precise number — Graham treats it as a defensible range or estimate derived from fundamentals (multi-year average earnings, asset backing, financial strength), not a point forecast of future price. The analyst's job is to estimate this range conservatively enough that a purchase below it leaves a genuine [[C - Margin of Safety]].
- What determines the estimate's reliability: the quality and stability of the underlying inputs. Graham (Ch. 12) warns that single-year reported earnings-per-share are frequently distorted by non-recurring items, accounting choices, and dilution, so averaging several years' earnings and adjusting for dilution materially improves the estimate's reliability relative to naively trusting one year's reported number.
- Distinct from market price by construction: market price is set by the marginal transaction of the moment (Mr. Market's mood on a given day), while intrinsic value is meant to be a slower-moving estimate grounded in the business's actual economics — the entire point of the framework is that the two can and do diverge, sometimes for extended periods.

## 3. Mathematical perspective (if applicable)

No single canonical formula in the source; the closest operational proxies given are multi-year average earnings capitalized at a conservative multiple, and (for the most conservative "net-net" case) net current asset value $=$ current assets $-$ total liabilities, entirely ignoring fixed assets and goodwill.

## 4. When it matters

- The reference point that makes [[C - Margin of Safety]] and [[C - Mr. Market]] meaningful — without an independent intrinsic-value estimate, "buy low, sell high" collapses into reacting to price momentum itself, which Graham treats as speculation rather than investment.
- Underlies the "Value Investing" strategy's alpha logic (see `04 - Strategies/S - Value Investing.md`): the strategy is only a coherent discipline, rather than arbitrary contrarianism, if a defensible intrinsic-value estimate exists to screen against.

## 5. Formalized By (Models)

- [[M - Fama-French Three-Factor Model]] — the value (HML) factor operationalizes "cheap relative to fundamentals" using observable multiples (book-to-market) as an empirical proxy for divergence from intrinsic value, at the population/factor level rather than the single-security level Graham analyzes.

## 6. Related Concepts

- [[C - Margin of Safety]] — the protective cushion defined relative to this value estimate.
- [[C - Mr. Market]] — the discipline for treating quoted price as distinct from this estimate.
- [[C - Efficient Market Hypothesis]] — the strong form of EMH implies price and intrinsic value cannot persistently diverge in an exploitable way; Graham's entire framework presupposes they can. See the Superinvestors of Graham-and-Doddsville material added to that Concept note.

## 7. Pitfalls

- Intrinsic value is an estimate, not a fact — treating it as a precise, provably correct number defeats the purpose of demanding a margin of safety against estimation error in the first place.
- Reported per-share earnings require real adjustment (multi-year averaging, dilution correction) before they are a reliable input; using a single raw reported EPS figure is a common, source-flagged error (Ch. 12).

## 8. Minimal Example

- Graham's four-company comparison (Ch. 13) applies the same intrinsic-value framework to companies of similar size but very different valuations, showing that the same analytical discipline yields very different investment conclusions depending on the price actually paid relative to the estimated value. Source: [[The Intelligent Investor]], Chapters 11-13.

#status/needs-review
