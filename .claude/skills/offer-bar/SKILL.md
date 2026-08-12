---
name: offer-bar
description: Write the closing bar of every asset, the offer and CTA, so it is consistent across the set and never invented per file.
---

# Offer Bar

## The output

One approved offer bar per placement, with character counts.

## The prompt

```
Below is the live offer, the guarantee, the price position read and the
character budgets for CTA fields.

SOURCE: [PASTE]

Write the offer bar variants.

Emit only:

| Placement | Offer line | CTA | Chars | Fits? | Risk reverser |

Rules:
- The offer line states the actual live offer. Never invent, round or improve
  the terms.
- Risk reverser is the guarantee or returns policy in five words or fewer, or
  NONE if the brand has none.
- If the price position read said JUSTIFY, the risk reverser is mandatory on
  every placement.
- Every string carries its real character count against its budget.
- No urgency language unless the deadline is real and stated in the source.
```

## Why this is centralized

When each asset writes its own closing bar, a set of twelve ships with nine
different offer phrasings, two of which overstate the terms. It is the single
most common source of compliance trouble in DTC creative, and it happens because
the bar is treated as the least important part of the file.

## What to do with it

Locked for the cycle. `static-spec` and `ugc-script` both read from it rather
than writing their own. `export-check` verifies the shipped bar matches this
table exactly.
