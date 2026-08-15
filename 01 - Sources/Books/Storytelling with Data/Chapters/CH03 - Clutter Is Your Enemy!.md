---
artifact: chapter
source: "Storytelling with Data"
source_id: storytelling-with-data
chapter_id: storytelling-with-data__ch03
chapter_number: 3
chapter_title: "Clutter Is Your Enemy!"
extraction_status: extracted
---

# Chapter 03 — Clutter Is Your Enemy!

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[Storytelling with Data]]

## Summary

Introduces cognitive load as the mental effort an audience must expend to process a visual, and frames decluttering as the discipline of removing any visual element that doesn't add enough informative value to justify its cognitive cost. Cites Tufte's data-ink ratio (maximize the share of a graphic's ink devoted to data) and the equivalent signal-to-noise framing, then walks through six Gestalt principles of visual perception (proximity, similarity, enclosure, closure, continuity, connection) as the mechanism that explains why structural chart elements (borders, gridlines, axis lines, legends) are frequently redundant — human perception already groups/orders data via spacing, color, and shape without them.

## Keywords

- [[C - Decluttering for Signal Clarity]]

## Claims

### Claim 1

Claim ID: `storytelling-with-data__ch03-C001`

Fingerprint: `91930c4bb6cb`

Text: Every visual element in a chart imposes cognitive load (mental processing effort) on the audience; decluttering means identifying and removing any element that isn't adding enough informative value to justify that cost. This is formalized as maximizing the data-ink ratio (Tufte) / signal-to-noise ratio: the larger the share of a graphic devoted to data (signal) versus non-data decoration (noise), the better, other things equal.

Type: `framework`

Section: `Cognitive load / data-ink ratio`

Target Node: [[C - Decluttering for Signal Clarity]]

Decision: `NEW`

### Claim 2

Claim ID: `storytelling-with-data__ch03-C002`

Fingerprint: `d7acef1227a3`

Text: The Gestalt principles of visual perception (proximity, similarity, enclosure, closure, continuity, connection) explain how the eye/brain already groups and orders visual elements without explicit structural aids — e.g. consistent white-space spacing (proximity) can substitute for table borders, and a set of dots aligned in a row is perceived as a line (closure) without a border needing to enclose it. This is the mechanism that makes many default chart elements (borders, background shading, axis lines, legends) genuinely removable without losing perceived structure — decluttering is not merely aesthetic preference but is grounded in how human visual perception fills in structure.

Type: `mechanism`

Section: `Gestalt principles of visual perception`

Target Node: [[C - Decluttering for Signal Clarity]]

Decision: `NEW`

## Notes

Grounds `C - Decluttering for Signal Clarity` directly in this chapter's own two core frameworks (data-ink/signal-to-noise ratio, and the Gestalt principles as the perceptual mechanism).

## Completeness

- Claims extracted: 2
- Claims rejected: individual worked before/after chart examples (same principle applied repeatedly, not a new claim each time).
- Claim density: high — this chapter is the primary source for the decluttering Concept.
