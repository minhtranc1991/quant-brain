---
artifact: chapter
source: "Python for Data Analysis"
source_id: python-for-data-analysis
chapter_id: python-for-data-analysis__ch04
chapter_number: 4
chapter_title: "NumPy Basics: Arrays and Vectorized Computation"
extraction_status: extracted
---

# Chapter 04 — NumPy Basics: Arrays and Vectorized Computation

_(SOURCE / INTERMEDIATE ARTIFACT — a provenance layer that supports ingestion, NOT a canonical Concept/Model/Strategy/Execution knowledge note. See `10 - Meta/Book Ingestion/pipeline-overview.md` and `schema/language-policy.md`.)_

Source: [[Python for Data Analysis]]

## Summary

Introduces the ndarray as NumPy's core homogeneous, fixed-type array structure and explains why vectorized (whole-array) operations vastly outperform equivalent per-element Python loops by delegating computation to optimized, compiled routines rather than the Python interpreter. Also covers broadcasting (implicit shape alignment between differently-shaped arrays), array slices as views sharing memory with their source (not copies), axis-wise reduction (sum/mean/cumsum along a chosen axis), and universal functions (ufuncs) for fast element-wise transforms.

## Keywords

- [[C - Vectorized Computation]]

## Claims

### Claim 1

Claim ID: `python-for-data-analysis__ch04-C001`

Fingerprint: `67342d7041b7`

Text: Performing an operation across a whole array at once (vectorized computation) is dramatically faster than an equivalent per-element Python loop, because the array operation is executed by optimized, compiled (typically C-level) routines rather than being interpreted element-by-element by the Python interpreter.

Type: `theoretical_claim`

Section: `NumPy Basics: Arrays and Vectorized Computation`

Target Node: [[C - Vectorized Computation]]

Decision: `NEW`

### Claim 2

Claim ID: `python-for-data-analysis__ch04-C002`

Fingerprint: `10188f0ff38e`

Text: NumPy arrays support broadcasting: operations between arrays of different but compatible shapes are automatically aligned and expanded along size-1 or missing dimensions, removing the need for explicit loops or manual shape-matching when combining differently-shaped data.

Type: `mechanism`

Section: `NumPy Basics: Arrays and Vectorized Computation`

Target Node: [[C - Vectorized Computation]]

Decision: `NEW`

## Notes

- Existing-node-first check: searched `02 - Concepts/` for an existing Vectorized Computation, Array Computing, or Broadcasting note; none found. Created as NEW_NODE.
- Grounded in the book's own markdown narrative (chapter 4 notebook), paraphrased, not verbatim-quoted.

## Completeness

- Claims extracted: 2
- Claims rejected: 0 (view-based slicing, ufuncs and axis-reduction are treated as supporting mechanisms of the same durable principle rather than separate claims).
- Claim density: normal for a TECHNICAL_SOURCE chapter with one clear durable principle.
