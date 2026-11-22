---
name: meeting-prep-brief
description: Create a prep brief with context, goals, risks, and suggested questions before customer, candidate, or internal meetings. Use when you have a customer, candidate, or internal meeting coming up and some notes or history to turn into a one-page prep brief.
license: CC-BY-4.0
compatibility: generic-agent, claude-style-workflow, chatgpt-project
metadata:
  author: OutcomeKit
  version: "1.1.0"
  category: ops
  pack-tier: basic
---

# Meeting Prep Brief

## Purpose
This skill turns scattered notes into a concise prep brief that helps people show up sharp. It packages relevant context, meeting goals, open questions, and what would make the conversation successful.

## Best Use Cases
- Preparing for a customer renewal conversation with usage data and open tickets
- Briefing a founder before a board meeting with key metrics and asks
- Getting context on a candidate before a final-round interview

## Required Inputs
- **Meeting notes or thread**: Calendar invite, notes, email thread, or CRM context
- **Meeting objective**: The outcome you want from the conversation

## Optional Inputs
- **CRM history**: Past deal notes, support tickets, or account health data
- **Attendee profiles**: LinkedIn or internal profiles of other participants


## Workflow
1. Ingest meeting notes, calendar context, and any related thread history
2. Identify the meeting type (for example renewal, first conversation, candidate interview, internal review) from the notes, and the primary objective; if the type is unclear, say so
3. Extract relevant context: relationship history, open issues, recent changes
4. Generate a suggested agenda aligned with the stated objective (skip it if the operator asked only for prep questions)
5. Draft 3-5 smart questions to advance the conversation
6. Flag risks or unknowns that need validation during the meeting
7. Append a follow-up reminder structure for after the meeting

## Decision Rules
- If the meeting is a renewal, include usage data and open support tickets; if the notes do not contain them, list them as missing
- If the meeting is a first conversation, focus on research and discovery questions
- If multiple attendees are listed, note each person's role and any priorities stated in the notes; where none are stated, say so instead of guessing
- If prior context is thin, recommend opening with a framing question to establish baseline
- If the meeting objective is vague, suggest clarifying it before the conversation
- Treat the brief as internal unless the operator says it will be shared; if it will be shared, leave out internal-only notes such as pricing limits and risk assessments

## Edge Cases
- The only context available is a calendar invite with a vague subject line
- The meeting was rescheduled three times and the original context is stale
- The attendee list changed since the invite was sent
- The meeting is a follow-up to a conversation the operator did not attend
- Notes reference internal jargon or acronyms without definitions
- The meeting objective is a difficult conversation (cancellation, pricing pushback, performance review)

## Output Requirements
The output must:
- State the meeting goal in one sentence
- Include relevant context from provided notes and history
- Suggest 3-5 questions tailored to the meeting objective
- Flag risks or unknowns to validate during the conversation
- Include a follow-up structure for after the meeting

## Failure Handling
If required information is missing:
- If only a calendar invite is available, generate a minimal brief focused on smart questions
- If the meeting objective is unclear, suggest clarifying it as the first agenda item

If confidence is low:
- Keep the brief shorter and focus on questions rather than assertions
- Recommend the operator add their own context before the meeting

## Constraints
- Do not fabricate context not present in the provided notes
- Do not assume the meeting outcome or pre-judge the attendees
- Do not include confidential internal notes in an external-facing brief
- Do not replace the operator's stated objective with a different one
- Do not generate a full meeting agenda when only prep questions were requested

## Examples Reference
See `/examples` for a worked standard case.
