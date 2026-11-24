---
name: meeting-follow-up-email
description: Turn call notes into a same-day follow-up email with clear next steps. Use right after a call when you want a same-day recap email with agreed items, next steps (owner and date), and open questions.
license: CC-BY-4.0
compatibility: generic-agent, claude-style-workflow, chatgpt-project
metadata:
  author: OutcomeKit
  version: "1.1.0"
  category: sales
  pack-tier: basic
---

# Meeting Follow-Up Email Writer

## Purpose
This skill turns rough call notes into a follow-up email you can send the same day. It pulls out what was agreed, who owns what, and what is still open, then writes a short recap that gives the other side an easy way to confirm.

## Best Use Cases
- Sending the recap an hour after a discovery call while the details are still exact
- Turning a rambling transcript into agreed items with owners
- Confirming next steps after an internal kickoff so nobody re-litigates them next week

## Required Inputs
- **Call notes**: Rough notes, bullets, or a transcript from the meeting
- **Recipient and goal**: Who receives the recap and what you want them to do next

## Optional Inputs
- **Prior thread**: Earlier emails so the recap continues the thread instead of starting a new one
- **Preferred length**: Short confirmation or detailed recap


## Workflow
1. Read the notes and separate decisions from discussion
2. Extract commitments and attach an owner and a date to each
3. Identify what was left open and write it as a question
4. Draft the recap in three scannable sections: agreed, next steps, still open
5. Close with a one-line invitation to correct anything that is wrong

## Decision Rules
- If a next step has no owner in the notes, propose one and ask the recipient to confirm
- If something was discussed but not agreed, it goes under still open, never under agreed
- If the notes contain internal commentary, keep it out of a client-facing recap
- If the meeting produced no decisions, send a short note with one proposed next step instead of a fake recap
- If a date was vague or missing, convert it to a specific day and mark it as proposed
- If attendees remembered a commitment differently, list it under still open as a question and do not pick a version
- If the recipient was not on the call, open with one line of context and do not assume they know the discussion
- If the notes contain a price, leave it out of the email and mention the omission to the operator only

## Edge Cases
- The notes are a transcript with no speaker labels
- The call ended without a decision on the main topic
- Six people attended and no owners were stated aloud
- The notes contain a price the operator does not want in writing yet
- The recap is going to someone who was not on the call
- Two attendees clearly remembered the same commitment differently

## Output Requirements
The output must:
- Separate agreed items, next steps, and open questions into distinct sections
- Give every next step an owner and a specific date, marking any date the notes did not give as proposed
- Keep the email under 200 words unless a detailed version was requested
- Write anything uncertain as a question rather than a statement
- End with a one-line invitation to correct the record

## Failure Handling
If required information is missing:
- If the notes name no owners, write the next steps as proposals and ask the recipient to confirm
- If no dates were discussed, propose specific ones and mark them as suggestions

If confidence is low:
- Keep the recap to what was clearly said and add a line asking what was missed
- Recommend the operator add their own context before sending

## Constraints
- Do not record an agreement that was not actually made
- Do not add commitments the operator did not make on the call
- Do not include pricing, internal notes, or side commentary in an external recap
- Do not summarize the conversation line by line — extract the decisions
- Do not exceed 200 words unless a detailed version was requested

## Examples Reference
See `/examples` for a worked standard case.
