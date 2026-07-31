# The Creative Pod

Ten seats that run a creative pod end to end, as Claude Code agents and skills.
Clone it, drop in your keys, run the cycle.

Built by [Augusta Productions](https://augustaproductionsllc.com), performance
creative for DTC brands. It is the run order we use, written down. Free, and
yours to adapt.

---

## What this actually is, and what it is not

**It is** ten agent definitions and ten skills that encode a creative testing
cycle: read the customer, read the category, decide the argument, brief it, spec
the statics, list the shots, write the hooks, brief the talent, check every
export, read the result back. Each one is a real, runnable prompt with a defined
input and a defined output, and the outputs chain.

**It is not** a set of integrations. This repo does not ship connectors for
Canva, Figma, Frame.io or anything else. Where a seat needs a tool, it names the
MCP server you point it at and you supply it. See [MCP](#mcp-optional) below.
Anyone telling you a folder of prompts is "wired into" nine SaaS products is
selling you something.

**The eleventh seat is not in here.** Ten seats ship. A real pod has eleven, and
the eleventh is the director: the person who looks at nine ranked arguments and
says "these four, and here is why." It is not withheld as an upsell and it is not
hard to write. It is left out because it was never the bottleneck. Nobody's
creative operation was ever slow because the director was slow. It was slow
because a brief sat in a queue, a designer was booked, nobody had read the
reviews, and the export check slipped. Those are the ten seats below, and they
are now genuinely fast.

---

## Setup

Requires [Claude Code](https://claude.com/claude-code).

```bash
git clone <this repo>
cd creative-pod
cp .env.example .env          # only needed if you wire MCP servers
mkdir -p config output
claude
```

Then, in Claude Code:

```
/agents        # confirm the ten seats loaded
```

That is the whole install. The agents and skills are plain markdown in
`.claude/`; there is nothing to build and no dependencies.

---

## The run order

The pod is a sequence, not a menu. Seat 3 produces the thing seats 4 through 8
all read from, so run it in order the first time.

| Seat | Agent | Job |
|---|---|---|
| 1 | `review-miner` | Reads your customers, returns their words |
| 2 | `category-mapper` | Reads the category, returns argument density |
| 3 | `angle-architect` | Ranks what is worth arguing, assigns ARG_IDs |
| 4 | `brief-writer` | One page per argument, against the real number |
| 5 | `static-speccer` | Argument to autofill-ready spec table |
| 6 | `shot-lister` | Argument to a runnable four-shot sheet |
| 7 | `hook-writer` | Seven structures for the first three seconds |
| 8 | `talent-briefer` | Creator briefs that argue rather than hold |
| 9 | `export-checker` | Seven checks against every finished file |
| 10 | `set-reader` | Reads what ran, by argument, and hands back to Seat 3 |

Seat 10 hands back to Seat 3. That backward edge is the only structural
difference between a pod and a production line. A production line ships assets;
a pod learns what to ship next.

### The ten skills

Support work the seats call on: `ingredient-file`, `objection-read`,
`persona-brief`, `character-budgets`, `layout-grid`, `ratio-matrix`,
`fatigue-watch`, `coverage-audit`, `argument-census`, `monday-report`.

Build `ingredient-file`, `character-budgets` and `layout-grid` before your first
cycle. They are one-time and everything downstream assumes they exist.

---

## The ARG_ID contract

Seat 3 assigns an ID to every argument. Every seat after it carries that ID
through, and shipped files are named:

```
[ARG_ID]-[CONCEPT_ID]-[ratio]        e.g.  A3-A3-C2-1x1
```

This is the only reason Seat 10 can answer **"which argument won"** rather than
**"which file won"**, and the second question is not worth asking. Break the
naming convention and the read at the end of the cycle silently stops working
while still producing a confident-looking table.

---

## A first cycle, end to end

```
1. /ingredient-file           fill the eleven fields for one product
2. use the review-miner       on your last 500 reviews, raw
3. use the category-mapper    on 25 competitor listings with run durations
4. use the angle-architect    on both outputs
5. strike every argument you would not defend out loud. Keep four.
6. use the brief-writer       on each survivor
7. use the static-speccer and shot-lister on the strongest
8. use the export-checker     on every file. Every one.
9. ship to your buyer
10. use the set-reader        weekly, and send the finding back to step 4
```

First full pass is an afternoon, most of it gathering. After that, a cycle is a
morning and the weekly rhythm is Seat 10 on Monday.

---

## MCP (optional)

Seats 1, 2 and 10 are more useful with live data. `.mcp.json.example` has the
shape; you supply the servers.

**We do not vendor MCP servers and we do not endorse specific packages.** Pick
your own, read its source, and scope it yourself. That last part matters:

> **Seat 10 is read-only by design.** If you connect an ads MCP server, grant
> read scope only. There is no part of this pod that needs permission to change
> a budget, a bid or a status. Augusta does not run media buying and this repo
> is scoped so it cannot. Your media buyer owns the spend.

Never put a token in `.mcp.json`. Use the environment, and keep `.env`
gitignored.

---

## Where this stops

The ten seats give you the sequence. Pointing them is the craft: which argument,
which buyer state, which format carries which claim, which result to chase and
which to cut. That does not come in a prompt, and it is the eleventh seat.

There is a second gap, quieter and more expensive: running the cycle every week
without it sliding. The pod does not decay in a dramatic failure. It decays in a
skipped Monday read, then a fortnight where nobody re-ran the category map, then
a quarter where the argument set went stale against a category that moved.

If you would rather have that run for you than run it yourself:
[go.augustaproductionsllc.com/apply](https://go.augustaproductionsllc.com/apply)

---

## Licence

MIT. Use it, fork it, strip the branding, ship it inside your own operation. If
it makes you money, that is the point.
