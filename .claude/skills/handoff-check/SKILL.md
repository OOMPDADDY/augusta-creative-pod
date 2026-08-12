---
name: handoff-check
description: Verify that one stage's output is genuinely consumable by the next, which is where creative operations actually break.
---

# Handoff Check

## The output

A handoff status per boundary, with what is missing named.

## The prompt

```
Below is the output of one stage and the input contract of the next.

UPSTREAM OUTPUT: [PASTE]
DOWNSTREAM REQUIREMENTS: [PASTE]

Emit only:

| Required field | Present? | Format correct? | Would need a human? |

"Would need a human" is YES if someone has to retype, reformat, interpret or
chase something to move this forward.

Then one line: "Handoff: CLEAN, or BROKEN ON N fields, N of which need a human."

Be strict about format. A table the next stage expects, delivered as prose, is
BROKEN even though the information is present.
```

## Why this exists at all

Two brands running the same tools get results that are not close, and the
difference is almost never the tools. It is whether stage three can read stage
two without a person in the middle rebuilding the file. Every human retype is a
delay, a defect surface and a place where the ARG_ID gets dropped, which is what
makes the final read unattributable.

## What to do with it

Any YES in the last column is a process fix, not a people fix. Fix it in the
upstream prompt so the correct format is produced at source. This is the skill
that keeps the pod a pod rather than ten prompts in a folder.
