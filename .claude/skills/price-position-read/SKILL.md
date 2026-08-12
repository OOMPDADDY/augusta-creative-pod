---
name: price-position-read
description: Establish where this product sits on price against the category, so creative stops apologizing for a premium or wasting a bargain.
---

# Price Position Read

## The output

A position line and the creative implication that follows from it.

## The prompt

```
Below are competitor products and prices, plus this product's price.

SOURCE: [PASTE]

Emit only:

| Brand | Product | Price | Unit price | Position |

Position: LOWEST, BELOW MEDIAN, AT MEDIAN, ABOVE MEDIAN or HIGHEST.

Then three lines and nothing more:
"This product sits: [position], at [X]% of category median."
"The price objection to expect: [one sentence]"
"The creative job: [JUSTIFY, IGNORE or LEAD]"

JUSTIFY if above median, IGNORE if at median, LEAD if lowest and the gap is
over 20%.
```

## Why this belongs in the creative pod

Price position decides how much of every asset gets spent on justification. A
brand at 140% of category median that runs the same creative as a brand at
median will lose, not because the ad is worse, but because it left the biggest
objection unaddressed. This is a thirty second skill that changes every brief
downstream.

## What to do with it

If the creative job is JUSTIFY, at least one concept in every set must carry the
grade A proof from `proof-inventory` in the first three seconds. If it is LEAD,
price goes in the headline and stays there.
