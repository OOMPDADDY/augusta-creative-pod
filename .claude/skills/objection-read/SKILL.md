---
name: objection-read
description: Read pre-sale messages and refund reasons to find the objection that actually stops the sale, and decide which ones are safe to raise in creative. Use after the ingredient file, before briefing.
---

# Objection Read

Reviews come from people who bought. Your support inbox comes from people who
nearly did not, and that is where the objection lives.

## The prompt

```
Below are [N] pre-sale customer messages and refund reasons for [PRODUCT].

MESSAGES:
[PASTE, WITH NAMES AND ORDER NUMBERS STRIPPED]

Read them and report. Do not write copy.

Emit ONLY a table:
OBJECTION | HOW OFTEN | VERBATIM | DO WE ANSWER IT? | RAISE IT IN ADS?

RAISE IT IN ADS?: YES only if we can answer it with proof in under 8 words.
  Otherwise NO, plus a three-word reason.

Rules: rank by HOW OFTEN, 6 to 10 rows, quotes uncleaned, no commentary.
```

## Why the last column defaults to NO

This is the opposite of most objection-handling advice. Raising an objection in
a five-second ad only helps if the answer fits in the same five seconds.
Otherwise you have introduced the doubt and run out of room.

Strip names and order numbers before pasting. Nothing personal goes into a
prompt.
