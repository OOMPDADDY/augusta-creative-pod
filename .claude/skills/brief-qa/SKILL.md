---
name: brief-qa
description: Audit a brief before production starts, checking for the six defects that make a set unreadable after the money is spent.
---

# Brief QA

## The output

A pass or fail against six checks, with the specific defect quoted.

## The prompt

```
Below is a set of argument briefs about to go into production.

BRIEFS: [PASTE]

Run six checks across the whole set.

1. DISTINCT       would a buyer hear these as different claims, or as one claim
                  in several outfits
2. PROVEN         every claim bound to cleared evidence
3. READABLE       one variable per test, held constant stated and identical
4. FILMABLE       every opening describable as a shot, not a concept
5. IN BUDGET      every string fits the measured character budget
6. COMPLETE       no [OPERATOR: SET THIS] left unresolved

Emit only:

| Check | Result | Failing brief | The specific defect |

Then one line: "N of 6 pass. Production status: GO or HOLD."

Quote the actual defective text. Never summarize it.
```

## Check one catches the expensive failure

Four briefs that a buyer would hear as one claim produce a full cycle of spend
and no learning, and this is the single most common defect in funded sets. It is
also invisible to the people who wrote them, because the authors know the
distinctions they intended. Reading them as a stranger, in one pass, side by
side, is what surfaces it.

## What to do with it

HOLD means production does not start. The fix is almost always cutting a brief
rather than editing one, and cutting is cheap here and expensive after a shoot.
