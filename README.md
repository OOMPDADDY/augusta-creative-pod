# The Creative Pod

Fifty skills and ten seats that run a creative testing operation end to end, as
Claude Code agents and skills. Clone it, drop in your keys, run the cycle.

Built by [Augusta Productions](https://augustaproductionsllc.com), performance
creative for DTC brands. It is the run order we use across the accounts we work
on, written down. Free, and yours to adapt.

---

## What this actually is, and what it is not

**It is** fifty skills and ten agent definitions that encode a creative testing
cycle: read the customer, read the category, decide the argument, make the set,
read the result. Every skill is a real, runnable prompt with a defined input and
a defined output, and the outputs chain into each other.

**It is not** a set of integrations. This repo does not ship connectors for
Canva, Figma, Frame.io or anything else. Where a seat needs a tool, it names the
MCP server you point it at and you supply it. See [MCP](#mcp-optional) below.
Anyone telling you a folder of prompts is "wired into" nine SaaS products is
selling you something.

**The eleventh seat is not in here.** Ten seats ship. A real pod has eleven, and
the eleventh is the director: the person who looks at nine ranked arguments and
says "these four, and here is why." It is not withheld as an upsell and it is
not hard to write. It is left out because it was never the bottleneck. Nobody's
creative operation was ever slow because the director was slow. It was slow
because a brief sat in a queue, a designer was booked, nobody had read the
reviews, and the export check slipped. Those are the fifty skills below, and
they are now genuinely fast.

---

## Setup

Requires [Claude Code](https://claude.com/claude-code).

```bash
git clone https://github.com/styfinity/augusta-creative-pod.git
cd augusta-creative-pod
cp .env.example .env          # only needed if you wire MCP servers
mkdir -p config output
claude
```

Then, in Claude Code:

```
/agents        # confirm the ten seats loaded
```

That is the whole install. The agents and skills are plain markdown in
`.claude/`, so there is nothing to build and no dependencies.

---

## The fifty skills

Grouped by the five stages a creative operation actually moves through, plus the
skills that keep the cycle running. Your constraint is at the earliest stage
that fails, not the one that hurts most.

### Stage 1: Read the buyer (8)

The words, moments and fears you are going to argue with. Everything downstream
is only as good as this.

| Skill | What it hands you |
|---|---|
| `review-pull` | Raw reviews to a clean evidence table, verbatim preserved |
| `voice-of-customer` | The 20 phrases customers actually use, ranked |
| `persona-brief` | The buyer, written so a creator can play them |
| `purchase-trigger` | The moment that made them buy, filmable |
| `switching-story` | What they used before and why they left it |
| `objection-read` | Every reason to disagree, in their words |
| `anxiety-ledger` | Every reason a sold buyer still does not click |
| `desire-ladder` | Stated, functional and unspoken want, all evidenced |

### Stage 2: Read the category (9)

What is already funded, what is saturated, and what nobody is saying.

| Skill | What it hands you |
|---|---|
| `competitor-ad-pull` | Live competitor ads, structured, with days live |
| `category-claim-map` | Every ad collapsed to the claims actually running |
| `claim-saturation` | A saturation score per claim, enter or avoid |
| `white-space-finder` | Arguments with demand and no supply |
| `proof-inventory` | Every proof you can legitimately show, graded |
| `price-position-read` | Where you sit, and whether creative must justify it |
| `format-census` | Category format split against yours |
| `coverage-audit` | What your live set covers and what it misses |
| `entry-points` | The situations that make someone a buyer at all |

### Stage 3: Decide the argument (8)

The stage that decides whether the money works. Almost every account we are
shown is short of arguments rather than short of assets.

| Skill | What it hands you |
|---|---|
| `argument-census` | One number: how many distinct arguments are live |
| `objection-to-argument` | Every objection inverted into a testable claim |
| `proof-match` | Each argument bound to cleared evidence, or refused |
| `argument-scorer` | Demand, proof and saturation on one comparable scale |
| `angle-stress-test` | Six attacks on an argument before spend finds them |
| `argument-brief` | Nine fields a designer, editor and creator all read |
| `test-design` | Concepts per argument, held constant, and the read rule |
| `kill-list` | What to stop running, with the budget released |

### Stage 4: Make the set (11)

Specs precise enough that nothing silently breaks between the brief and the
account.

| Skill | What it hands you |
|---|---|
| `character-budgets` | The real character capacity of every template field |
| `layout-grid` | Five layout archetypes built at every ratio |
| `ratio-matrix` | Which ratios every concept needs for full coverage |
| `headline-bank` | 40 headlines, one argument, four structures, all in budget |
| `static-spec` | Field by field spec a designer or image model builds from |
| `hook-bank` | 20 first three seconds, line and shot paired |
| `shot-sheet` | A numbered shot list with a must-have per shot |
| `ugc-script` | A creator script that sounds like a person and still argues |
| `talent-brief` | Eight sections so footage comes back usable first time |
| `offer-bar` | One approved closing bar for the whole set |
| `export-check` | Every file against its spec before it reaches the account |

### Stage 5: Read the result (8)

Reading by argument rather than by asset, which is the only view that tells you
what to make next.

| Skill | What it hands you |
|---|---|
| `hook-rate-read` | Separates a bad argument from a bad opening |
| `hold-rate-read` | The exact beat that lost them, joined to the shot sheet |
| `winner-teardown` | Which component carried the win, and where it transfers |
| `loser-teardown` | Cause of death in order, so good arguments survive defects |
| `fatigue-watch` | Decay caught before the account feels it |
| `ncr-per-argument` | New customer revenue by argument, and the wasted spend |
| `monday-report` | The weekly read, same shape every week |
| `iteration-brief` | Last cycle's read becomes next cycle's plan in one pass |

### Running the pod (6)

The unglamorous skills that decide whether any of the above compounds.

| Skill | What it hands you |
|---|---|
| `ingredient-file` | Eleven fields, filled once per product |
| `cycle-kickoff` | Readiness check before anyone starts |
| `capacity-plan` | Capacity converted into answers rather than assets |
| `brief-qa` | Six checks that stop an unreadable set going into production |
| `handoff-check` | Whether stage N is genuinely consumable by stage N+1 |
| `asset-registry` | The table that makes every later read possible |

Build `ingredient-file`, `character-budgets` and `layout-grid` before your first
cycle. They are one-time and everything downstream assumes they exist.

---

## The ten seats

The skills are the jobs. The seats are the roles that run them in order.

| Seat | Agent | Job |
|---|---|---|
| 1 | `review-miner` | Reads your customers, returns their words |
| 2 | `category-mapper` | Reads the category, returns argument density |
| 3 | `angle-architect` | Ranks what is worth arguing, assigns ARG_IDs |
| 4 | `brief-writer` | One page per argument, against the real number |
| 5 | `static-speccer` | Argument to autofill-ready spec table |
| 6 | `shot-lister` | Argument to a runnable shot sheet |
| 7 | `hook-writer` | Structures for the first three seconds |
| 8 | `talent-briefer` | Creator briefs that argue rather than hold |
| 9 | `export-checker` | Every check against every finished file |
| 10 | `set-reader` | Reads what ran, by argument, and hands back to Seat 3 |

Seat 10 hands back to Seat 3. That backward edge is the only structural
difference between a pod and a production line. A production line ships assets.
A pod learns what to ship next.

---

## The ARG_ID contract

Seat 3 assigns an ID to every argument. Every seat after it carries that ID
through, and shipped files are named:

```
[ARG_ID]-[CONCEPT_ID]-[ratio]        e.g.  A3-C2-1x1
```

This is the only reason Seat 10 can answer **"which argument won"** rather than
**"which file won"**, and the second question is not worth asking. Break the
naming convention and the read at the end of the cycle silently stops working
while still producing a confident-looking table.

---

## A first cycle, end to end

```
 1. /cycle-kickoff            confirm nothing is stale or missing
 2. /ingredient-file          fill the eleven fields for one product
 3. /review-pull              on your last 500 reviews, raw
 4. /voice-of-customer        and /purchase-trigger on the output
 5. /competitor-ad-pull       on 25 competitor listings with run durations
 6. /category-claim-map       then /white-space-finder against step 4
 7. /argument-scorer          on the candidates, fund the top four
 8. /angle-stress-test        on each. Drop what fails on the mirror test.
 9. /capacity-plan            then /test-design. Cut arguments, never concepts.
10. /argument-brief           on each survivor, then /brief-qa on the set
11. /static-spec /shot-sheet /hook-bank /ugc-script as the formats require
12. /export-check             on every file. Every one.
13. ship to your buyer
14. /monday-report            weekly, then /ncr-per-argument at cycle end
15. /iteration-brief          which becomes the input to step 7
```

First full pass is an afternoon, most of it gathering. After that a cycle is a
morning, and the weekly rhythm is the Monday read.

---

## MCP (optional)

Stages 2 and 5 are more useful with live data. `.mcp.json.example` has the
shape, and you supply the servers.

**We do not vendor MCP servers and we do not endorse specific packages.** Pick
your own, read its source, and scope it yourself. That last part matters:

> **Everything that touches an ad account here is read-only by design.** If you
> connect an ads MCP server, grant read scope only. There is no part of this pod
> that needs permission to change a budget, a bid or a status. Augusta does not
> run media buying and this repo is scoped so it cannot. Your media buyer owns
> the spend.

Never put a token in `.mcp.json`. Use the environment, and keep `.env`
gitignored.

---

## Where this stops

Fifty skills give you the sequence and the craft inside each step. Pointing them
is the part that does not come in a prompt: which argument, which buyer state,
which format carries which claim, which result to chase and which to cut. That
is the eleventh seat.

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
