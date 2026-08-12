---
name: format-census
description: Count what formats the category is actually running, so format choice becomes a decision rather than a habit.
---

# Format Census

## The output

A format table with the category split and this brand's split beside it.

## The prompt

```
Below are competitor ads and this brand's live ads.

ADS: [PASTE]

Emit only:

| Format | Category count | Category % | This brand count | This brand % | Delta |

Formats: STATIC, UGC VIDEO, PRODUCT DEMO, FOUNDER TO CAMERA, CAROUSEL,
MOTION GRAPHIC, TESTIMONIAL, COMPARISON.

Then one line: "Largest delta: [format], [over or under] indexed by [N] points."

No commentary.
```

## What the delta means, and what it does not

A large delta is a question, not an instruction. Under-indexing on UGC in a
category that runs mostly UGC might mean an opportunity, or it might mean the
brand tried it and it lost. Ask which before briefing. What the delta reliably
catches is the brand running one format because that is what the last agency
sold them.

## What to do with it

Take the largest delta to the operator with one question: was this a decision or
a default. If it was a default, the next set covers the gap. Send the result to
`ratio-matrix` so coverage gets built at every placement the format needs.
