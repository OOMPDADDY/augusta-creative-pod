---
name: competitor-ad-pull
description: Turn a raw pull from the public ad libraries into a structured table of what the category is actually running right now.
---

# Competitor Ad Pull

## The output

One row per live competitor ad, with its argument named.

## The prompt

```
Below are competitor ads pulled from the public ad library, with their copy,
format and run dates.

ADS: [PASTE]

Emit only:

| Brand | Format | Days live | Headline | The argument it makes | Angle type |

Days live: from the library's start date to today. If missing, write UNKNOWN.
The argument: one sentence, the claim the ad is actually making, not a
  description of the visual.
Angle type: PRICE, QUALITY, SPEED, SOCIAL PROOF, FEAR, IDENTITY, CONVENIENCE,
  NOVELTY or OTHER.

No commentary. If two ads make the same argument, they still get their own row.
```

## Read days live before anything else

Days live is the only free performance signal in the whole category. Nobody
funds a losing ad for ninety days. An ad that has been running since March is a
winner, and the argument it makes is a funded argument. Sort by that column
before you read a single headline.

## What to do with it

Feed the whole table to `category-claim-map` and `claim-saturation`. Anything
running over sixty days goes to `argument-scorer` as proven category demand.
