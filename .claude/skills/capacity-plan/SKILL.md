---
name: capacity-plan
description: Convert available production capacity into testable units, so the cycle is planned in answers rather than in assets.
---

# Capacity Plan

## The output

Capacity stated in testable units, with the honest limit named.

## The prompt

```
Below is available production capacity for the cycle and the ratio matrix.

CAPACITY: [PASTE]
RATIO MATRIX: [PASTE]

Convert to testable units.

Emit only:

| Input | Count |

Rows: total files producible, ratios per concept, concepts producible,
concepts per argument required, arguments testable this cycle.

Then three lines:
"Testable units this cycle: N"
"Arguments this cycle can answer: N"
"If you fund more than N arguments, the cycle answers none of them."

Placement is coverage. Never count ratios as testable units.
```

## The arithmetic nobody does

A hundred files sounds like a hundred tests and is usually twenty, because five
ratios per concept is coverage rather than variation. Teams fund six arguments
against capacity for three, split the concepts, and end the cycle with six
unreadable results. Doing this arithmetic before funding is a ten minute job
that decides whether the cycle produces answers.

## What to do with it

The last line is a constraint on `test-design`, not a suggestion. If the
operator wants more arguments funded, the honest response is more capacity or
fewer arguments, and this table is what makes that conversation short.
