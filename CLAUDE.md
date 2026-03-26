# junekim-reading

Textbooks and research papers translated into runnable code with SVG diagrams. Live at [june.kim/reading](https://june.kim/reading/).

## Local dev

```
pnpm install
pnpm dev        # localhost:12345
```

## Deploy

No deploy script in this repo. The site is built and deployed via the june.kim blog repo:

```
cd ~/Documents/june.kim && bash deploy.sh
```

That script builds reading as a subpath and syncs everything to S3/CloudFront.

## Tests

```
pnpm test       # vitest
```

## Link prefixes

Every external link gets an inline icon before the link text:

| Domain | Prefix | Example |
|---|---|---|
| `june.kim/*` | `<img src="/reading/jk.png" alt="jk" style="display:inline;height:1em;vertical-align:-0.1em;margin-right:0.2em;"/>` | jk initials logo |
| `github.com/*` | `<img src="/reading/github.svg" alt="gh" style="display:inline;height:1em;vertical-align:-0.1em;margin-right:0.2em;"/>` | GitHub octocat |
| `en.wikipedia.org/*` | `<img src="/reading/wikipedia.svg" alt="wp" style="display:inline;height:1em;vertical-align:-0.1em;margin-right:0.2em;"/>` | W in circle, inverts in dark mode |
| `arxiv.org/*` | `<img src="/reading/arxiv.png" alt="arxiv" style="display:inline;height:1em;vertical-align:-0.1em;margin-right:0.2em;"/>` (if available) | arXiv logo |

The `jk`, `gh`, and `arxiv` images invert in dark mode via `filter: invert(1)` in `Base.astro`. The Wikipedia emoji needs no inversion.

**Exceptions:** Footer attribution links (`june.kim` as a byline) don't get the prefix.

### Internal cross-section links

Links between different sections of the reading site use the target section's emoji as prefix. Examples:

```
🐱 Milewski Ch.1        (linking to category-theory)
📐 Linear Algebra Ch.3   (linking to linear-algebra)
✏️ Natural Framework      (linking to the-natural-framework-lean)
🎲 Game Theory            (linking to game-theory)
```

Links within the same section (e.g. Auction.lean → Efficiency.lean inside vector-space-proof) don't need a prefix — they're siblings, not cross-references.
