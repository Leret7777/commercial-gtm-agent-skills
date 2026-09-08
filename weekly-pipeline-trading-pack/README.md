# Weekly pipeline trading pack

An agent skill for the weekly trading cycle: a fresh pipeline snapshot has landed, and someone has to turn it into a verdict before the trading call.

## What it does

Takes a weekly pipeline export plus orders and target figures and turns them into an editable KPI-and-commentary pack: whether the week traded green, what moved in the funnel week on week, and when the current pipeline is expected to land as orders. It reads pipeline cover against target, the top five won and lost, ARPU and win rate across a chosen cut, and the billing expectation profile, with commentary against each number.

Orders against target decide green; pipeline growth never does. Cover inflated by deals with distant or missing billing dates is not cover, and treating pipeline growth as good news is the most common error the pack is built to avoid.

## What it deliberately does not do

It does not declare a green week on pipeline movement alone. Orders booked against the orders target are the only thing that decides green, and a growing funnel behind a missed orders number is still a missed week.

Where an input is missing — most often the previous week's snapshot — it runs a point-in-time read and states plainly that week-on-week movement could not be assessed, rather than filling the gap. It never guesses a target or an orders figure.

## Inputs

Open opportunities, one line each with value, stage, expected billing date, product, sector, segment and owner, and the orders booked and orders target for the period are required. The orders figures usually come from finance rather than the CRM. The previous week's snapshot is strongly wanted, because movement is the point of the pack; without it the pack is a point-in-time read only.

Inputs are accepted however the user has them — typed figures, pasted text, an uploaded file, or a live connection. No tool is named anywhere, because the reader's stack is unknown.

## Output

An editable KPI-and-commentary pack, HTML by default since it edits and converts cleanly to PDF or image. The first line gives the green or not-green verdict; KPIs and written commentary follow across the chosen cut.

## Who it's for

Commercial trading, planning, performance and CVM teams working from a pipeline snapshot. The analyst seat: the person who receives the data rather than the person who creates it.

## Using it

Copy `skills/leret-mutkut/weekly-pipeline-trading-pack/SKILL.md` into your agent's skills directory. It is a plain markdown file — any agent that reads skills can use it.

## Licence

MIT. Encodes method, not any employer's commercial data. No thresholds, margin floors or internal figures appear in it.
