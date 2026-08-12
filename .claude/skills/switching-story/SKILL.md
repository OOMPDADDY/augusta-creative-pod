---
name: switching-story
description: Reconstruct what the customer used before and why they left it, which is the most persuasive structure available in a competitive category.
---

# Switching Story

## The output

A switching table, one row per reconstructed switch.

## The prompt

```
Below are customer reviews.

REVIEWS: [PASTE]

For every review that mentions a prior product, brand, method or workaround,
reconstruct the switch.

Emit only:

| From (their words) | Why they left | What made this one different | Named? |

"Named?" is YES if the customer named a competitor brand, NO if they described a
category ("the drugstore ones", "the one from the big box store").

Include rows where the prior alternative was doing nothing at all. "I just put
up with it" is a switch, and it is often the biggest segment.

Do not infer a switch that is not stated.
```

## The rule about naming

A NO row is usually more useful than a YES. Naming a competitor in an ad invites
a comparison the viewer has to adjudicate, and it hands the competitor free
awareness. The category description does the same persuasive work with none of
the risk. Keep the column anyway, because a cluster of YES rows against one
competitor tells you exactly who you are actually up against.

## What to do with it

The "Why they left" column is the highest converting objection material in the
whole research stage. Feed it to `objection-to-argument`. The "just put up with
it" rows go to `purchase-trigger`, because inertia breaks on a moment.
