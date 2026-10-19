# Market Data Comparison

Market-data comparison is most useful when the conditions behind each observation are clear.

Two charts can show the same instrument and still differ because of ordinary differences in timing, session coverage, aggregation, historical adjustments or source methodology.

The purpose of this document is to provide a practical framework for comparing market-data views before interpreting the result.

## Start With the Research Question

Before comparing two charts or data sources, define what you are trying to understand.

Examples include:

- Why do two sources show different closing prices?
- Why does reported volume differ?
- Why do historical charts have different shapes?
- Does one source include a different market session?
- Are the sources using different adjustment methods?

A clear research question helps determine which inputs need to be aligned.

## Confirm the Instrument

A comparison should begin by confirming that both views represent the same instrument.

Useful details may include:

- ticker or symbol
- market or exchange
- quoted currency
- instrument type
- listing or share class where relevant

Similar names do not always mean identical instruments.

A comparison becomes weaker if the identity of the underlying instrument is unclear.

## Align the Time Context

A visible timestamp may represent different events.

It can refer to:

- the time of a trade
- the opening or closing time of a candle
- a data update
- an interface refresh
- a publication or filing event

For reproducible research, record both the timestamp and its time zone.

For example:

`19 October 2026, 14:30 UTC — chart observation time`

is more useful than:

`14:30`

The additional context makes the observation easier to reconstruct later.

## Match the Chart Interval

The same underlying market activity can look very different depending on how it is aggregated.

A five-minute chart and a daily chart may both be valid, but they answer different research questions.

Before comparing chart structure, confirm that both views use comparable:

- intervals
- date ranges
- aggregation settings

A difference in interval can change visible volatility, candle structure, highs, lows and volume distribution.

## Check the Market Session

Session settings can also change the appearance of a chart.

One source may display only the regular market session.

Another may include pre-market or after-hours activity.

If the session definitions differ, the charts may show different:

- opening values
- closing context
- highs and lows
- volume
- gaps
- candle structure

Before treating the difference as a data-quality problem, confirm whether the session settings are comparable.

## Review Historical Adjustments

Historical series may be transformed after corporate or structural events.

Examples include:

- stock splits
- reverse splits
- dividends
- contract rolls
- symbol changes
- data corrections

One source may display adjusted history while another may use a different treatment.

Both series can be internally consistent while still producing visibly different charts.

The adjustment method should therefore be recorded explicitly when it matters to the comparison.

## Preserve Source Context

The visible chart is the final presentation layer.

A useful comparison also records information about the source behind it.

Relevant context may include:

- data provider
- observation time
- methodology notes
- update frequency
- session rules
- adjustment policy
- revision history where available

The objective is not to assume that every difference has a simple explanation.

The objective is to make the comparison traceable.

## Separate Observation From Explanation

A research note should distinguish between what is directly visible and what may explain it.

Example:

**Observation:**  
Source A displays higher volume than Source B for the selected period.

**Possible explanation:**  
The sources may use different session definitions or aggregation methods.

The observation can be documented immediately.

The explanation still requires verification.

This distinction reduces the risk of turning an early assumption into a conclusion.

## Comparison Example

A compact comparison record may look like this:

```text
Research question:
Why do two sources show different historical closing prices?

Instrument:
Example equity

Market / exchange:
Same listing confirmed

Currency:
Same quote currency

Source A:
Provider A

Source B:
Provider B

Observation time:
19 October 2026, 14:30 UTC

Chart interval:
Daily

Session:
Regular session

Adjustment setting:
Source A: split-adjusted
Source B: not yet confirmed

Observation:
Historical closing values diverge before the corporate-action date.

Possible explanation:
Different adjustment methodologies.

Verification needed:
Confirm Source B historical adjustment policy.
