---
name: test-design
description: Decide how many concepts each argument gets, what is held constant and what counts as a read, before anything is made.
---

# Test Design

## The output

A test plan table, plus the read rule stated in one line.

## The prompt

```
Below are the funded arguments and the available production capacity.

ARGUMENTS: [PASTE]
CAPACITY (assets available this cycle): [PASTE]

Design the test.

Emit only:

| ARG_ID | Concepts | Variable tested | Held constant | Placements | Files |

Then three lines:
"Total testable units: N"
"Total files: N"
"The read rule: an argument is called when [condition]."

Rules:
- Placement is coverage, never a test axis. Do not count ratios as variants.
- Every argument gets the same number of concepts unless you state why.
- If capacity does not cover the funded arguments, cut arguments rather than
  cutting concepts per argument. Half a test is not a test.
```

## The cut rule is the whole skill

When capacity is short, every team cuts concepts per argument, because dropping
an argument feels like giving up on an idea. It is exactly backwards. Four
arguments with one concept each produces four unreadable results. Two arguments
with two concepts each produces two answers, and answers compound into the next
cycle.

## What to do with it

The plan goes on the wall for the cycle. `set-reader` reads against the read
rule stated here, and `argument-census` checks the resulting live set against
the plan. If the two disagree, something shipped that nobody designed.
