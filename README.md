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
| Concepts | 38 |
| Models | 9 |
| Strategies | 5 |
| Execution | 2 |
| People | 0 |
| Frameworks | 0 |
| Case Studies | 0 |
| Maps | 0 |
<!-- AUTO-GENERATED:KNOWLEDGE-COVERAGE:END -->


<!-- AUTO-GENERATED:KNOWLEDGE-SOURCES:BEGIN -->
## Knowledge Sources

Knowledge currently synthesized from 8 books.

- *A Random Walk Down Wall Street* — Burton G. Malkiel
- *Economics in One Lesson* — Henry Hazlitt
- *Fooled by Randomness* — Nassim Nicholas Taleb
- *Principles for Dealing with the Changing World Order* — Ray Dalio
- *Python for Data Analysis* — Wes McKinney:
- *Storytelling with Data* — Cole Nussbaumer Knaflic
- *The Art of Statistics - Learning From Data* — David Spiegelhalter:
- *The Intelligent Investor* — - Benjamin Graham
<!-- AUTO-GENERATED:KNOWLEDGE-SOURCES:END -->

## Getting Started with Obsidian

The easiest way to explore this knowledge graph is with [Obsidian](https://obsidian.md/).

### 1. Download the Repository

Download the repository from GitHub as a ZIP file and extract it to a local folder.

Alternatively, if you are familiar with Git:

```bash
git clone <repository-url>
```

The repository contains only the public knowledge layer. The private research library and knowledge-building pipeline are intentionally excluded.

### 2. Open It as an Obsidian Vault

Open Obsidian and select:

**Open folder as vault** → select the downloaded repository folder.

You do not need to install or configure anything else to start browsing the knowledge base.

The repository is plain Markdown, so the notes can also be read with any Markdown-compatible editor.

### 3. Start Exploring

Start with the main knowledge layers:

- `02 - Concepts/` — core ideas, phenomena, biases, and theories.
- `03 - Models/` — formal models and mathematical frameworks.
- `04 - Strategies/` — trading and investing approaches.
- `05 - Execution/` — practical implementation and portfolio techniques.
- `06 - People/` — researchers and practitioners.
- `07 - Frameworks/` — reusable analytical frameworks.
- `08 - Case Studies/` — real-world market episodes and applications.
- `09 - Maps/` — curated indexes connecting related notes.

Open any note and follow its `[[wikilinks]]` to navigate through the knowledge graph.

### 4. Recommended Starting Point

If you are new to the repository, start with `02 - Concepts/` and follow the links from Concepts to Models, Strategies, and Execution.

A typical path through the graph looks like:

**Concept → Model → Strategy → Execution**

For example:

**Efficient Market Hypothesis → Capital Asset Pricing Model → Value Investing → Portfolio Rebalancing**

The graph is designed to be explored through relationships rather than read linearly like a book.

### 5. Using the Graph View

Obsidian's built-in Graph View can be used to visualize relationships between notes.

Open:

**Settings → Core plugins → Graph view**

Then use the graph to explore connections between Concepts, Models, Strategies, and other layers.

For a more focused view, open the graph from an individual note to see its local neighborhood.

### 6. Keeping Your Own Copy

The repository is a public knowledge base, so you are free to download it and use it as your own local Markdown/Obsidian knowledge base.

You can add your own private notes locally without publishing them back to the repository.

If you want to keep your local additions separate from the public knowledge base, consider using your own Git branch or a separate private vault.

### 7. Keeping Your Copy Updated

If you downloaded the repository as a ZIP file, download a new copy when you want the latest version.

If you cloned the repository with Git, update it with:

```bash
git pull
```

Because the repository contains only the public knowledge layer, updates do not include the private research sources or internal knowledge-building workflow used to create the notes.

### 8. Note on Wikilinks

The notes use Obsidian-compatible wikilinks such as:

```markdown
[[Efficient Market Hypothesis]]
[[Capital Asset Pricing Model]]
[[Momentum Investing]]
```

Obsidian resolves these links automatically when the corresponding notes are present in the vault.

If you use another Markdown application, the notes remain readable, but wikilink navigation may require application-specific support.