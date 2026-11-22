---
name: weekly-metrics-summary
description: Summarize weekly metrics, outliers, likely drivers, and recommended follow-up in one operating brief. Use when you have this week's dashboard numbers and a team sync coming up, and want a short brief of what moved, likely drivers, and what to discuss.
license: CC-BY-4.0
compatibility: generic-agent, claude-style-workflow, mcp-friendly
metadata:
  author: OutcomeKit
  version: "1.1.0"
  category: ops
  pack-tier: basic
---

# Weekly Metrics Summary

## Purpose
This skill turns a spreadsheet or copied dashboard numbers into a short weekly operating brief. It highlights what changed, where the anomalies are, and what deserves follow-up before your team meeting.

## Best Use Cases
- Turning a Monday morning dashboard export into a team-readable narrative
- Flagging a 15% drop in activation rate before the weekly sync
- Comparing this week's pipeline numbers against last week, or against a trailing 4-week average if your export includes one

## Required Inputs
- **Metric export**: Copied dashboard values, spreadsheet rows, or BI export
- **Primary KPIs**: The few metrics your team actually steers by

## Optional Inputs
- **Previous week's summary**: For trend comparison and narrative continuity
- **Alert thresholds**: Custom thresholds for flagging anomalies


## Workflow
1. Ingest the metric export and identify the primary KPIs
2. Calculate week-over-week deltas for each tracked metric
3. Flag outliers: any metric past the operator's alert threshold, or past 15% week-over-week if none was given
4. Hypothesize likely drivers for significant changes
5. Generate 2-3 questions the team should discuss
6. Summarize the overall health signal in 1-2 sentences
7. Format as a scannable brief for the weekly team sync

## Decision Rules
- If any metric moved more than 15% week-over-week, flag it as an outlier; if the operator gave alert thresholds, use those instead. For metrics that are themselves percentages, show the change in points and the relative change, and apply the 15% test to the relative change
- If multiple metrics moved in the same direction, look for a common driver
- If the data seems incomplete or has gaps, note it rather than interpolating
- If all metrics are flat (none moved more than 5% either way), frame the summary around stability and what to watch
- If a leading indicator conflicts with a lagging indicator, highlight the tension
- If a metric has no prior-week value, show this week's value, mark it 'no baseline', and skip the delta
- If two sources report the same metric differently, show both figures and ask which is correct; do not pick one
- If a spike is tied to a one-time event the operator named, show the number as reported and note the event; if no event was named, ask whether one happened
- If the export includes a trailing 4-week average, show the change against it next to the week-over-week change
- If the export looks like it mixes test or staging data with production, flag it and hold back conclusions until the data is confirmed

## Edge Cases
- Only half the expected metrics are available this week
- A metric spiked due to a one-time event (data migration, holiday, outage)
- The same metric is reported differently by two data sources
- All metrics are flat for the third consecutive week
- A new metric was added this week with no historical baseline
- The dashboard export includes test or staging data mixed with production

## Output Requirements
The output must:
- Show week-over-week deltas for all primary KPIs
- Highlight outliers exceeding normal variance
- Hypothesize drivers for significant changes
- Include 2-3 discussion questions for the team
- Be readable in under 2 minutes

## Failure Handling
If required information is missing:
- If only partial metrics are available, summarize what's present and list what's missing
- If KPIs are not specified, use the top 5 metrics by variance as the default focus

If confidence is low:
- Flag hypothesized drivers as speculative rather than definitive
- Recommend checking the data source before acting on the summary

## Constraints
- Do not interpolate missing data points
- Do not present hypothesized drivers as confirmed causes
- Do not recommend strategic pivots based on a single week of data
- Do not ignore metrics that declined in favor of only highlighting wins
- Do not alter the reported numbers for any reason

## Examples Reference
See `/examples` for a worked standard case.
