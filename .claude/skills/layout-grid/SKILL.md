---
name: layout-grid
description: Define the five layout archetypes as real templates at every ratio, so a spec table can autofill into something that exists. One-time build, permanent.
---

# Layout Grid

The spec table the Static Speccer emits assumes five layouts exist as real
templates. This builds them.

## The five archetypes

- HERO: product dominant, headline above, CTA below.
- SPLIT: image one side, copy the other, hard vertical divide.
- BEFORE_AFTER: two panels, thin divider, small labels.
- QUOTE: customer quote dominant, small avatar, product secondary.
- BIG_NUMBER: one numeral dominating the canvas, short supporting line.

## Rules

- Build each one at EVERY ratio you run. A template that exists at 1:1 and not
  at 9:16 will silently produce a broken vertical.
- Name fields identically across all five: HEADLINE, SUBHEAD, PROOF_CHIP, CTA,
  IMAGE. The speccer's output maps by field name.
- Leave 8% safe margin on every edge.
- No layout should depend on a specific copy length to look intentional.

## Why five

Fewer and every set looks like one ad repeated. More and you cannot tell whether
a result came from the layout or the argument. Five is enough variety to avoid
repetition and few enough to stay readable.
