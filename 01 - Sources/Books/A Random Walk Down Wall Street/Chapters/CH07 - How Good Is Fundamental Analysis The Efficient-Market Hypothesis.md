---
artifact: chapter
source: "A Random Walk Down Wall Street"
source_id: a-random-walk-down-wall-street
chapter_id: a-random-walk-down-wall-street__ch07
chapter_number: 7
chapter_title: "How Good Is Fundamental Analysis? The Efficient-Market Hypothesis"
extraction_status: extracted
---

# Chapter 07 — How Good Is Fundamental Analysis? The Efficient-Market Hypothesis

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[A Random Walk Down Wall Street]]

## Summary

Presents the core evidence for the Efficient-Market Hypothesis (EMH). Security analysts' earnings forecasts (tested via Malkiel and Cragg's survey of 19 Wall Street firms) are shown to do no better,  and sometimes worse, than naive extrapolation; five structural reasons are given (random events, creative accounting, analyst error, loss of top analysts to sales/portfolio management, and investment-banking conflicts of interest). Mutual-fund performance data (Ibbotson/Lipper/SPIVA, the WSJ dartboard contest, survivorship-bias-adjusted fund samples) show that professionally managed portfolios do not persistently beat a broad index. The chapter formally defines the weak, semi-strong, and strong forms of EMH and closes with a note arguing high-frequency trading improves rather than harms price efficiency for ordinary investors.

## Keywords

- [[C - Efficient Market Hypothesis]]
- [[C - Random Walk Hypothesis]]
- [[C - Survivorship Bias]]

## Claims

### Claim 1

Claim ID: `a-random-walk-down-wall-street__ch07-C001`

Fingerprint: `cd530573ccec`

Text: The efficient-market hypothesis states that a security's price already reflects all available information (public information in the semi-strong form, all information including inside information in the strong form), so that no investor can systematically earn above-average risk-adjusted returns using that information; prices move essentially randomly because they react so quickly to new (unpredictable) information that no one can trade fast enough to profit from it.

Type: `definition`

Section: `The Semi-Strong and Strong Forms of the EMH`

Target Node: [[C - Efficient Market Hypothesis]]

Decision: `NEW`

### Claim 2

Claim ID: `a-random-walk-down-wall-street__ch07-C002`

Fingerprint: `099b77682587`

Text: A study comparing 19 major Wall Street firms' one-year and five-year earnings forecasts against actual outcomes found the forecasts did no better than, and for five-year horizons sometimes worse than, naive extrapolation of past trends; forecast errors were large (averaging over 30% per year in a separate study) and no analyst was consistently superior across years.

Type: `empirical_claim`

Section: `Are Security Analysts Fundamentally Clairvoyant?`

Target Node: [[C - Efficient Market Hypothesis]]

Decision: `EXISTING`

### Claim 3

Claim ID: `a-random-walk-down-wall-street__ch07-C003`

Fingerprint: `33d23c08290c`

Text: Comparisons of mutual-fund returns against broad market indexes over multi-decade periods (Ibbotson/Lipper/SPIVA data) consistently show the average actively managed equity fund underperforming a low-cost index fund, and this holds after controlling for survivorship bias (funds with poor records tend to be merged away, inflating the apparent average performance of the surviving sample).

Type: `empirical_claim`

Section: `Do Security Analysts Pick Winners?`

Target Node: [[C - Survivorship Bias]]

Decision: `NEW`

### Claim 4

Claim ID: `a-random-walk-down-wall-street__ch07-C004`

Fingerprint: `0a696ad91e1b`

Text: High-frequency trading (HFT), despite criticism that it advantages a select group of traders, primarily benefits ordinary investors by keeping exchange-traded index fund prices closely arbitraged to their underlying net asset value, though front-running of visible order flow is a genuine, separately addressable regulatory concern.

Type: `competing_view`

Section: `A Note on High-Frequency Trading (HFT)`

Target Node: [[C - Efficient Market Hypothesis]]

Decision: `EXISTING`

## Notes

- **NEW_NODE:** Efficient Market Hypothesis and Survivorship Bias are both genuinely new, reusable Concepts (no existing vault notes to enrich, per the Source Resolution/dedup check on an empty vault).

## Completeness

- Claims extracted: 4
- Claims rejected: 0
- Claim density: normal
