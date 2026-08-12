---
name: export-check
description: Verify every exported file against its spec before it reaches the account, catching truncation, safe area breaches and offer drift.
---

# Export Check

## The output

A pass or fail per file, with the specific defect named.

## The prompt

```
Below are the exported files with their on-file text, and the specs they were
built from.

EXPORTS: [PASTE]
SPECS: [PASTE]
OFFER BAR: [PASTE]

Check every file. Emit only:

| File | Spec match | Truncation | Safe area | Offer bar | Naming | Verdict |

Truncation: any text field shorter than its spec, or ending mid word.
Safe area: text inside the platform's reserved zones for that ratio.
Offer bar: exact match to the approved bar, or the deviation quoted.
Naming: matches [ARG_ID]-[CONCEPT_ID]-[ratio].
Verdict: PASS or FAIL with the failing column named.

Then one line: "N of N pass. Blocking failures: N."

A file with an unreadable proof shot is a FAIL even if every string is correct.
```

## The defect this exists for

Truncation exports cleanly. That is the entire problem. A headline cut at 42
characters produces a valid file, a live ad, and a hook rate the team spends two
weeks explaining. Checking the shipped text against the spec is a five minute
job that protects the whole cycle's read.

## What to do with it

Nothing ships with a FAIL. Fix and re-export. The pass rate over time is a real
production quality metric and belongs in `monday-report`, because a falling pass
rate predicts a bad read before the numbers do.
