---
artifact: chapter
source: "A Random Walk Down Wall Street"
source_id: a-random-walk-down-wall-street
chapter_id: a-random-walk-down-wall-street__ch14
chapter_number: 14
chapter_title: "A Life-Cycle Guide to Investing"
extraction_status: extracted
---

# Chapter 14 — A Life-Cycle Guide to Investing

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[A Random Walk Down Wall Street]]

## Summary

Presents five asset-allocation principles tied to investor life stage: risk and reward are related; actual risk in stocks/bonds depends on holding period; dollar-cost averaging reduces the risk of poorly timed lump-sum investment; rebalancing can reduce risk and, empirically, sometimes increase return; and investors should distinguish their objective risk capacity from subjective risk tolerance. Provides age-banded life-cycle asset-allocation guidance and discusses retirement drawdown, annuities, and life-cycle (target-date) funds.

## Keywords

- [[E - Dollar-Cost Averaging]]
- [[E - Portfolio Rebalancing]]
- [[C - Diversification]]

## Claims

### Claim 1

Claim ID: `a-random-walk-down-wall-street__ch14-C001`

Fingerprint: `f36267d1edec`

Text: Dollar-cost averaging (investing a fixed dollar amount at regular intervals rather than a lump sum) reduces the risk of purchasing an entire equity position at a temporarily inflated price, at the cost of potentially lower total return in a steadily rising market; Malkiel illustrates that in a volatile-but-flat five-year scenario, dollar-cost averaging a fixed $1,000/year produced a $1,048 gain versus a smaller gain in a steadily-rising scenario, because more shares are automatically purchased when prices are low.

Type: `mechanism`

Section: `Dollar-Cost Averaging Can Reduce the Risks of Investing in Stocks and Bonds`

Target Node: [[E - Dollar-Cost Averaging]]

Decision: `NEW`

### Claim 2

Claim ID: `a-random-walk-down-wall-street__ch14-C002`

Fingerprint: `23514baa2e72`

Text: Periodically rebalancing a portfolio back to its target asset-class weights (e.g. 60% stocks/40% bonds) reduces portfolio volatility and, empirically over 1996-2013 (60% Russell 3000/40% Barclays Aggregate Bond, annually rebalanced vs. never rebalanced), also modestly increased average annual return (8.41% vs. 8.14%) while reducing volatility (11.55% vs. 13.26%), because rebalancing systematically sells recent winners and buys recent underperformers.

Type: `empirical_claim`

Section: `Rebalancing Can Reduce Investment Risk and Possibly Increase Returns`

Target Node: [[E - Portfolio Rebalancing]]

Decision: `NEW`

## Notes

- **NEW_NODE:** Dollar-Cost Averaging and Portfolio Rebalancing are concrete, reusable Execution mechanisms with specific parameters and empirical results -- both created as Execution-layer notes per the Concept->Model->Strategy->Execution ontology, linked back to the Diversification Concept and (implicitly) the passive-indexing strategy they support.

## Completeness

- Claims extracted: 2
- Claims rejected: 0
- Claim density: normal
