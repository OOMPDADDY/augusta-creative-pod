---
name: asset-registry
description: Maintain the one table that maps every shipped file back to its argument, concept and cycle, which is what makes any read possible later.
---

# Asset Registry

## The output

One row per shipped file. The registry is the memory of the whole operation.

## The prompt

```
Below are the files shipped this cycle with their specs, plus the current
registry.

SHIPPED: [PASTE]
REGISTRY: [PASTE]

Add the new files. Emit the updated registry only:

| File | ARG_ID | CONCEPT_ID | Ratio | Cycle | Format | Shipped | Status |

Status: LIVE, PAUSED, KILLED or ARCHIVED.

Rules:
- File name must match [ARG_ID]-[CONCEPT_ID]-[ratio]. Flag any that do not.
- Never overwrite an existing row. Update its Status only.
- Flag any ARG_ID in the registry that has no corresponding argument brief.

Then one line: "N live, N paused, N killed. Unregistered files: N."
```

## The unregistered count is the health metric

Files that reach the account without a registry row cannot be read, cannot be
attributed to an argument, and quietly corrupt every roll up that follows. In
most accounts we pick up, a meaningful share of live spend sits against files
nobody can trace to a brief. That number, tracked over cycles, is the single
best indicator of whether the operation is a system or a queue.

## What to do with it

`ncr-per-argument` reads from this table, which is why it has to be current
before any read runs. Unregistered files go on `kill-list` as OFF PLAN unless
someone can produce the brief.
