---
name: ingredient-file
description: Build the one structured source of truth every seat reads from: eleven fields per product, filled once. Use before any seat runs. Triggers on "ingredient file", "set up a product", "new product".
---

# Ingredient File

Every seat needs the same facts about the product, and in most operations each
one gets them re-typed by a different person from a different memory. This is
one structured document every prompt reads from. Boring to build, and the reason
everything else works.

## The eleven fields

```
PRODUCT: [name, one line of what it physically is]
PRICE: [price, and the comparison price if there is one]
CATEGORY: [the shelf a buyer would put it on]
PRIMARY CLAIM: [the one thing you would say if you got one sentence]
PROOF FOR THAT CLAIM: [what makes it true. test, ingredient, spec, guarantee]
SECONDARY CLAIMS: [up to four, each with its own proof line]
BUYER IN THEIR WORDS: [6 to 10 verbatim review lines, unedited, typos kept]
TOP OBJECTION: [the reason people do not buy, verbatim if you have it]
WHAT IT IS NOT: [the adjacent thing people mistake it for]
FORMAT CONSTRAINTS: [ratios you run, brand fonts, hex codes, logo rules]
DO NOT SAY: [claims legal or the platform will not allow]
```

## The two fields that do most of the work

BUYER IN THEIR WORDS separates output that sounds like a customer from output
that sounds like a brand. It must be verbatim. Clean up the grammar and you have
deleted the thing you were harvesting.

DO NOT SAY stops you generating a hundred assets you cannot run. In a supplement
or skincare category that field is the difference between a working build and a
wasted afternoon.

Save to `config/ingredient-file.md`. Every seat reads it from there.
