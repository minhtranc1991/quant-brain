---
modified:
  - "2026-08-15"
created:
  "2026-08-15"
tags:
layer: concept
type: core
domain:
  - "data-visualization"
  - "quantitative-research"
---
## 1. Definition

**Chart Type Selection for Quantitative Data** is the principle that a visual display should be chosen to match the specific data relationship the audience needs to see — comparison across categories, change over time, correlation between two variables, or composition of a whole — rather than chosen by default, habit, or what a tool makes easiest. A related, narrower requirement follows for magnitude-comparison charts specifically: bar charts must use a zero baseline, because the eye judges a bar's value by comparing its length/endpoint against that baseline, and a non-zero baseline produces a false visual comparison.

## 2. Intuition

- Different graph families encode data differently, and each encoding is read by a different visual judgment: a scatterplot lets the eye assess the relationship between two variables along independent x/y axes; a line graph or slopegraph lets the eye read a trend or rate of change via slope/direction; a bar chart lets the eye compare category magnitudes via the length of aligned, common-baseline bars; an area/square-area chart lets the eye compare very different magnitudes compactly, at the cost of humans being poor at judging two-dimensional area accurately.
- Because bar charts are read by comparing bar *length* from a common baseline, that baseline must be zero — otherwise the visual ratio between bars no longer matches the underlying numeric ratio. A concrete illustration from the source: a chart of a tax rate moving from 35% to 39.6%, plotted with a baseline of 34% instead of 0%, visually implied roughly a 460% increase (computed from the truncated bar heights) versus the true 13% increase. This distortion does **not** apply to line graphs, where the comparison is of relative position/slope in space, not of length from a baseline — a non-zero baseline is tolerable there (with care), but never for bars.
- The same selection logic extends to a short "avoid" list: pie charts and donut charts ask the eye to compare angles, areas, or arc lengths — visual judgments people are demonstrably bad at (a real example: a 31% pie slice was widely misjudged as larger than an adjacent 34% slice due to 3D tilt and area-based comparison). 3D charts distort magnitude further through rendering artifacts (e.g. a 3D bar's rendered height in Excel is derived from an invisible tangent plane, not a direct mapping to the data value). Secondary y-axes force extra cognitive work to determine which series maps to which axis and can visually imply a spurious relationship between two unrelated series.

## 3. Mathematical perspective (if applicable)

For a bar chart with baseline $b \neq 0$ and true values $v_1, v_2$, the rendered bar heights are $h_i = v_i - b$. The visually implied ratio of change, $\frac{h_2 - h_1}{h_1} = \frac{v_2 - v_1}{v_1 - b}$, diverges from the true ratio of change $\frac{v_2 - v_1}{v_1}$ whenever $b \neq 0$, and the divergence grows as $b \to v_1$. This is a structural property of any bar/length-based encoding, not a rendering bug — it is why the zero-baseline requirement is a hard rule for bars specifically, and not a general axis-scaling rule for every chart type.

## 4. When it matters

- Choosing the right chart for backtest performance comparisons across strategies, risk/return dashboards, factor-exposure breakdowns, or research-finding summaries — the same distortions (truncated bar axes, pie charts for portfolio composition, 3D bar charts, dual/secondary y-axes overlaying price and volume or price and a signal) are common, well-documented sources of misread quantitative results in finance and research communication.
- Any point where a systematic researcher or PM is presenting a quantitative result to a non-technical stakeholder (risk committee, investor letter, internal report) and the chart itself — not just the underlying analysis — could mislead.

## 5. Formalized By (Models)

_(None — this is a communication/presentation principle, not a model with parameters or an estimation procedure.)_

## 6. Related Concepts

- [[C - Decluttering for Signal Clarity]]
- [[C - Preattentive Attention Design]]

## 7. Pitfalls

- Truncating a bar chart's y-axis (non-zero baseline) inflates or deflates the visual magnitude of a change relative to the true numeric change — always use a zero baseline for bar charts.
- Using pie charts, donut charts, or 3D charts for quantitative comparison — human perception is unreliable at judging angle, arc length, and 3D-rendered magnitude; a bar chart (or, for parts of a whole, a 100%-stacked bar) is almost always a more accurately read substitute.
- Using a secondary y-axis to overlay two series in different units — this both burdens the reader with figuring out which axis belongs to which series and can visually suggest a correlation between the series that isn't actually established by the data. Preferable alternatives: label data points directly, or stack the two series' panels vertically sharing a common x-axis.
- Choosing a chart type by default/tool-familiarity rather than by the relationship being shown — e.g. defaulting to a line graph for genuinely categorical (non-continuous) data implies a false connectedness between adjacent categories.

## 8. Minimal Example

- A bar chart of five products' average prices over 2008-2014 was redesigned (per the source) by moving from a default multi-series layout toward one that keeps a zero baseline, orders/labels categories for the story being told, and drops a redundant legend in favor of direct labeling — the same underlying data, but a chart-type/axis choice that reads far more accurately and quickly.

#status/needs-review
