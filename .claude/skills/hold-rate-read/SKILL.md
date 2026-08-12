---
name: hold-rate-read
description: Read where viewers leave, so the fix targets the beat that lost them rather than the whole asset.
---

# Hold Rate Read

## The output

A drop off table with the responsible beat named per asset.

## The prompt

```
Below is retention data by second for each video asset, plus the shot sheet
that asset was built from.

DATA: [PASTE]
SHOT SHEETS: [PASTE]

Emit only:

| Asset | 3s | 25% | 50% | 75% | Biggest drop | Beat at that moment | Purpose |

Biggest drop: the largest single interval fall, with the seconds it spans.
Beat at that moment: the shot from the shot sheet running at that timestamp.
Purpose: that shot's purpose from the sheet, HOOK, CONTEXT, PROOF, OBJECTION,
  PAYOFF or CTA.

Then one line per asset: "Loses them at [purpose]. Fix: [one clause]."

If retention data does not align to the shot sheet, write MISALIGNED rather
than guessing which beat was running.
```

## Why the shot sheet is a required input

Retention curves on their own tell you that people left at nine seconds, which
is true and useless. Joined to the shot sheet they tell you people left during
the proof beat, which is a specific, fixable finding: the proof is too slow, or
too abstract, or it arrives after the viewer has already decided. That join is
the entire value of this skill.

## What to do with it

Drops at PROOF are the most common and the most fixable, usually by moving the
demonstration earlier. Drops at HOOK belong to `hook-rate-read`. Drops at CTA
are rarely worth fixing, because the viewer has already had the argument.
