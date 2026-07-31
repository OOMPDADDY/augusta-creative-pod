---
name: persona-brief
description: Turn the evidence tables into a one-page buyer-state brief describing the moment the argument lands, not a demographic. Use between the angle-architect and the brief-writer.
---

# Persona Brief

A demographic is not a buyer state. "Women 35 to 54" tells you nothing about
when someone is ready to hear a claim. This produces the moment instead.

## The prompt

```
From the evidence below, describe the buyer state for [ARG_ID].

CUSTOMER EVIDENCE: [PASTE SEAT 1]
OBJECTIONS: [PASTE OBJECTION READ]

Emit, in under 250 words:

THE MOMENT: when this argument becomes relevant. A situation, not a person.
WHAT THEY ALREADY BELIEVE: quoted from the evidence.
WHAT THEY HAVE ALREADY TRIED: and why it did not hold.
WHAT WOULD MAKE THEM SCROLL PAST: be specific and unflattering.
THE SENTENCE THEY WOULD SAY: one line, in their words, from the corpus.

Rules: no demographics unless the evidence forces one. No invented psychology.
Every claim traceable to a quote. No commentary.
```

The WHAT WOULD MAKE THEM SCROLL PAST field is the useful one. Most persona docs
only describe the version of the buyer who is already interested.
