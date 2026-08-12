---
name: category-claim-map
description: Collapse every competitor ad into the small number of claims the category actually runs, so you can see the real shape of the conversation.
---

# Category Claim Map

## The output

A claim map. Usually five to nine rows for a category people describe as
crowded.

## The prompt

```
Below is a table of live competitor ads with their arguments.

ADS: [PASTE]

Collapse them into distinct CLAIMS. Two ads make the same claim if a buyer
would hear the same promise, regardless of visual treatment or wording.

Emit only:

| Claim | Brands running it | Ad count | Longest run (days) | Crowding |

Crowding: OWNED if one brand runs it and has for over 90 days, CONTESTED if two
to four brands run it, SATURATED if five or more do.

Then one final line: "Distinct claims in category: N"

No commentary.
```

## What the number tells you

Most categories that feel impossible to enter are running six claims. The
feeling of crowding comes from asset volume, not argument variety. Once the map
is on one page, the open ground is usually visible without any further analysis.

## What to do with it

OWNED claims are expensive to attack and should be avoided unless the brand has
a genuinely better proof. SATURATED claims are where cost per acquisition goes
to die. Send the whole map to `white-space-finder`.
