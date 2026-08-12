---
name: proof-inventory
description: List every piece of proof the brand can legitimately put on screen, graded by strength, so no concept gets briefed against evidence that does not exist.
---

# Proof Inventory

## The output

A graded inventory. One row per available proof asset.

## The prompt

```
Below is everything the brand can evidence: test results, certifications,
review counts and ratings, sales volumes, press, named customers, guarantees,
founder credentials, demonstrations that can be filmed.

SOURCE: [PASTE]

Emit only:

| Proof | Type | Strength | Cleared for ads? | Shows on camera? |

Type: DEMONSTRATION, THIRD PARTY, VOLUME, CREDENTIAL, GUARANTEE or TESTIMONIAL.
Strength: A if a skeptic would accept it without follow-up, B if it needs a
  qualifier, C if it is suggestive only.
Cleared for ads: YES, NO or UNKNOWN. Default to UNKNOWN.
Shows on camera: YES if it can be filmed happening, NO if it can only be stated.

Never upgrade a grade. Never write a proof that is not in the source.
```

## The two columns that decide the set

A grade A proof that shows on camera is the most valuable asset a brand owns,
and most brands have one and never use it. A grade C proof that can only be
stated is a caption, not a concept. Sorting on those two columns tells you what
the set can actually claim before anyone writes a headline.

## What to do with it

Every argument going into `proof-match` must land against a row here. An
argument with no matching proof is either dropped or briefed as a question
rather than a claim.
