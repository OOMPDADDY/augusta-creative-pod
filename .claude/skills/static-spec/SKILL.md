---
name: static-spec
description: Emit a field by field static specification a designer or an image model can build from directly, with every string inside its character budget.
---

# Static Spec

## The output

One spec table per concept. Every field, every ratio, no ambiguity.

## The prompt

```
Below are the argument brief, the chosen headlines, the layout grid and the
character budgets.

BRIEF: [PASTE]
HEADLINES: [PASTE]
LAYOUT GRID: [PASTE]
CHARACTER BUDGETS: [PASTE]

For each concept emit a spec table and nothing else:

| Field | Content | Chars | Budget | Fits? |

Fields, in this order: EYEBROW, HEADLINE, SUBHEAD, PROOF LINE, CTA, LEGAL,
BADGE, IMAGE DIRECTION.

IMAGE DIRECTION is one sentence describing what the image shows, in nouns and
verbs. Never adjectives about mood.

Rules:
- Every text field carries its real character count against its budget.
- Any field over budget is rewritten until it fits. Never ship a NO.
- File name is [ARG_ID]-[CONCEPT_ID]-[ratio].
- Emit one table per ratio in the matrix. Fields that change per ratio are
  rewritten, not truncated.
```

## Truncation is the failure this prevents

A 60 character headline in a 42 character field exports successfully. It just
exports wrong, and nobody catches it until the set is live and the hook rate is
inexplicable. Counting at the spec stage costs nothing and removes the single
most common silent defect in static production.

## What to do with it

Straight into the brand templates, or into an image model, or to a designer. The
spec is deliberately tool agnostic. `export-check` validates the output against
this same table, which is why both read the same fields.
