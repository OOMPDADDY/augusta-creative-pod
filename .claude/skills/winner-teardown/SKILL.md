---
name: winner-teardown
description: Take apart a winning asset into its transferable components, so the next set inherits the win rather than reprinting it.
---

# Winner Teardown

## The output

A component table separating what transfers from what does not.

## The prompt

```
Below is a winning asset with its performance, its brief, its shot sheet and
its spec.

WINNER: [PASTE]

Take it apart. Emit only:

| Component | What it was | Transferable? | Transfers to |

Components, all of them: ARGUMENT, OPENING SHOT, SPOKEN HOOK, PROOF TREATMENT,
OBJECTION HANDLING, PACING, TALENT, SETTING, OFFER BAR, FORMAT.

Transferable: YES if it would work against a different argument, NO if it only
works because of this specific argument, UNKNOWN if untested.

Then two lines:
"The transferable win: [the one component most likely responsible]"
"The next test: [what to hold constant and what to vary to confirm it]"

Do not credit every component. Most of them were neutral.
```

## Against reprinting the winner

The standard response to a winner is fifteen near copies, which produces a brief
lift and then a fatigue curve, because the audience saw the same argument
fifteen times. The useful response is identifying which single component carried
it and testing that component against a different argument. That is how a win
compounds instead of decaying.

## What to do with it

The transferable component goes into the next `argument-brief` as a fixed
element. The confirming test goes to `test-design`. Log the finding, because a
transferable component is durable brand knowledge and survives every agency
change.
