---
name: headline-bank
description: Generate a full headline bank for one argument across four structures, written to the real character budget so nothing breaks on export.
---

# Headline Bank

## The output

Forty headlines for one argument. Ten in each of four structures, all inside
budget.

## The prompt

```
Below is one argument brief and the character budgets for the target templates.

BRIEF: [PASTE]
CHARACTER BUDGETS: [PASTE]

Write 40 headlines for this argument. Ten in each structure:

DIRECT CLAIM     states the claim flatly
QUESTION         asks the thing the buyer is already wondering
SITUATION        opens on the entry point moment, not the product
CONTRAST         sets what they have against what this is

Emit only:

| # | Structure | Headline | Chars | Fits? |

Rules:
- Every headline makes the SAME argument. Different phrasing, same claim.
- Chars is the actual count. Fits is YES or NO against the budget given.
- Use the customer's phrase bank language where it fits naturally.
- Never write a headline that needs a subhead to make sense.
- No headline may use the pattern "Not X. Y."
```

## Forty, and all one argument

The instinct is to spread forty headlines across four arguments so the set feels
broad. That produces forty assets and zero learning. Forty phrasings of one
argument is how you find out whether the argument works, separately from whether
the wording did, and the phrasing winner transfers to the next argument for free.

## What to do with it

The top ten by the operator's read go into `static-spec`. Keep the whole bank,
because the bank is what makes the next iteration take twenty minutes rather
than a day.
