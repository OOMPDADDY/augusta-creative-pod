---
name: argument-brief
description: Turn one funded argument into a one page brief that a designer, editor and creator can all work from without asking a follow up question.
---

# Argument Brief

## The output

One page. Nine fields. No preamble.

## The prompt

```
Below is a funded argument with its bound proof, evidence and stress test.

ARGUMENT: [PASTE]

Write the brief. Exactly these nine fields, in this order, nothing else:

ARG_ID          the identifier this argument carries for its whole life
THE CLAIM       one sentence, the thing we are asserting
WHO IT IS FOR   the entry point situation, not a demographic
THE PROOF       the specific evidence, with its grade
THE OPENING     what the first two seconds must establish
THE OBJECTION   the one thing this must pre-empt
WHAT IT IS NOT  the nearest argument this must not drift into
CONCEPT COUNT   how many distinct concepts test this argument
HELD CONSTANT   what stays identical across those concepts so the read is clean

Every field is mandatory. If a field cannot be filled from the source, write
[OPERATOR: SET THIS]. Never estimate.
```

## The two fields people skip

WHAT IT IS NOT is what stops three funded arguments collapsing into one by the
time they are edited, which is the single most common way a test set produces no
learning. HELD CONSTANT is what makes the result readable at all. Without it you
have four assets that differ in six ways and a result you cannot attribute.

## What to do with it

This brief is the handoff. `static-spec`, `shot-sheet`, `hook-bank` and
`talent-brief` all read from it and none of them should need anything else. If
they do, the brief was incomplete and the fix belongs here.
