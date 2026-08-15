---
artifact: chapter
source: "Python for Data Analysis"
source_id: python-for-data-analysis
chapter_id: python-for-data-analysis__ch11
chapter_number: 11
chapter_title: "Time Series"
extraction_status: extracted
---

# Chapter 11 — Time Series

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[Python for Data Analysis]]

## Summary

Covers using datetime values as a Series/DataFrame index to get automatic time-based alignment when combining differently-dated data; resampling between frequencies (e.g. daily to monthly) for both downsampling (aggregating) and upsampling; Period objects for calendar-aware business concepts (e.g. a fiscal quarter) that plain date arithmetic does not capture; the distinction between naive and timezone-localized timestamps and the silent-error risk of comparing/aligning across them (especially around daylight-saving transitions); rolling-window statistics (e.g. a moving average) computed over a sliding time window without explicit date-range loops; and shifting/lagging a series to study leading/lagging relationships between time-dependent variables.

## Keywords

- [[C - Time-Series Data Alignment]]

## Claims

### Claim 1

Claim ID: `python-for-data-analysis__ch11-C001`

Fingerprint: `e0473e4b3137`

Text: Using a datetime-based index is what makes time-series alignment automatic: combining two differently-dated datasets on a shared datetime index re-aligns them by timestamp without manual date-matching logic, the same way ordinary label-based alignment works for non-time-indexed data.

Type: `theoretical_claim`

Section: `Time Series`

Target Node: [[C - Time-Series Data Alignment]]

Decision: `NEW`

### Claim 2

Claim ID: `python-for-data-analysis__ch11-C002`

Fingerprint: `7ed9309dea79`

Text: A naive (timezone-unaware) timestamp and a timezone-localized timestamp are not interchangeable: comparing, aligning, or arithmetic-combining them without first reconciling time zones (and accounting for daylight-saving transitions) can silently produce incorrect alignments rather than raising an obvious error.

Type: `theoretical_claim`

Section: `Time Series`

Target Node: [[C - Time-Series Data Alignment]]

Decision: `NEW`

### Claim 3

Claim ID: `python-for-data-analysis__ch11-C003`

Fingerprint: `01b79f3c962e`

Text: Resampling to a coarser or finer frequency and computing rolling-window statistics (e.g. a moving average over a fixed trailing window) are the two general mechanisms for changing a time series's effective time resolution — resampling changes the sampling frequency itself, while a rolling window smooths/summarizes at the original frequency.

Type: `mechanism`

Section: `Time Series`

Target Node: [[C - Time-Series Data Alignment]]

Decision: `NEW`

## Notes

- Existing-node-first check: searched `02 - Concepts/` and `03 - Models/` for an existing Time Series / Time-Series Alignment / Resampling note; none of the 21 existing Concepts or 5 Models cover this (closest are C - Random Walk Hypothesis and C - Ergodicity, which are about stochastic-process properties, not indexing/alignment mechanics — no overlap). Created as NEW_NODE.
- Period objects and shift/lag treated as supporting mechanisms of the same alignment/resolution principle, not separate claims.

## Completeness

- Claims extracted: 3
- Claims rejected: 0
- Claim density: normal-to-high; this chapter has the clearest quant-adjacent durable content in the book (time-series data is directly relevant to quantitative trading data pipelines).
