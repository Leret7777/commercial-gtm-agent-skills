# Revenue and margin variance review

An agent skill for the monthly and quarterly variance review: billed revenue has come in away from forecast, and someone has to account for it before the performance call.

## What it does

Takes billed revenue actuals and forecast, locates the gap, and attributes it to causes that can be checked in the data rather than derived from it — slippage, late billing, work in progress, thin opportunity cover, and known seasonal buying patterns. Reports margin alongside revenue, then states what is left to cover for the rest of the period and whether pipeline supports closing it.

Revenue leads and margin qualifies it. Landing revenue on forecast while margin falls is a worse month than the revenue line suggests, and it is the movement most often missed.

## What it deliberately does not do

It does not decompose a variance into price, volume and mix effects. Those are resolved upstream before opportunities are recorded and discounts are priced in, so there is no residual left to split. A skill that went looking for a price effect would invent one.

Where the data does not support attributing a gap, it says so and asks for what is missing. An unattributed variance is a legitimate finding and usually means an input is incomplete.

## Inputs

Billed revenue actuals and current year forecast are required. Prior year forecast, margin after all costs, the sold-versus-in-service position, and open pipeline cover all improve it.

Forecast files often span three years, so the skill selects the relevant period rather than assuming a single year.

Inputs are accepted however the user has them — typed figures, pasted text, an uploaded file, or a live connection. No tool is named anywhere, because the reader's stack is unknown.

## Output

A chart mapping revenue, margin, forecast and variance together, with KPIs and commentary. Commentary comes from the user; if none is supplied the skill drafts one and labels it as drafted.

## Who it's for

Commercial planning and performance, trading, CVM and commercial finance. The analyst seat: the person who receives the data rather than the person who creates it.

## Using it

Copy `skills/leret-mutkut/revenue-variance-review/SKILL.md` into your agent's skills directory. It is a plain markdown file — any agent that reads skills can use it.

## Licence

MIT. Encodes method, not any employer's commercial data. No thresholds, margin floors or internal figures appear in it.
