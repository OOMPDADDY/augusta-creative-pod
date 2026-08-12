---
name: anxiety-ledger
description: List every reason a warm buyer does not complete the purchase, ranked by how often it surfaces, so creative closes the gap instead of widening the top.
---

# Anxiety Ledger

## The output

A ranked ledger of purchase anxieties with a handling note against each.

## The prompt

```
Below are reviews, support tickets, pre-purchase questions and any comments on
live ads.

SOURCE: [PASTE]

List every ANXIETY: a reason someone who already wants this would still not buy.
Fit, sizing, durability, whether it works for their specific case, how long it
takes, what happens if it does not work, whether it is worth the price.

Emit only:

| Rank | Anxiety | Their words | Where it surfaces | Answerable in creative? |

Where it surfaces: REVIEW, TICKET, PRE-PURCHASE or AD COMMENT.
Answerable in creative: YES if a single asset could resolve it, PARTIAL if it
needs the landing page too, NO if only a policy change fixes it.

Rank by how often it appears. No commentary.
```

## Why this is separate from objections

An objection is a reason to disagree. An anxiety is a reason to delay, and delay
is what actually kills DTC purchases. The person is sold and still does not
click, because they do not know if it fits, or how long the return window is.
Those are information problems rather than persuasion problems, and creative
fixes them faster than a landing page rewrite.

## What to do with it

Every YES row is a candidate asset. Ranks one to three go into the next set as
dedicated concepts, not as a line of small print at the bottom of an existing
one. NO rows go to the operator, because they are a business note rather than a
creative brief.
