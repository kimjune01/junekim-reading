# junekim-reading

Textbooks and research papers translated into runnable code with SVG diagrams. Live at [june.kim/reading](https://june.kim/reading/).

## Structure

**Mathematics**
```
/reading/calculus/          ∫   Active Calculus (15 ch)
/reading/real-analysis/     ∞   Jiří Lebl (8 ch)
/reading/linear-algebra/    📐  Jim Hefferon (5 ch)
/reading/abstract-algebra/  🔗  Tom Judson (8 ch)
/reading/discrete-math/     🔢  Oscar Levin (5 ch)
/reading/number-theory/     #   Jim Hefferon (8 ch)
/reading/geometry/          △   Wikipedia + june.kim (12 ch)
/reading/logic/             🔑  Craig DeLancey (10 ch)
/reading/proof-writing/     ✎   Jim Hefferon (8 ch)
/reading/category-theory/   🐱  Bartosz Milewski (24 ch)
```

**Computer Science**
```
/reading/programming/              🪄  Abelson & Sussman — SICP (22 ch)
/reading/algorithms/               ⚙   Nievergelt & Hinrichs (10 ch)
/reading/theory-of-computation/    🔀  Maheshwari & Smid (8 ch)
/reading/operating-systems/        🖥   Wikipedia (10 ch)
/reading/databases/                🗄   Wikipedia (10 ch)
/reading/distributed-systems/      🌐  Wikipedia + Cambridge CS (10 ch)
/reading/cryptography/             🔐  Wikipedia (6 ch)
/reading/machine-learning/         🤖  MML + Dive into Deep Learning (12 ch)
```

**Science & Engineering**
```
/reading/physics/            ⚛   Benjamin Crowell (12 ch)
/reading/control/            🎛   Wikipedia (10 ch)
/reading/probability/        🎰  Grinstead & Snell (12 ch)
/reading/statistics/         📊  OpenIntro (5 ch)
/reading/information-theory/ 📡  Shannon 1948 + Wikipedia (8 ch)
```

**Social Science**
```
/reading/game-theory/        🎲  Jennifer Nordstrom
/reading/economics/          💰  Smith, Ricardo, Marshall + Wikipedia (8 ch)
/reading/finance-1/          📈  OpenStax + MIT OCW 15.401 (12 ch)
/reading/finance-2/          📉  MIT OCW 18.S096 + 15.450 (12 ch)
/reading/cognitive-science/  🧠  Lovelace textbook (8 ch)
```

**Papers**
```
/reading/natural-breadcrumbs/       🍞  21 applied category theory papers
/reading/the-natural-framework-lean/ ✏️  Lean 4 proof navigator
/reading/vector-space-proof/        📐  VCG on Gaussian embeddings — Lean 4
/reading/scientific-method/         🔬  Bacon → Mayo (17 works)
/reading/cognitive-architecture/    🏛️  Minsky → LLM agents (5 papers)
/reading/auction-theory/            💎  Vickrey → Lahaie-Lubin (8 papers)
/reading/prose-writing/             ✍️  Aristotle → Google (9 works)
/reading/commons/                   ⚖   Bush → Mikolov (10 works)
```

## Sources and licenses

Every page attributes its source and inherits the source license. The site itself is CC BY-SA 4.0.

| Source | License | Content |
|---|---|---|
| Active Calculus | CC BY-SA 4.0 | Calculus |
| Jiří Lebl | CC BY-SA 4.0 | Real analysis |
| Jim Hefferon | GFDL / CC BY-SA | Linear algebra, number theory, proofs |
| Tom Judson | GFDL | Abstract algebra |
| Oscar Levin | CC BY-SA 4.0 | Discrete math |
| Craig DeLancey | CC BY-NC-SA | Logic |
| Bartosz Milewski | CC BY-SA 4.0 | Category theory |
| Abelson & Sussman | CC BY-SA 4.0 | Programming (SICP) |
| Nievergelt & Hinrichs | CC BY-SA | Algorithms |
| Maheshwari & Smid | CC BY-SA | Theory of computation |
| Benjamin Crowell | CC BY-SA | Physics |
| Grinstead & Snell | GFDL | Probability |
| OpenIntro | CC BY-SA 3.0 | Statistics |
| OpenStax | CC BY 4.0 | Finance foundations |
| MIT OCW 15.401/18.S096/15.450 | CC BY-NC-SA 4.0 | Finance theory and quantitative methods |
| Jennifer Nordstrom | CC BY-SA 4.0 | Game theory |
| Wikipedia | CC BY-SA 4.0 | Multiple subjects (geometry, OS, databases, etc.) |
| Shannon 1948 | Public domain | Information theory |
| 21 arXiv papers | CC BY-SA derivatives | Applied category theory |
| Various papers | Original expressions (CC BY-SA) | Scientific method, cognitive architecture, auctions, prose, commons |

Permissive sources (MIT, Apache, CC BY) are linked as external pointers, not incorporated as derivatives. Only copyleft and public domain content is compiled into this site. See [Canon](https://june.kim/canon) for the rationale.

## Each page has

- Plain English explanation
- SVG diagrams (inline, currentColor, dark/light mode)
- Runnable Scheme REPL (BiwaScheme, primary)
- Runnable Python REPL (Pyodide, in details/summary)
- Notation reference table
- Neighbor links (prev/next, cross-references, Wikipedia)
- Source attribution with license

## Stack

- **Astro** + React + Tailwind
- **Pyodide** for client-side Python
- **BiwaScheme** for client-side Scheme
- Deployed to S3/CloudFront at `june.kim/reading/`

## Dev

```
pnpm install
pnpm dev        # localhost:12345
```

## Deploy

Built as a static site. Output goes to `dist/`, synced to S3 via the june.kim deploy pipeline (`bash deploy.sh` in the blog repo).

## Adding a new book

1. Verify the source is copyleft or public domain
2. Add a directory under `src/pages/` (e.g., `src/pages/algebra/`)
3. Create an index page and chapter pages following the existing template
4. Pick an emoji, add a `favicon` prop to the Layout
5. Add the book to the foundations table on `src/pages/index.astro`
6. Add the domain to PageLeft's copyleft allowlist if applicable
7. Update this README
