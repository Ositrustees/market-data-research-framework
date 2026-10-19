# Chart Settings

Chart settings can materially change how market data appears on screen.

Two charts may show the same instrument and still look different because of differences in interval, session coverage, time zone, historical adjustments or display methodology.

The purpose of this document is to show which chart settings should be recorded before interpreting a visible difference.

## Why Chart Settings Matter

A chart is not a neutral picture of the market.

It is a visual output produced from a set of inputs and display rules.

Those rules may include:

- chart interval
- date range
- time zone
- market session
- historical adjustment method
- aggregation logic
- source methodology

If those settings differ, the chart can differ too.

This does not automatically mean one view is wrong.

It means the conditions behind the comparison need to be checked.

## Chart Interval

The chart interval determines how individual market observations are grouped.

Common examples include:

- 1 minute
- 5 minutes
- 15 minutes
- 1 hour
- daily
- weekly

A short interval can show detail that disappears inside a longer interval.

A price move that looks large on a 5-minute chart may appear as a small part of a daily candle.

For reproducible research, record the interval explicitly.

Example:

```text
Chart interval:
5 minutes
```

or:

```text
Chart interval:
Daily
```

## Date Range

The visible date range also affects interpretation.

A short window can make a move appear unusually large.

A longer window may place the same move inside a broader trend.

When comparing two charts, use comparable date ranges whenever possible.

Example:

```text
Date range:
1 September 2026 to 19 October 2026
```

## Time Zone

Time zones can affect candle boundaries, timestamps and the interpretation of market events.

A chart displayed in local time may not align with another chart displayed in UTC or exchange time.

For research notes, record the time zone clearly.

Example:

```text
Time zone:
UTC
```

or:

```text
Time zone:
Eastern Time
```

If the platform does not state the time zone clearly, record that uncertainty.

Example:

```text
Time zone:
Not confirmed
```

## Market Session

Session settings can change the shape of a chart.

Depending on the source, a chart may include:

- regular trading hours only
- pre-market activity
- after-hours activity
- extended-hours activity
- a broader electronic session

If one source includes extended activity and another does not, visible differences may appear in:

- opening prices
- closing context
- highs and lows
- volume
- gaps
- candle structure

Record the session setting whenever it matters to the comparison.

Example:

```text
Session:
Regular market hours
```

or:

```text
Session:
Regular + extended hours
```

## Historical Adjustments

Historical prices may be adjusted after corporate or structural events.

Examples include:

- stock splits
- reverse splits
- dividends
- symbol changes
- contract rolls
- historical corrections

One source may use adjusted history while another may use raw or differently processed values.

This can change the appearance of the entire historical chart.

Record the adjustment setting explicitly when it is known.

Example:

```text
Adjustment setting:
Split-adjusted history
```

If the methodology is unclear:

```text
Adjustment setting:
Not confirmed
```

Do not infer the adjustment method only from the appearance of the chart.

## Aggregation and Candle Construction

Two sources can use similar underlying data while constructing candles differently.

Differences may appear in:

- opening value
- closing value
- high
- low
- volume
- interval boundaries

If a source documents its aggregation methodology, keep that information connected to the chart observation.

If the methodology is not documented, note the uncertainty.

Example:

```text
Aggregation methodology:
Not documented
```

## Volume Settings

Volume can be especially sensitive to source and session settings.

Before comparing volume across charts, check:

- whether the same session is included
- whether the same interval is used
- whether the source uses the same aggregation method
- whether the instrument is identical
- whether delayed or revised data may be involved

A visible volume difference is an observation first.

The explanation should be investigated separately.

## Visual Scale and Display Settings

Some chart differences come from presentation rather than underlying data.

Examples include:

- linear versus logarithmic scale
- auto-scaling
- percentage view
- normalized view
- overlay indicators
- adjusted versus raw series

These settings can change how the same data looks without changing the underlying values.

If the research question depends on the visual structure of the chart, record the relevant display settings.

Example:

```text
Price scale:
Logarithmic
```

## Indicators and Derived Overlays

Indicators can add another analytical layer to a chart.

Examples include:

- moving averages
- volatility bands
- volume averages
- relative-strength measures
- custom calculated indicators

These overlays should not be confused with raw market data.

If an indicator is used, record:

- indicator name
- calculation period
- source or methodology
- relevant settings

Example:

```text
Indicator:
20-period moving average

Calculation:
Based on closing prices
```

## Observation Before Interpretation

A chart setting can explain a visible difference, but that explanation should be verified.

Example:

**Observation:**  
Chart A shows a higher opening price than Chart B.

**Possible explanation:**  
Chart A may include extended-hours trading.

The observation is visible.

The explanation still needs confirmation from the session settings.

This distinction helps prevent a plausible explanation from becoming a conclusion too early.

## Chart Settings Record

A compact chart-settings record may look like this:

```text
Instrument:
Example equity

Source:
Provider A

Observation time:
19 October 2026, 14:30 UTC

Chart interval:
Daily

Date range:
1 September 2026 to 19 October 2026

Time zone:
UTC

Session:
Regular market hours

Adjustment setting:
Split-adjusted history

Price scale:
Linear

Indicators:
None

Methodology notes:
Available

Uncertainty:
Volume aggregation method not documented
```

## Suggested Review Sequence

Before comparing two charts, use this sequence:

**Instrument → Time Zone → Interval → Date Range → Session → Adjustments → Display Settings → Source Context**

The sequence does not need to be rigid.

The purpose is to identify the settings that could materially affect the visible result.

## When Charts Still Differ

Even after chart settings are aligned, two sources may still disagree.

At that point, the difference may come from deeper source methodology, update timing, historical revisions or data-processing rules.

The correct next step is not to assume one chart is wrong.

The correct next step is to document what remains different and investigate the source context.

## Final Principle

A chart should be interpreted together with the conditions that produced it.

Interval, session, time zone, historical adjustments and display settings can all change what appears on screen.

Preserving those settings makes the research easier to review, reproduce and challenge.

**Research. Compare. Verify.**

---

This document is part of the Ositrustees Market Data Research Framework and is provided for educational and analytical purposes only.
