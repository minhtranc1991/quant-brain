# Quant Trading Knowledge Graph

A public quantitative knowledge base — a structured, interconnected graph of
concepts, models, strategies, and execution mechanisms in quantitative
trading, investing, portfolio management, and market microstructure.

This is not a book-summary library. Each note is a synthesized, reusable
knowledge unit: a mechanism, a claim, a framework, or a technique — written
so it stands on its own and links to the other notes it relates to.

## What This Repository Contains

This repository publishes the **knowledge product**: the notes themselves.
It does not publish the private research library, source PDFs, or the
internal tooling used to build the graph — see "What's Not Included" below.

## Ontology

Every note belongs to one of these layers:

| Layer | Meaning |
| --- | --- |
| **Concepts** | A definable idea, phenomenon, bias, or theory (e.g. Efficient Market Hypothesis, Loss Aversion). |
| **Models** | A formal mechanism or mathematical framework (e.g. Capital Asset Pricing Model, Fama-French Three-Factor Model). |
| **Strategies** | A trading or investing approach built from one or more Concepts/Models (e.g. Momentum Investing, Value Investing). |
| **Execution** | A concrete implementation technique (e.g. Dollar-Cost Averaging, Portfolio Rebalancing). |
| **People** | Notable practitioners, researchers, or theorists whose work shaped the graph. |
| **Frameworks** | Reusable structured thinking tools that span multiple Concepts/Models. |
| **Case Studies** | Real-world episodes (bubbles, crashes, strategy failures/successes) analyzed through the ontology above. |
| **Maps** | Curated indexes connecting related notes across layers. |

Concepts, Models, Strategies, and Execution form the graph's core hierarchy
— a Strategy is typically built on one or more Models, and a Model typically
formalizes one or more Concepts. People, Frameworks, Case Studies, and Maps
are supporting, non-competing layers.

## How Knowledge Is Organized

Every note is a living document. When new evidence, a new perspective, or a
more precise mechanism becomes available, an existing note is **enriched**
rather than duplicated. A materially different mechanism or materially
different trading logic becomes a new Model or Strategy rather than
overwriting an existing one. When sources genuinely disagree, both positions
are preserved — under `Perspectives` / `Competing Views` / `Current
Synthesis` sections — rather than collapsed into false consensus.

## Provenance

Claims are traced back to where they came from. Each note distinguishes
between what a cited source claims, what independent research supports,
prior knowledge already in the graph, and original synthesis connecting
them. Standard theory is never presented as if it were a particular author's
original claim just because that author discusses it.

## How the Graph Evolves

New knowledge enters the graph by processing a book, paper, or other source:
the source is read, meaningful claims are identified, each claim is checked
against the existing graph, and the result is either an enrichment of an
existing note or a new note — never a duplicate. Every newly created or
substantively modified note is marked `#status/needs-review` and awaits
human review before being marked reviewed. This repository only reflects
knowledge that has gone through that process.

## Reusing This Knowledge

Every note is a self-contained Markdown file with a plain-language
explanation, a mental-model "Intuition" section (not a dictionary
definition), and wikilinks to related notes. You can browse the folders
directly, or clone the repository into any Markdown-aware tool (e.g.
Obsidian) to navigate the graph interactively.

## What's Not Included

This repository is intentionally scoped to the public knowledge product.
It does not include: the private research library or source PDFs/EPUBs,
the internal ingestion/synthesis tooling and prompts that build this graph,
internal process/audit documentation, or any local machine or workflow
configuration. Book titles are cited as bibliographic attribution where
relevant (see Knowledge Sources below), but the underlying source files
themselves are never published, out of respect for copyright.


<!-- AUTO-GENERATED:KNOWLEDGE-COVERAGE:BEGIN -->
## Knowledge Coverage

| Layer | Notes |
| --- | ---: |
| Concepts | 12 |
| Models | 5 |
| Strategies | 4 |
| Execution | 2 |
| People | 0 |
| Frameworks | 0 |
| Case Studies | 0 |
| Maps | 0 |
<!-- AUTO-GENERATED:KNOWLEDGE-COVERAGE:END -->


<!-- AUTO-GENERATED:KNOWLEDGE-SOURCES:BEGIN -->
## Knowledge Sources

Knowledge currently synthesized from 1 book.

- *A Random Walk Down Wall Street* — Burton G. Malkiel
<!-- AUTO-GENERATED:KNOWLEDGE-SOURCES:END -->
