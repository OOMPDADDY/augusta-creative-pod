---
name: white-space-finder
description: Cross the customer evidence against the category claim map and name the arguments customers make that nobody is running.
---

# White Space Finder

## The output

A ranked white space list. Every row is an argument with demand and no supply.

## The prompt

```
You have two inputs.

CUSTOMER EVIDENCE (phrases, triggers, switching reasons, anxieties):
[PASTE]

CATEGORY CLAIM MAP (what competitors run):
[PASTE]

Find the WHITE SPACE: arguments with evidence of customer demand and no
corresponding claim in the category map.

Emit only:

| Argument | Customer evidence | Closest category claim | Gap type |

Gap type:
  OPEN     nothing in the category is close
  ADJACENT the category runs something near it but weaker or narrower
  BURIED   one brand runs it but not as a primary claim

Rank OPEN first, then ADJACENT, then BURIED.

An argument with no customer evidence is not white space, it is a guess. Leave
it out.
```

## The discipline

White space is only valuable when it has demand behind it. Empty ground with no
customers standing on it is empty for a reason, and every category has some.
This is why the skill requires both inputs and refuses to run on one.

## What to do with it

The top three OPEN rows go straight to `argument-scorer`. If nothing comes back
OPEN, that is a real finding: the brand competes on proof and execution rather
than on a new argument, and the set should be briefed accordingly.
