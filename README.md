# Commercial GTM Agent Skills

Skills for the commercial side of go-to-market — pipeline, trading, variance, pricing and base management — written for the teams that work from BI snapshots and spreadsheets rather than a live sales stack.

Most go-to-market skills assume a stack: a CRM, an enrichment vendor, a sequencer, a webhook firing on a signal. Large commercial teams don't work that way. They get a weekly export from a data team, open it, and have to turn it into a decision before the trading call. These skills are written for that reality.

Each skill accepts its inputs however the user has them — typed figures, pasted text, an uploaded file, or a live connection to the source. None of them assume a named tool.

## Who these are for

Commercial trading, planning and performance, CVM, pricing operations, sales operations and commercial finance. The analyst seat: the person who receives the data rather than the person who creates it.

## Skills

| Skill | What it does |
|---|---|
| [weekly-pipeline-trading-pack](skills/leret-mutkut/weekly-pipeline-trading-pack) | Turns a weekly pipeline export plus orders and target figures into an editable KPI-and-commentary pack: did the week trade green, what moved, and when the pipeline lands as orders. |

Planned:

- **Variance explanation** — splits a gap against plan into price, volume, mix, churn and timing.
- **Discount check** — benchmarks a discount request against comparable closed deals.

## Installing

These are plain `SKILL.md` files. Any agent that reads skills can use them.

```bash
# everything in this library
npx skills add Leret7777/commercial-gtm-agent-skills

# a single skill
npx skills add Leret7777/commercial-gtm-agent-skills --skill weekly-pipeline-trading-pack
```

Add `-a claude-code`, `-a cursor` or another agent flag to target a specific tool.

If you can't run a terminal, open the skill folder above and copy `SKILL.md` into your agent's skills directory by hand. That works just as well.

## Layout

```
skills/
└── <author-slug>/
    ├── author.md
    └── <skill-name>/
        ├── SKILL.md
        └── references/        (optional, deeper material)
```

This mirrors the layout used by [gtmskills.com](https://gtmskills.com), so a skill written here can be contributed there without restructuring.

## Licence

MIT. Use, copy, modify and redistribute freely.

These skills encode method, not any employer's commercial data. No thresholds, margin floors or internal figures appear in them.
