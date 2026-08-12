---
name: cycle-kickoff
description: Check that everything the cycle depends on actually exists before anyone starts, which is a five minute skill that prevents most mid cycle stalls.
---

# Cycle Kickoff

## The output

A readiness table. Green or blocked, with the blocker named.

## The prompt

```
Below is the state of the config folder, the last cycle's outputs and the
capacity for this cycle.

STATE: [PASTE]

Check readiness. Emit only:

| Requirement | Status | Blocker | Who unblocks |

Requirements, all of them:
  Ingredient file complete, all eleven fields
  Character budgets measured against the live templates
  Layout grid built at every ratio in the matrix
  Ratio matrix current for the placements being run
  Proof inventory refreshed, clearance resolved
  Offer bar approved and current
  Last cycle's iteration brief written
  Capacity confirmed in assets, not hours

Status: READY, STALE with the age, or MISSING.

Then one line: "Cycle status: GO or BLOCKED ON N."

A STALE requirement blocks if it is older than one cycle.
```

## The one that blocks most often

Character budgets, because templates change and nobody re-measures. A cycle that
starts with stale budgets ships truncated files that pass export and fail
silently in the account, and the read is contaminated for the whole flight. It
takes fifteen minutes to re-measure and it belongs here rather than in a
retrospective.

## What to do with it

BLOCKED goes to the operator as a single list with owners, before any research
starts. Nothing downstream should begin against a blocked cycle, because every
seat after this one assumes these inputs are current.
