---
name: kill-list
description: Name the arguments and assets to stop running, with the reason attached, so budget moves instead of accumulating.
---

# Kill List

## The output

A kill list with a reason per row and a released budget total.

## The prompt

```
Below is every live asset with its argument, spend, and performance to date,
plus the current test plan.

LIVE SET: [PASTE]

Emit only:

| Asset | ARG_ID | Spend | Reason to kill | Confidence |

Reason to kill:
  LOST         underperformed on a fair read
  FATIGUED     was a winner, metrics are decaying
  REDUNDANT    duplicates a stronger asset making the same argument
  UNREADABLE   differs from its siblings in too many ways to learn from
  OFF PLAN     running against an argument nobody funded

Confidence: HIGH, MEDIUM or LOW, based on whether it has had a fair read.

Then one line: "Budget released: $N across N assets."

Never kill an asset with under a fair read. Mark it WAIT instead.
```

## Why REDUNDANT and UNREADABLE are on the list

Most kill lists only carry losers. The expensive rows are the other two. A
redundant asset splits spend across two files making one argument, so both look
mediocre and the argument gets blamed. An unreadable asset burns budget
producing a result nobody can attribute, which is worse than a loss, because a
loss at least teaches you something.

## What to do with it

The released budget figure is the point. It goes to the operator alongside the
next set, so the conversation is about reallocation rather than a new request.
Augusta never changes spend. The brand or their buyer acts on this.
