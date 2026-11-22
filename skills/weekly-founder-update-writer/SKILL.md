---
name: weekly-founder-update-writer
description: Turn raw notes into a founder update for investors, advisors, or your team with a consistent structure. Use when you have a week of scattered notes and need a short investor, advisor, team, or client update with wins, blockers, asks, and next priorities.
license: CC-BY-4.0
compatibility: generic-agent, claude-style-workflow, chatgpt-project
metadata:
  author: OutcomeKit
  version: "1.1.0"
  category: content
  pack-tier: basic
---

# Weekly Founder Update Writer

## Purpose
This skill turns fragmented weekly notes into a consistent update your stakeholders will actually read. It organizes what changed, what matters, where help is needed, and what to watch next.

## Best Use Cases
- Writing a Friday investor update from scattered Slack messages and dashboard screenshots
- Formatting a weekly team digest when the founder is traveling
- Turning raw notes into a short operating summary for your board or advisors

## Required Inputs
- **Weekly notes**: Metrics, wins, blockers, and raw team notes
- **Audience**: Investors, advisors, internal team, or clients

## Optional Inputs
- **Previous update**: Last week's update for continuity and week-over-week narrative
- **Metric screenshots**: Dashboard images or exported charts


## Workflow
1. Ingest raw weekly notes, metrics, and any Slack or doc dumps
2. Extract wins, blockers, and open asks from the raw material
3. Identify the 1-2 most important narratives for the week
4. Structure the update: headline, wins, blockers, asks, next week priorities
5. Adjust tone for the target audience (investors vs. team vs. clients)
6. Generate a scannable draft under 300 words
7. If a previous update was provided, add one line on last week's top priority and what this week's notes say about it; if none was provided, skip the line

## Decision Rules
- If metrics are included, lead with the most meaningful delta
- If no blockers exist, say so explicitly rather than inventing friction
- If the audience is investors, emphasize traction and asks
- If the audience is the internal team, emphasize priorities and accountability
- If the week was uneventful, keep the update short and honest
- If the audience is advisors, emphasize the decisions and asks where you want their judgment
- If the audience is clients, leave out internal revenue, churn, and hiring detail and report progress on their work
- If metrics contradict each other (for example revenue up and churn up), report both figures side by side and do not net them into one story
- If the notes state no priorities for next week, propose one or two from the open blockers and asks, label them as proposed, and ask the founder to confirm
- If the week included a crisis, state what happened, the impact, and what is being done in plain words, without softening the facts
- If one update must serve investors and the team, write two short versions rather than one blended one, each under 300 words
- If the notes contain something that looks unsuitable for the stated audience (customer names, salaries, legal matters), leave it out and list what was omitted in a note to the founder
- If the founder is announcing a pivot, state it in the founder's own words and keep the metrics factual

## Edge Cases
- The founder provides only two bullet points for the entire week
- Metrics are contradictory (revenue up but churn also up)
- The week included a crisis that the founder wants to frame carefully
- Notes are entirely qualitative with no metrics at all
- The same update needs to serve both investors and the internal team
- The founder wants to communicate a pivot or strategic shift

## Output Requirements
The output must:
- Open with a one-line headline
- Include wins, blockers, and asks as distinct sections
- Keep total length under 300 words
- Reference specific metrics or events, not vague summaries
- Match tone to the stated audience
- End with next week's top 1-2 priorities, marked as proposed when the notes did not state them

## Failure Handling
If required information is missing:
- If only partial notes are provided, structure the update around what's available
- Explicitly mark sections where data is missing rather than fabricating wins or metrics

If confidence is low (the notes are thin or contradict each other):
- Keep the update shorter and more qualitative
- Suggest the founder add 2-3 specific data points before sending

## Constraints
- Do not fabricate metrics or wins not present in the notes
- Do not editorialize about company strategy unless the notes support it
- Do not include confidential information that should not be shared with the stated audience
- Do not exceed 300 words unless the operator explicitly requests a longer format
- Do not change the factual content of what the founder reported

## Examples Reference
See `/examples` for a worked standard case.
