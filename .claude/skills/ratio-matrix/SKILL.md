---
name: ratio-matrix
description: Fix which ratios ship to which placements, and enforce that placement is coverage rather than a test axis. Use before any bulk export.
---

# Ratio Matrix

## The rule this enforces

Placement is coverage. It is not a test axis.

Running the same concept at five ratios is not five tests. It is one test,
delivered properly. Treating ratios as variants is how a set of a hundred files
reports twenty winners and teaches you nothing.

## The matrix

```
PLACEMENT | RATIO | REQUIRED?
Feed             | 1:1   | yes
Stories/Reels    | 9:16  | yes
Right column     | 1:1   | no
In-stream video  | 16:9  | only if video
...
```

Fill it once for your account. Every concept ships at every REQUIRED ratio, and
the file name carries the ratio so Seat 10 can collapse them back into one
concept when it reads.

## Naming

`[ARG_ID]-[CONCEPT_ID]-[ratio]`

Seat 10 groups on ARG_ID and de-duplicates on CONCEPT_ID. Without the ratio
suffix it cannot tell five placements of one concept from five concepts.

Save to `config/ratio-matrix.md`.
