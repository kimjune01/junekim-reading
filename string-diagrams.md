# String Diagrams Plan

SVG string diagrams to add across the site. Each should work in both dark and light mode (use `currentColor` or CSS variables, not hardcoded colors).

## Priority (high-value, reusable)

### Copy and discard (Fritz page)
- Wire splits into two = copy (ν)
- Wire ends with a dot = discard (ε)
- Deterministic morphism: copy then apply = apply then copy (both diagrams side by side)
- Stochastic morphism: the two diagrams differ

### COMP rule (Staton page — already exists, could be refined)
- Two boxes connected by a wire = sequential composition
- The intermediate wire labeled R = handshake

### Pipeline (landing page or framework page)
- Six boxes in sequence with the feedback loop
- Consolidate as a backward wire from Remember to Attend's policy input

### Kleisli composition (Fritz page)
- A box with a distribution fan-out on the output wire
- Composing two: each output wire fans into the next box

## Medium priority

### Graded triple (Graded page)
- A box with a grade label on top = cost annotation
- Two graded boxes composed: grades add

### Open game (Hedges page)
- Forward wire (play) and backward wire (utility)
- Two subgames composed: forward chains, backward chains

### Bayesian lens (Smithe page)
- Lens shape: forward top wire, backward bottom wire
- Composition: lenses stack

### Optic (Capucci page)
- Parametrised optic: forward + backward with a parameter wire

## Low priority (nice to have)

### Effect algebra (Cho-Jacobs page)
- Predicate as a wire going to 1+1 (two-outcome test)

### Divergence (Sato page)
- Two parallel morphisms with a distance label between them

### Support monad morphism
- A functor arrow from M-wires to Set-wires

## Style guide
- Minimal: thin lines, rounded box corners, no gradients
- Colors: use CSS `currentColor` for lines, muted accent for labels
- Dark/light: SVGs should inherit text color from the page
- Size: max-width 500px, inline with the text flow
- No external dependencies — raw SVG in the Astro pages
