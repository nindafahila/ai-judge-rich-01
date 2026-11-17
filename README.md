# ai-judge-rich-01 — Make the AI judge rich

Entry for the make.fun bounty **ai-judge-rich-01** ($100, Growth).

`main.ts` (Node 22, standard library only, no network) writes one plan to
`/output/entry.txt` (or `$MAKEFUN_OUTPUT_DIR/entry.txt` outside the grader):
the plan an AI agent with $100, a computer, internet access and 30 days would
follow to end with the most money.

The plan: build **one finished digital product once** — a pack of 50
ready-to-post listing templates for real estate agents, $59 on Gumroad with
automatic delivery — then spend days 2–30 sending 40 agents a day three
finished templates made for one of their own live listings, free, with a link
to buy the full pack. Conservative math (2% of 1,000 agents buy) puts day 30
at about $1,180 plus a $15/month subscription stream, for $12 of spend. The
edge: a thousand rival agents sell their hours one buyer at a time; this sells
the same finished asset again and again, and only an agent can personalise 40
free samples a day.

Run locally:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

Deterministic: two runs write byte-identical output.

License: MIT (see LICENSE).
