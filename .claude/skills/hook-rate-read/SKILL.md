---
name: hook-rate-read
description: Read hook rate across the set to separate a bad argument from a bad opening, which are fixed in completely different places.
---

# Hook Rate Read

## The output

A hook rate table with one diagnosis line.

## The prompt

```
Below is every live asset with three second video plays over impressions, and
the argument each one carries.

DATA: [PASTE]

Emit only:

| Asset | ARG_ID | Hook rate | vs set median | Hook type | Read |

Read:
  OPENING WINS    well above median
  OPENING LOSES   well below median
  FLAT            within 10% of median

Then group by ARG_ID and emit a second table:

| ARG_ID | Assets | Median hook rate | Spread | Diagnosis |

Diagnosis:
  ARGUMENT PROBLEM   every asset for this argument is below set median
  EXECUTION PROBLEM  wide spread inside one argument
  HEALTHY            at or above median with tight spread

Never diagnose an argument on fewer than two assets. Write INSUFFICIENT.
```

## The distinction that saves money

An argument nobody stops for and an opening nobody stops for look identical in
the account and cost completely different amounts to fix. If every asset for an
argument underperforms, the argument is wrong and no amount of new hooks will
save it. If one asset in four underperforms, the hook was wrong and the argument
is fine. Teams routinely rewrite hooks for a month against a dead argument.

## What to do with it

EXECUTION PROBLEM goes back to `hook-bank`, which already holds fifteen unused
hooks for that argument. ARGUMENT PROBLEM goes back to `argument-scorer`, and
the argument goes on the `kill-list`.
