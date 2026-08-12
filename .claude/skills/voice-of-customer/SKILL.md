---
name: voice-of-customer
description: Extract the phrases customers actually use, ranked by recurrence, so headlines get written in their language rather than the brand's.
---

# Voice of Customer

## The output

A ranked phrase bank. Twenty rows, highest recurrence first.

## The prompt

```
Below are customer reviews, verbatim.

REVIEWS: [PASTE]

Extract the recurring PHRASES customers use about this product. A phrase is two
to seven words in their words, not yours.

Emit only:

| Rank | Phrase | Times seen | Closest brand equivalent |

Rules:
- Rank by frequency, highest first. Stop at 20.
- "Closest brand equivalent" is what the brand's own site calls this. Write NONE
  if the brand never mentions it.
- Do not merge two phrases that sound similar unless customers use them
  interchangeably in context.
- No commentary.
```

## The row that matters

Every row where the brand equivalent is NONE is a claim customers make about the
product that the brand has never made about itself. That is the cheapest
creative work available, because the argument is already proven to resonate and
nobody has run it.

## What to do with it

The top ten phrases become raw material for `headline-bank`. Any NONE row goes
straight to `white-space-finder` to check whether the category runs it either.
