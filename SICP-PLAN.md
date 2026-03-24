# Programming Foundations: SICP + Composing Programs

## Sources

| Source | License | Role |
|---|---|---|
| SICP (Abelson & Sussman, 2e) | CC BY-SA 4.0 | Scheme text, examples, exposition |
| Composing Programs (DeNero) | CC BY-SA 3.0 | Python translations in `<details>` blocks |

Both are CC BY-SA compatible. Derivative ships as CC BY-SA 4.0.

## Emoji

📖 Programming (SICP)

## Route

`/reading/sicp-NN/`

## Spine (22 pages, ★ = paper-critical)

### Part I — Building Abstractions with Procedures

| # | SICP Section | One-line | ★ |
|---|---|---|---|
| 01 | 1.1 Expressions | The REPL is the lab bench | ★ |
| 02 | 1.2 Recursion & iteration | A process is not a procedure | ★ |
| 03 | 1.3 Higher-order functions | Functions that take and return functions | ★ |

### Part II — Building Abstractions with Data

| # | SICP Section | One-line | ★ |
|---|---|---|---|
| 04 | 2.1 Data abstraction | Pairs, barriers, "what is data?" | ★ |
| 05 | 2.2 Hierarchical data | Lists, trees, map/filter/reduce, closure property | ★ |
| 06 | 2.3 Symbolic data | Symbols, sets, Huffman trees | ★ |
| 07 | 2.4 Multiple representations | Tagged data, data-directed programming | |
| 08 | 2.5 Generic operations | Coercion, type towers | |

### Part III — Modularity, Objects, and State

| # | SICP Section | One-line | ★ |
|---|---|---|---|
| 09 | 3.1 Assignment & state | `set!` changes everything | ★ |
| 10 | 3.2 Environment model | How the machine tracks bindings | |
| 11 | 3.3 Mutable data | Tables, queues, constraint nets | ★ |
| 12 | 3.4 Concurrency | Serializers, deadlock | |
| 13 | 3.5 Streams | Infinite sequences, delayed evaluation | ★ |

### Part IV — Metalinguistic Abstraction

| # | SICP Section | One-line | ★ |
|---|---|---|---|
| 14 | 4.1 Metacircular evaluator | Scheme in Scheme | ★ |
| 15 | 4.2 Lazy evaluation | Normal order, thunks | |
| 16 | 4.3 Nondeterministic computing | `amb`, backtracking search | |
| 17 | 4.4 Logic programming | Query language, unification | |

### Part V — Computing with Register Machines

| # | SICP Section | One-line | ★ |
|---|---|---|---|
| 18 | 5.1 Register machines | Designing a machine | |
| 19 | 5.2 Register-machine simulator | Building the simulator | |
| 20 | 5.3 Memory & GC | Storage allocation, stop-and-copy | |
| 21 | 5.4 Explicit-control evaluator | The evaluator as a machine | |
| 22 | 5.5 Compilation | Translating to register code | |

## Paper connections (★ pages only)

| Page | Papers that need it |
|---|---|
| 01 Expressions | All (the REPL is the interface) |
| 02 Recursion | Fractal tower (Lean proof), Markov chains |
| 03 Higher-order | Fritz 2020 (kernels), Hedges 2018 (strategies) |
| 04 Data abstraction | Smithe 2021 (lenses), Spivak 2013 (typed ports) |
| 05 Hierarchical data | Leinster 2021 (magnitude), compositional structure |
| 06 Symbolic data | Staton 2025 (preconditions), Hoare logic |
| 09 Assignment & state | Gaboardi 2021 (graded effects), Capucci 2021 (feedback) |
| 11 Mutable data | Kura 2026 (indexed state) |
| 13 Streams | Panangaden 2009 (bisimulation over infinite processes) |
| 14 Metacircular evaluator | Staton 2025 (programs reasoning about programs), Milewski ch9 (Curry-Howard) |

## Format

Same as Milewski/Nordstrom pages:
- SchemeRepl primary (from SICP)
- Python in `<details>` blocks (from Composing Programs)
- SVG diagrams (original, matching site style)
- Notation reference table
- Neighbors section linking to paper pages and Wikipedia
- Translation notes explaining what was adapted

## Attribution (index page)

> Sources: Harold Abelson and Gerald Jay Sussman with Julie Sussman,
> *Structure and Interpretation of Computer Programs*, 2nd ed. (CC BY-SA 4.0);
> John DeNero, *Composing Programs* (CC BY-SA 3.0).
