---
name: review-pull
description: Turn a raw dump of reviews into a clean, deduplicated evidence table the rest of the pod can read. Run once per product, refresh quarterly.
---

# Review Pull

## The output

A table. One row per review, four columns, no commentary.

## The prompt

```
Below is a raw dump of customer reviews. Some are duplicates, some are one
word, some are about shipping rather than the product.

REVIEWS: [PASTE]

Emit a table with these columns and nothing else:

| ID | Verbatim | Subject | Usable |

ID: R001 upward.
Verbatim: the customer's exact words, trimmed to the sentence that carries the
  claim. Never paraphrase. Never fix their grammar.
Subject: PRODUCT, SERVICE, SHIPPING, PRICE or OTHER.
Usable: YES only if the row says something about the product experience that a
  stranger could not have guessed. Everything else is NO.

Drop nothing. Mark it instead. A NO row is evidence that the review set is thin,
and that is worth seeing.
```

## Why verbatim matters

The most expensive habit in creative research is tidying the customer up. "It
arrived and I honestly thought they sent the wrong one, it is so much heavier
than I expected" becomes "customers value quality," and the ad written off the
summary is the ad nobody stops for. The weight detail was the whole asset. Keep
the words.

## What to do with it

Feed the YES rows into `voice-of-customer` and `objection-read`. If fewer than
40 rows come back YES, the review set is too thin to build arguments on, and the
honest answer is to say so before anyone briefs a set.
