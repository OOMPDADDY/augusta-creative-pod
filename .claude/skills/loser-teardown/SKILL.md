---
name: loser-teardown
description: Establish why an asset lost before writing it off, because half of losses are production defects rather than wrong arguments.
---

# Loser Teardown

## The output

A cause of death, with the evidence for it.

## The prompt

```
Below is an underperforming asset with its performance, brief, spec, shot sheet
and export check result.

LOSER: [PASTE]

Work through the causes in this order and stop at the first that fits.

1. DEFECT       failed export check, truncated text, unreadable proof, wrong
                offer bar, safe area breach
2. UNREADABLE   differed from its siblings in more than one way, so the result
                cannot be attributed
3. UNDER READ   did not receive enough impressions for a fair read
4. EXECUTION    hook or pacing lost them, argument untested
5. ARGUMENT     every asset for this argument underperformed

Emit only:

| Cause | Evidence | Confidence | Fix | Cost to fix |

One row. Then one line: "Verdict: [cause]. This argument is [DEAD, UNTESTED or
ALIVE]."

An argument is only DEAD if the cause is ARGUMENT. Everything else leaves it
untested.
```

## The order is the point

Teams diagnose losers by starting at the argument, because that is the
interesting conversation. Most of the time the answer is further up: the file
was truncated, or it never got a fair read, or it differed from its siblings in
three ways. Working the list in order stops good arguments getting killed for
production defects, which is the most expensive mistake in the whole cycle.

## What to do with it

DEFECT goes to `export-check` and the process gets fixed, not the argument.
UNREADABLE goes to `test-design`. Only an ARGUMENT verdict reaches `kill-list`.
