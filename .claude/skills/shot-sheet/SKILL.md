---
name: shot-sheet
description: Turn one argument into a numbered shot list a creator or an editor can film against, with duration and purpose per shot.
---

# Shot Sheet

## The output

A numbered shot list with a running duration.

## The prompt

```
Below is the argument brief, the chosen hook, and the proof.

BRIEF: [PASTE]
HOOK: [PASTE]

Emit only:

| # | Shot | Duration | Purpose | Audio | Must have |

Purpose: HOOK, CONTEXT, PROOF, OBJECTION, PAYOFF or CTA.
Audio: SPOKEN with the line, VO with the line, or AMBIENT.
Must have: the one thing that has to be visible or the shot is a reshoot.

Rules:
- Total runtime under 30 seconds. Show the running total on a final line.
- The PROOF shot is mandatory and must show the proof happening, not a caption
  stating it.
- Every shot is filmable with one person, the product, and a phone.
- Number shots continuously. Do not group them into scenes.
```

## The must-have column

Every reshoot in creative production traces back to a shot that was filmed
correctly and missed one detail: the label was turned away, the hands covered
the seam, the before state was never captured. Naming the one thing per shot
turns a reshoot into a retake while the creator is still standing there.

## What to do with it

Goes to `talent-brief` if a creator is filming it, or straight to the editor if
it is being cut from existing footage. `export-check` verifies the PROOF shot
survived the edit, because it is the one most often cut for time.
