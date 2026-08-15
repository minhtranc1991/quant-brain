---
artifact: chapter
source: "Storytelling with Data"
source_id: storytelling-with-data
chapter_id: storytelling-with-data__ch02
chapter_number: 2
chapter_title: "Choosing an Effective Visual"
extraction_status: extracted
---

# Chapter 02 — Choosing an Effective Visual

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[Storytelling with Data]]

## Summary

Surveys the small set of visual display types (simple text, tables, heatmaps, and graphs built from points/lines/bars/area) that cover most business data-communication needs, and gives concrete selection rules: match the display type to the relationship being shown (a scatterplot for two-variable relationships, a line/slopegraph for change over time, bars for categorical comparison). Establishes the zero-baseline rule for bar charts (illustrated by a Fox News tax-rate chart whose truncated axis inflated a 13% change into an apparent 460% change) and a list of chart types/elements to avoid: pie charts, donut charts, 3D, and secondary y-axes, each because they distort or obscure accurate quantitative comparison.

## Keywords

- [[C - Chart Type Selection for Quantitative Data]]

## Claims

### Claim 1

Claim ID: `storytelling-with-data__ch02-C001`

Fingerprint: `13b17f247d1b`

Text: Different graph families suit different data relationships: scatterplots for the relationship between two variables, line graphs/slopegraphs for change over time, bar charts for comparison across categories, and area/square-area graphs (used sparingly) for numbers of vastly different magnitude — the graph type should be chosen to match the specific relationship the audience needs to see, not chosen by default or habit.

Type: `framework`

Section: `Graphs`

Target Node: [[C - Chart Type Selection for Quantitative Data]]

Decision: `NEW`

### Claim 2

Claim ID: `storytelling-with-data__ch02-C002`

Fingerprint: `55d6137a41ac`

Text: Bar charts must use a zero baseline because the eye judges bar magnitude by comparing the length/endpoint of each bar; starting the axis above zero creates a false visual comparison. A real example: a bar chart of a 35%-to-39.6% tax-rate change with a non-zero (34%) baseline visually implied a 460% increase, versus the true 13% increase once replotted with a zero baseline. This zero-baseline requirement does not apply to line graphs, where position-in-space (not bar length from a baseline) carries the comparison.

Type: `mechanism`

Section: `Bars`

Target Node: [[C - Chart Type Selection for Quantitative Data]]

Decision: `NEW`

### Claim 3

Claim ID: `storytelling-with-data__ch02-C003`

Fingerprint: `5a7f066ead45`

Text: Pie charts, donut charts, 3D charts, and secondary y-axes should generally be avoided in quantitative communication: pie/donut charts ask the eye to compare angles/arc-lengths/areas that humans read poorly (a chart used in the book's own example was misread — the visually "largest" 31% pie slice was actually smaller than an adjacent 34% slice); 3D distorts values via perspective/rendering (Excel's 3D bar height is computed from an invisible tangent plane, producing bar heights that don't match the plotted values); secondary y-axes force the reader to work out which series maps to which axis and can visually imply a relationship between two series that may not exist.

Type: `limitation`

Section: `To be avoided`

Target Node: [[C - Chart Type Selection for Quantitative Data]]

Decision: `NEW`

## Notes

This is the chapter this ingestion is most grounded in for `C - Chart Type Selection for Quantitative Data` — definition, mechanism (zero-baseline), and pitfalls (misleading chart types) are all drawn directly from this chapter's worked examples, not from general reputation of the book.

## Completeness

- Claims extracted: 3
- Claims rejected: table/heatmap design details (borders, conditional formatting), bar-width "Goldilocks" guidance, category-ordering guidance — real but secondary styling detail, not separately durable enough to warrant their own claim beyond the parent framework.
- Claim density: high — this chapter is the primary source for the chart-type-selection Concept.
