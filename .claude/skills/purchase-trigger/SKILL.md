---
name: purchase-trigger
description: Identify the specific moment that made someone buy, so creative can recreate the moment instead of listing features.
---

# Purchase Trigger

## The output

A trigger table. One row per distinct trigger, with the evidence attached.

## The prompt

```
Below are customer reviews and any post-purchase survey responses.

SOURCE: [PASTE]

Find the TRIGGER in each: the specific moment, event or realization that moved
this person from not buying to buying. A trigger is a situation, not a benefit.
"It is durable" is a benefit. "My old one snapped mid-move" is a trigger.

Emit only:

| Trigger | Situation in their words | Count | Recreatable on camera? |

Recreatable on camera: YES if a six second shot could show this situation, NO if
it is internal or abstract. Be strict.

If a review contains no trigger, do not invent one. Leave it out.
```

## Why triggers beat benefits

Benefits ask the viewer to imagine wanting something. Triggers show them a
situation they have already been in, and the wanting arrives on its own. A
category where everyone runs benefits is a category where the first brand to run
triggers has a two second head start on every impression.

## What to do with it

Every YES row is a shot for `shot-sheet` and an opening beat for `ugc-script`.
Triggers with a count above three and no live creative against them go to
`argument-scorer` as candidates.
