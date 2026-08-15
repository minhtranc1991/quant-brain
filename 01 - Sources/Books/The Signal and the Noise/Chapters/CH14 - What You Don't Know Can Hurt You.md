---
artifact: chapter
source: "The Signal and the Noise"
source_id: the-signal-and-the-noise
chapter_id: the-signal-and-the-noise__ch14
chapter_number: 14
chapter_title: "What You Don't Know Can Hurt You"
extraction_status: extracted
---

# Chapter 14 — What You Don't Know Can Hurt You

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[The Signal and the Noise]]

## Summary

Examines terrorism prediction, centered on the failure to anticipate Pearl Harbor and September 11. Introduces the distinction (via economist Thomas Schelling) between the unfamiliar and the improbable - a contingency that has not been seriously considered is mentally categorized as improbable simply because it is unfamiliar, producing a kind of "mind-blindness" (Rumsfeld's "unknown unknowns") rather than a reasoned probability judgment. Also discusses terrorism magnitudes following a power-law (fat-tailed) distribution, per research by Aaron Clauset.

## Keywords

- [[C - Probability Blindness]]
- [[C - Rare Event Risk (Fat-Tail Mispricing)]]

## Claims

### Claim 1

Claim ID: `the-signal-and-the-noise__ch14-C001`

Fingerprint: `c9341fe71db9`

Text: Before Pearl Harbor, U.S. military planners implicitly reasoned via a flawed syllogism ("The United States is rarely attacked; Hawaii is part of the United States; therefore Hawaii is unlikely to be attacked") that ignored Hawaii's genuinely distinct risk profile (geographic proximity to Japan, presence of the Pacific fleet) - an out-of-sample generalization error. Economist Thomas Schelling's sharper point (quoted by Silver) is that the failure runs deeper than flawed reasoning: "there is a tendency in our planning to confuse the unfamiliar with the improbable" - an unconsidered contingency is not merely judged unlikely, it frequently is not consciously considered as a possibility at all, producing a structural blind spot rather than a correctable probability misjudgment.

Type: `mechanism`

Section: `Chapter 13, "The Unfamiliar and the Improbable"`

Target Node: [[C - Probability Blindness]]

Decision: `EXISTING`

### Claim 2

Claim ID: `the-signal-and-the-noise__ch14-C002`

Fingerprint: `0c500d55ebb2`

Text: Research by Aaron Clauset and colleagues finds that terrorist attack magnitudes (casualties per event) follow an approximately power-law (fat-tailed) distribution rather than a normal one, meaning extreme, catastrophic events are far more probable than a normal-distribution-based intuition would suggest, and the largest historical event in a given dataset is a weak upper bound on what can occur, not a ceiling.

Type: `empirical_claim`

Section: `Chapter 13, "Defining and Measuring Terrorism"`

Target Node: [[C - Rare Event Risk (Fat-Tail Mispricing)]]

Decision: `EXISTING`

## Notes

- **[[ENRICH]]:** `C - Probability Blindness` - added a fourth, distinct manifestation: mistaking the unfamiliar for the improbable (Schelling's mechanism), structurally different from the ritual-formation, loss-aversion, and prosecutor's-fallacy manifestations already documented - this one operates by preventing a contingency from being consciously considered at all, rather than by miscalculating a probability that was considered.
- **[[ENRICH]]:** `C - Rare Event Risk (Fat-Tail Mispricing)` - added the terrorism power-law/fat-tail empirical evidence (Clauset et al.) as a second domain (alongside the existing options-trading example from `Fooled by Randomness`) documenting the general fat-tailed-distribution mechanism behind rare-event mispricing.

## Completeness

- Claims extracted: 2
- Claims rejected: several (Rumsfeld interview biographical detail, detailed Pearl Harbor/9-11 timeline narrative)
- Claim density: high.
