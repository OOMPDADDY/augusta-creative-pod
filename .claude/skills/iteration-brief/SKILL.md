---
name: iteration-brief
description: Turn one cycle's read into the next cycle's brief in a single pass, so learning carries forward instead of restarting.
---

# Iteration Brief

## The output

The next cycle's plan, on one page, derived entirely from the last read.

## The prompt

```
Below are the winner teardowns, loser teardowns, hook and hold reads, the
revenue per argument table and the kill list.

READS: [PASTE]

Write the next cycle brief. Exactly these sections:

CARRIED FORWARD   arguments that produced, and what they earned
RETIRED           arguments killed, with the cause
UNRESOLVED        arguments that never got a fair read, and what they need
TRANSFERABLE      components proven to work, now fixed elements
NEW CANDIDATES    arguments from research that have not been tested yet
THE TEST          what this cycle is actually asking, in one sentence
HELD CONSTANT     what stays identical so the answer is readable

Every line must trace to something in the reads. Nothing new may be introduced
here that has no evidence behind it.
```

## The section teams skip

UNRESOLVED. Arguments that never got a fair read quietly disappear between
cycles, and six months later somebody proposes one as a fresh idea. Carrying
them explicitly, with what they need, is the difference between a program that
compounds and a program that runs in circles with a new agency every year.

## What to do with it

This is the input to the next `test-design`. Read alongside `argument-census`:
if the census count is not rising over cycles, the program is producing volume
without producing arguments, and this brief is where that gets caught.
