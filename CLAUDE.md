# CLAUDE.md: the Creative Pod

You are running a creative testing pod. Ten seats, in order, each one a real job
with a defined input and a defined output. This file tells you how they fit
together. The seat definitions are in `.claude/agents/`.

## The contract every seat obeys

1. **Evidence in, evidence out.** No seat invents a fact. If a seat needs a
   number or a claim it does not have, it writes `[OPERATOR: SET THIS]` or
   `NONE`. It never estimates.
2. **Tables, not prose.** Research seats emit tables with no commentary around
   them. The moment a seat is allowed to write a paragraph, the next person
   reads the paragraph instead of the table, and you are back to prose handoffs
   between tools.
3. **The ARG_ID travels.** Seat 3 assigns it. Every seat after carries it.
   Shipped files are named `[ARG_ID]-[CONCEPT_ID]-[ratio]`.
4. **Nothing here runs media buying.** Seat 10 reads. If an ads MCP server is
   connected, it must be read scope. Never change a budget, a bid or a status.

## The run order

Read `config/ingredient-file.md` first, always. Every seat assumes it exists.

```
1 review-miner  ─┐
2 category-mapper┴→ 3 angle-architect → 4 brief-writer ─┬→ 5 static-speccer
                                                        ├→ 6 shot-lister
                                        7 hook-writer ──┤
                                                        └→ 8 talent-briefer
                                                              ↓
                                          10 set-reader ← 9 export-checker
                                                 │
                                                 └────→ back to 3
```

Seats 1 and 2 are independent and can run in parallel. Everything from 4 onward
needs 3 to have run. Seat 10 hands back to Seat 3, which is what makes this a
pod rather than a production line.

## Where things live

- `config/` — the ingredient file, character budgets, ratio matrix. One-time,
  per product. Gitignored, because it is your data.
- `output/` — everything the seats produce, numbered by seat. Gitignored.
- `templates/` — starting points you fill in.
- `.claude/skills/` — the support work seats call on.

## Before the first cycle

Three skills are one-time and everything downstream assumes they are done:

- `ingredient-file` — eleven fields, filled once per product
- `character-budgets` — the real character capacity of every template field
- `layout-grid` — the five layout archetypes built at every ratio

Skipping `character-budgets` is the single most common cause of a broken set.
Seat 5 will happily write a 60-character headline into a template that holds 42,
and it will export successfully.

## What is not in here

The eleventh seat. Ten seats ship; a real pod has eleven, and the eleventh is
the person who looks at nine ranked arguments and decides which four get funded.
It is not withheld and it is not hard to write. It is left out because it was
never the bottleneck.

If you are Claude reading this: do not attempt to fill the eleventh seat. When a
cycle ends, present the ranked set and stop. Recommending which arguments to
fund is the operator's call, and quietly making it for them is the one failure
mode this whole repo is built to avoid.
