# Source Context

A market-data value becomes more useful when the source remains connected to the observation.

A chart, filing, financial statement, company announcement or calculated field may all provide useful information, but each source type carries different context.

The purpose of source documentation is not simply to save a link.

It is to preserve enough information to understand how the observation was produced and what may affect its interpretation.

## Why Source Context Matters

Two sources can display similar information and still differ in important ways.

The difference may come from:

- timing
- methodology
- session coverage
- historical adjustments
- data normalization
- document revisions
- calculated versus directly observed values

Without source context, those differences can look more mysterious than they really are.

A research note becomes stronger when the source, timestamp and methodology remain visible alongside the observation.

## A Source Is More Than a URL

A URL identifies where the information was found.

It does not always explain how the information was created.

Useful source context may include:

- source name
- source type
- observation time
- publication time
- revision status
- methodology notes
- session rules
- adjustment policy
- update frequency
- calculation method where relevant

The exact fields depend on the research question.

The goal is to preserve the details that could materially change the interpretation.

## Market-Data Sources

For market-data research, source context can include details such as:

- the data provider
- the instrument identifier
- the market or exchange
- the quoted currency
- the timestamp convention
- the chart interval
- the market session
- the historical adjustment method

For example, two charts may show the same instrument but use different session rules.

One source may include extended-hours activity.

Another may display only the regular session.

The visible difference can be real even when both sources are internally consistent.

## Corporate Information Sources

Corporate information can include:

- regulatory filings
- company announcements
- financial statements
- investor-relations documents
- corporate-action notices
- revised or amended documents

A corporate source should be recorded with enough context to identify the specific document and version being used.

Relevant details may include:

- document title
- publication or filing date
- acceptance time where available
- revision or amendment status
- issuing organization
- source URL

This helps prevent an updated or amended document from being confused with an earlier version.

## Direct Observation vs Calculated Information

Not every value displayed by a platform is directly observed.

Some values may be calculated, normalized or derived from other data.

Examples can include:

- percentage changes
- moving averages
- sector aggregates
- volatility measures
- normalized scores
- composite indicators

When a value is calculated, methodology becomes part of the source context.

A useful research note should distinguish between:

**Direct observation** — a value reported directly by the source.

**Calculated value** — a value produced using a documented or inferred formula or methodology.

This distinction matters when two platforms produce different outputs from similar underlying data.

## Timestamp Context

A timestamp should describe the event it refers to.

Possible examples include:

- trade time
- candle open time
- candle close time
- source update time
- screen observation time
- document publication time
- filing acceptance time

A timestamp without that context can be misleading.

For example:

`19 October 2026, 14:30 UTC — chart observation time`

is more useful than:

`14:30`

because another researcher can understand what the time actually represents.

## Revision and Update History

Sources can change after an observation is recorded.

A filing may be amended.

A historical dataset may be revised.

A methodology page may be updated.

A chart may later reflect a corporate-action adjustment.

When possible, record whether the source has a visible revision history or update date.

If the revision status cannot be confirmed, that uncertainty should remain in the research note.

Example:

**Revision status:** Not confirmed.

That is more useful than assuming the current version is identical to the version used earlier.

## Preserve Uncertainty

Source documentation should make uncertainty visible.

Examples include:

- methodology not documented
- session coverage unclear
- adjustment policy not confirmed
- update frequency not stated
- revision history unavailable
- calculated field methodology not disclosed

These statements do not weaken the research record.

They show which parts of the comparison still need verification.

## Example Source Record

A compact source record may look like this:

```text
Source:
Provider A

Source type:
Market-data interface

Instrument:
Example equity

Market / exchange:
Same listing confirmed

Observation time:
19 October 2026, 14:30 UTC

Timestamp meaning:
Chart observation time

Chart interval:
Daily

Session:
Regular session

Adjustment policy:
Split-adjusted history

Methodology notes:
Available

Revision status:
Not applicable

Uncertainty:
Volume aggregation method not documented

## Source Context in the Research Workflow

Source context should remain connected to the observation throughout the research process.

A useful sequence is:

**Find the source → Record the context → Observe the result → Check the methodology → Preserve uncertainty → Interpret carefully**

The objective is not to create unnecessary documentation.

The objective is to preserve the information that another researcher would need to review the same observation.

## Final Principle

A source is useful when it can be traced.

A value becomes more meaningful when the researcher can explain:

where it came from,

when it was observed,

what methodology shaped it,

and what still remains uncertain.

That is the role of source context in reproducible market-data research.

**Research. Compare. Verify.**

---

This document is part of the Ositrustees Market Data Research Framework and is provided for educational and analytical purposes only.
