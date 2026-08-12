---
name: ncr-per-argument
description: Report new customer revenue by argument rather than by asset, which is the only view that tells you what to fund next.
---

# New Customer Revenue Per Argument

## The output

A revenue table by argument, sorted, with cost per new customer beside it.

## The prompt

```
Below is performance by asset with spend, new customer revenue and new customer
count, plus the ARG_ID each asset carries.

DATA: [PASTE]

Roll up by ARG_ID. Emit only:

| ARG_ID | The claim | Assets | Spend | New customer revenue | nCAC | nROAS |

Sort by new customer revenue, highest first.

Then three lines:
"Arguments funded: N. Arguments producing: N."
"Best argument by nROAS: [ARG_ID], [figure]"
"Spend against arguments producing nothing: $N"

Use new customer figures only. If only blended figures are available, say
BLENDED ONLY on every affected row and do not silently mix the two.
```

## Why per argument and not per asset

Asset level reporting rewards whichever file happened to get the impressions and
tells you nothing about what to make next. Argument level reporting answers the
only question that matters at the start of a cycle: which claims produce new
customers, and which ones have we been funding out of habit. It is also the view
that survives a creative refresh, because the assets change and the arguments
persist.

## What to do with it

The last line is the one to read out loud. Spend against arguments producing
nothing is the recoverable budget in the account, and it goes to the operator
with the `kill-list`. Augusta reports it. The brand or their buyer moves the
money.
