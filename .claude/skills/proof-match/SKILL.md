---
name: proof-match
description: Bind every candidate argument to a specific piece of cleared evidence, and refuse the ones that have none.
---

# Proof Match

## The output

A binding table, and an explicit list of the arguments that failed.

## The prompt

```
You have two inputs.

CANDIDATE ARGUMENTS: [PASTE]
PROOF INVENTORY (with grades and clearance): [PASTE]

Bind each argument to its proof.

Emit only:

| Argument | Bound proof | Proof grade | Cleared? | Verdict |

Verdict:
  READY        grade A or B proof, cleared
  NEEDS CLEAR  proof exists, clearance UNKNOWN
  UNPROVEN     no proof in the inventory supports this

Then a second block titled "UNPROVEN, do not brief:" listing those arguments
with one line each on what evidence would unlock them.

Never bind an argument to proof that does not directly support it. A related
proof is not a match.
```

## The rule this enforces

An argument without proof still gets made, it just gets made by an editor at
eleven at night with a stat they found on the brand's homepage. Binding the
proof at the argument stage is the only place in the process where this is cheap
to catch. After the brief it costs a reshoot.

## What to do with it

Only READY rows go to `argument-brief`. NEEDS CLEAR rows go to the operator as a
single batched question, which is far easier to answer than five separate ones.
The UNPROVEN block is a genuinely useful document for the brand even though it
briefs nothing.
