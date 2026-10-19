# Research Note Template

A reproducible research note should preserve enough context for another researcher to understand what was observed, which conditions shaped the result, and what still requires verification.

The purpose of this template is not to document every action.

The purpose is to preserve the details that could materially change the interpretation.

## Core Research Note

Use this compact structure for most market-data observations:

```text
Research question:

Instrument:

Market / exchange:

Currency:

Source:

Observation time:

Time zone:

Chart interval:

Date range:

Session:

Adjustment setting:

Relevant source methodology:

Observation:

Possible explanation:

What still needs verification:
```

## Research Question

Start with the question the research is trying to answer.

A clear question helps determine which inputs matter.

Examples:

```text
Why do two sources show different historical closing prices?
```

```text
Why does reported volume differ between two chart views?
```

```text
Does one source include a different market session?
```

```text
Is the historical series adjusted differently across providers?
```

Avoid starting with a conclusion.

The research question should define what needs to be checked.

## Instrument Context

Record enough information to identify the instrument clearly.

Useful fields may include:

```text
Instrument:
Ticker or symbol

Market / exchange:
Relevant venue

Currency:
Quote currency

Instrument type:
Equity, index, fund, contract, or other relevant category
```

Similar names do not always represent identical instruments.

Instrument identity should be confirmed before comparing market-data outputs.

## Source Record

The source should remain connected to the observation.

A useful source record can include:

```text
Source:
Provider or document name

Source type:
Market-data interface, filing, financial statement, company announcement, analytical field, or other source

Source URL:
Optional when relevant

Methodology notes:
Available / unavailable / partially documented

Revision status:
Confirmed / not confirmed / not applicable
```

A URL alone may not explain how the value was produced.

When methodology matters, preserve that context.

## Time Context

Record both the timestamp and what the timestamp represents.

Example:

```text
Observation time:
19 October 2026, 14:30 UTC

Timestamp meaning:
Chart observation time
```

Other possible timestamp meanings include:

- trade time
- candle open time
- candle close time
- source update time
- filing publication time
- filing acceptance time
- interface refresh time

If the time convention is unclear, record the uncertainty.

Example:

```text
Timestamp meaning:
Not confirmed
```

## Chart Context

When a chart is part of the research, record the settings that could affect the view.

Example:

```text
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
```

Not every field is required for every research question.

Record the settings that could materially affect the interpretation.

## Observation

The observation should describe what is directly visible or documented.

Example:

```text
Observation:
Source A displays higher reported volume than Source B for the selected period.
```

Another example:

```text
Observation:
Historical closing prices diverge before the corporate-action date.
```

The observation should not include an explanation unless that explanation has already been verified.

## Possible Explanation

Record hypotheses separately.

Example:

```text
Possible explanation:
The sources may use different session definitions.
```

or:

```text
Possible explanation:
The historical series may use different adjustment methodologies.
```

A possible explanation is not a confirmed conclusion.

Keeping this distinction visible makes the research easier to review.

## Verification Needed

Document unresolved questions explicitly.

Examples:

```text
What still needs verification:
Confirm Source B historical adjustment policy.
```

```text
What still needs verification:
Check whether extended-hours activity is included.
```

```text
What still needs verification:
Confirm the timestamp convention used by the source.
```

```text
What still needs verification:
Review whether the underlying document has been amended.
```

Uncertainty should remain visible until it is resolved.

## Corporate Information Add-On

When corporate information is relevant, add fields such as:

```text
Corporate source:

Document title:

Document type:

Publication date:

Publication time:

Revision or amendment status:

Observed relationship to market data:

Causation confirmed:
Yes / No / Not established
```

The final field is important.

A corporate event and a market move can occur near each other without proving that one caused the other.

## Comparison Add-On

For two-source comparisons, add:

```text
Source A:

Source B:

Instrument match:
Confirmed / not confirmed

Time alignment:
Confirmed / not confirmed

Interval alignment:
Confirmed / not confirmed

Session alignment:
Confirmed / not confirmed

Adjustment alignment:
Confirmed / not confirmed

Visible difference:

Likely explanation:

Verification status:
```

This makes it easier to separate aligned inputs from unresolved differences.

## Example Completed Research Note

```text
Research question:
Why do two sources show different historical closing prices?

Instrument:
Example equity

Market / exchange:
Same listing confirmed

Currency:
USD

Source:
Provider A and Provider B

Observation time:
19 October 2026, 14:30 UTC

Time zone:
UTC

Chart interval:
Daily

Date range:
1 January 2026 to 19 October 2026

Session:
Regular market hours

Adjustment setting:
Source A: split-adjusted
Source B: not confirmed

Relevant source methodology:
Source A documents historical adjustments.
Source B methodology not confirmed.

Observation:
Historical closing values diverge before the corporate-action date.

Possible explanation:
Different historical adjustment methodologies.

What still needs verification:
Confirm Source B adjustment policy and revision history.
```

## Short-Form Research Note

For simple observations, a shorter format may be enough:

```text
Question:

Source:

Time:

Settings:

Observation:

Possible explanation:

Verification needed:
```

Use the short form only when the research question does not require more detailed context.

## Research Note Review Checklist

Before considering a note complete, check whether another researcher could answer:

- What was being investigated?
- Which instrument or dataset was used?
- Where did the information come from?
- When was the observation made?
- Which settings affected the view?
- What was directly observed?
- What was interpreted?
- What remains uncertain?
- What evidence would resolve the uncertainty?

If those questions can be answered from the note, the research trail is usually strong enough to revisit later.

## Final Principle

A useful research note preserves the path between the source and the conclusion.

It should show what was observed, which conditions mattered, what explanation was considered, and what still requires verification.

The goal is not more documentation.

The goal is a research record that can be reviewed, reproduced and challenged.

**Research. Compare. Verify.**

---

This document is part of the Ositrustees Market Data Research Framework and is provided for educational and analytical purposes only.
