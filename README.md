# Commercial Agent Skills

Agent skills for the commercial side of go-to-market — pipeline, trading,
variance, pricing and base management.

## What this is

A small, growing library of `SKILL.md` files that any agent capable of reading
skills can use. Each skill is a single self-contained file. Nothing here assumes
a particular vendor or tool.

| Skill | What it does |
|---|---|
| [`weekly-pipeline-trading-pack`](skills/weekly-pipeline-trading-pack/SKILL.md) | Turns a weekly pipeline export plus orders and target figures into an editable KPI-and-commentary trading pack: did the week trade green, what moved, and when the pipeline lands as orders. |
| [`revenue-variance-review`](skills/revenue-variance-review/SKILL.md) | Locates a billed revenue gap against forecast, attributes it to slippage, late billing, work in progress, thin cover or seasonality, checks margin alongside it, and states what is left to cover. |

## Why it exists

Most go-to-market skills assume a stack — a CRM, an enrichment vendor, a
sequencer, a webhook firing on a signal. Large commercial teams don't work that
way. They get a weekly export from a data team, open it, and have to turn it
into a decision before the trading call.

These skills are written for that reality. Each one accepts its inputs however
the user has them — typed figures, pasted text, an uploaded file, or a live
connection to the source — and names no tool, because the reader's stack is
unknown.

## Who it's for

Commercial trading, planning and performance, CVM, pricing operations, sales
operations and commercial finance. The analyst seat: the person who receives
the data rather than the person who creates it.

## Using a skill

Each skill is a plain markdown file. Open the one you want from the table above
and copy its `SKILL.md` into your agent's skills directory — any agent that
reads skills can use it. No installation, account or tool is required.

## Layout

```
skills/
└── <skill-name>/
    └── SKILL.md        (references/ alongside it, if a skill needs deeper material)
```

## Author

**Leret Mutkut** — commercial data and analytics in enterprise telecoms, across
planning, performance, trading, CVM and pricing operations. Previously a product
manager and product trader on a large ITS and cloud portfolio, so these skills
are written from both sides of the number: the person producing the commercial
view and the people arguing about it on the trading call. They're written for
teams that work from BI snapshots and spreadsheets rather than a live sales
stack — the analysts who receive a weekly export and have to turn it into a
decision by Thursday.

## Licence

MIT. These skills encode method, not any employer's commercial data — no
thresholds, margin floors or internal figures appear in them.
