---
name: desire-ladder
description: Map what the customer says they want, what they actually want, and what they would never say out loud, so the set can test all three levels.
---

# Desire Ladder

## The output

A three rung ladder per segment, with a testable line at each rung.

## The prompt

```
Below is customer research: reviews, surveys, and the phrase bank.

SOURCE: [PASTE]

Build a three rung desire ladder.

RUNG 1, STATED: what customers explicitly say they want. Quote them.
RUNG 2, FUNCTIONAL: what that gets them in practice, in plain language.
RUNG 3, UNSPOKEN: the status, identity or relief underneath, phrased the way a
  friend would say it, never the way a marketer would.

Emit only:

| Rung | The want | Evidence | One testable headline |

Rules:
- Rung 3 must be supportable by something in the source. If nothing supports it,
  write NONE. Do not write a poem.
- Each testable headline must be a claim, not a mood.
```

## The trap on rung 3

Rung 3 is where creative teams write things nobody has ever felt. The discipline
is that it still has to be evidenced. If four reviews mention showing it to
someone else, rung 3 is about being seen. If none do, rung 3 is NONE and the
brand tests rungs 1 and 2 like everybody else, which is fine.

## What to do with it

The three rungs become three distinct arguments, not three phrasings of one.
Send them to `argument-scorer`. A set that tests all three rungs learns more in
one flight than a set that tests eight variations of rung 1.
