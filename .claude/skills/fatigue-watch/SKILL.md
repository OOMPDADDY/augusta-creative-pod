---
name: fatigue-watch
description: Compare first-week to last-week performance per asset and flag anything sliding past the threshold, so a dying asset is caught as a trend rather than a feeling. Run weekly.
---

# Fatigue Watch

## The rule

If last-7-day CPA is 30% or more worse than first-7-day CPA on the same asset,
that asset is done. Not paused for review. Done.

Replace it from the same ARG_ID group: same argument, new execution. Retiring
the asset is not retiring the argument, and conflating the two is how a working
argument gets abandoned because one execution wore out.

## The prompt

```
For every asset live more than 14 days in the export below, show first-7-day
CPA against last-7-day CPA, and flag anything that has moved more than 30% the
wrong way.

EXPORT: [PASTE]

Emit ONLY: ASSET | ARG_ID | FIRST 7 | LAST 7 | % MOVE | FLAG

Sort by % MOVE, worst first. No commentary.
```

## Why a threshold and not a judgement

Without a number, fatigue gets argued about weekly and acted on monthly. The
threshold is the point: it converts a discussion into a decision.
