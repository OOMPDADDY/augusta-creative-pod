---
name: argument-scorer
description: Score every candidate argument on demand, proof and saturation so funding decisions are made on one comparable scale.
---

# Argument Scorer

## The output

A scored table, sorted, with the arithmetic visible.

## The prompt

```
Below are candidate arguments with their customer evidence, bound proof and
category saturation scores.

CANDIDATES: [PASTE]

Score each on three axes, 0 to 5, and show your reasoning in one short clause
per axis.

DEMAND    how much customer evidence supports it. 0 is none, 5 is the most
          recurring theme in the research.
PROOF     the grade of the bound evidence. A is 5, B is 3, C is 1, none is 0.
SATURATION INVERTED. A saturated claim scores low. 5 means nobody runs it.

Emit only:

| Argument | Demand | Proof | Saturation | Total | Why (one clause) |

Sort by Total, highest first. Do not round in the brand's favor.
```

## Why three axes and not more

Every extra axis makes the score feel more rigorous and the decision less clear.
These three are the ones that independently predict whether an argument is worth
funding: somebody wants it, you can prove it, and it is not already being
shouted by five competitors. Anything else is a reason to like an idea rather
than a reason to fund it.

## What to do with it

Fund the top three to five. Send the rest to `kill-list` rather than a backlog,
because an unfunded argument sitting in a document gets rediscovered every
quarter and re-argued from scratch.
