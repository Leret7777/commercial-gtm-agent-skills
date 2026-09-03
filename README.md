# Commercial GTM Agent Skills

Agent skills for the commercial side of go-to-market — pipeline, trading,
variance, pricing and base management.

## What this is

A small, growing library of `SKILL.md` files that any agent capable of reading
skills can use. Each skill is a self-contained package in its own top-level
folder, holding everything it needs: the skill itself, an author profile, a
licence, and its own README. Nothing here assumes a particular vendor or tool.

| Folder | What it does |
|---|---|
| [`weekly-pipeline-trading-pack`](weekly-pipeline-trading-pack) | Turns a weekly pipeline export plus orders and target figures into an editable KPI-and-commentary trading pack: did the week trade green, what moved, and when the pipeline lands as orders. |

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

## Layout

Each skill lives in its own folder, laid out so it can be contributed onward to
[gtmskills.com](https://gtmskills.com) without restructuring:

```
<skill-name>/
├── README.md
├── CONTRIBUTING.md
├── LICENSE
└── skills/
    └── <author-slug>/
        ├── author.md
        └── <skill-name>/
            ├── SKILL.md
            └── references/     (optional, deeper material)
```

Open a skill's folder for its own README and full detail.

## Licence

MIT. These skills encode method, not any employer's commercial data — no
thresholds, margin floors or internal figures appear in them.
