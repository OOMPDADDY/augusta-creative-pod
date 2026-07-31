---
name: character-budgets
description: Measure the real character capacity of every field in every template at every ratio, so the static-speccer writes to what the template actually holds. One-time build per template set.
---

# Character Budgets

The single most common cause of a broken set, and the one nobody specifies.

## Why this exists

A 60-character headline reflows to three lines in a template built for two,
shoves the CTA off the canvas, and exports successfully. Nothing errors.

## How to build it

For each template, at each ratio you run:

1. Fill the field with a repeating character string.
2. Increase the length until the layout breaks: reflow past its line count,
   overlap, or push another element out of frame.
3. Record the number BEFORE the break, minus 10% of safety margin.
4. Record it per field, per ratio.

## The output

```
TEMPLATE | RATIO | FIELD | MAX CHARS
HERO     | 1:1   | HEADLINE   | 42
HERO     | 9:16  | HEADLINE   | 34
...
```

Take the LOWEST number across all ratios for a field. That is the budget the
speccer writes to. Writing to the highest and hoping is the same as not having
budgets.

Save to `config/character-budgets.md`.

## Do not guess these

An estimated budget is worse than none, because it produces confidence and the
same silent failure.
