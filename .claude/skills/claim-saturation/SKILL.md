---
name: claim-saturation
description: Score how contested each claim is before you fund creative against it, so spend does not go to the most crowded corner of the category.
---

# Claim Saturation

## The output

A saturation score per claim, and one recommendation line.

## The prompt

```
Below is the category claim map with brand counts and run lengths.

CLAIM MAP: [PASTE]

Score each claim for saturation.

Emit only:

| Claim | Brands | Total ads | Longest run | Saturation score | Verdict |

Saturation score, 0 to 10: brands running it, weighted by ad count and run
length. Show the arithmetic in one short parenthetical per row.
Verdict: ENTER if under 4, ENTER WITH BETTER PROOF if 4 to 7, AVOID if over 7.

Then one line: "Least contested claim with customer demand: [claim]"
```

## The point of scoring rather than eyeballing

Everyone can see that a claim is crowded. What nobody does is compare crowding
against the alternatives on one scale, so the crowded claim keeps getting funded
because it is the one that feels safest. A number makes the comparison happen in
a planning meeting instead of after the flight.

## What to do with it

AVOID claims only get funded if the brand has a grade A proof from
`proof-inventory` that no competitor can match. Everything else routes to
`argument-scorer` with the saturation score attached as an input.
