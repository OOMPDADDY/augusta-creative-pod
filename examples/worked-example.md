# A worked cycle

One full pass, so the handoffs are visible. The product is invented. The shapes
are real.

## Seat 1 emits

```
CLAIM                             | HOW OFTEN | VERBATIM EVIDENCE                       | ON OUR SITE?
Lasts longer than the cheap ones  | 41        | "third winter and its still going"      | NO
Warm without the bulk             | 33        | "not puffy like the other one i had"    | YES
Packs down small                  | 18        | "shoved it in a carryon no problem lol" | NO
```

Row 1 is the finding. Forty-one customers say it and the site has never
mentioned it. The ON OUR SITE? column is where the gap usually shows up, and it
is the reason this seat runs before anything gets written.

Note the quotes are untidied. "its" and "lol" stay. That is the register the
buyer writes in.

## Seat 2 emits

```
ARGUMENT               | ADVERTISERS  | ASSET COUNT | LONGEST RUN | WE HOLD PROOF?
Packs down small       | none         | 0           | n/a         | row 3
Lasts multiple winters | Brand C      | 2           | 11 months   | row 1
Warm without bulk      | A, B, C, E   | 19          | 14 months   | row 2
```

Sorted ascending, so open ground sits at the top. Nineteen assets across four
advertisers argue "warm without bulk" and one of them has run it for fourteen
months, which tells you it works and that entering there means outspending four
brands who got there first.

## Seat 3 emits

```
ARG_ID | ARGUMENT               | WHO IT LANDS ON             | PROOF WE HOLD | DENSITY | OPEN?
A1     | Packs down small       | Booking carry-on only       | row 3         | 0       | YES
A2     | Lasts multiple winters | Replaced one last year      | row 1         | 2       | YES
A3     | Warm without bulk      | Owns a puffy one they avoid | row 2         | 19      | NO, saturated
```

WHO IT LANDS ON is a moment, not a demographic. "Booking carry-on only" is a
situation you can write a hook against. "Women 35 to 54" is not.

## Seat 5 emits, for A1

```
CONCEPT_ID | HEADLINE (max 42)                     | LAYOUT
A1-C1      | Fits in the bag you already carry     | HERO
A1-C2      | Third winter. Still one bag.          | BIG_NUMBER
A1-C3      | The coat that needs no coat bag       | SPLIT
```

Files ship as `A1-C1-1x1`, `A1-C1-9x16`, `A1-C2-1x1` and so on. Five placements
of one concept are one concept, not five tests.

## Seat 10 reads back

```
ARG_ID | ASSET COUNT | TOTAL SPEND | RESULT | TESTED?
A3     | 14          | 48,200      | ...    | YES
A1     | 3           | 6,100       | ...    | NO, spend 8x below A3
A2     | 1           | 900         | ...    | NO, one asset
```

Distinct arguments live: 3.

The finding writes itself. A3 has the most assets and the most spend, which is
why it looks like the winner. It was also the saturated argument the category
already owned. A1 was the open position, held real proof, and has never had a
budget behind it.

That goes back to Seat 3, not to Seat 5. A1 does not need more assets yet. It
needs a decision about whether it gets funded properly or dropped, and that
decision is the eleventh seat.
