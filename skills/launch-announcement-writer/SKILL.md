---
name: launch-announcement-writer
description: Turn a product update into launch posts for X, LinkedIn, and email. Use when you have shipped a product update and need an X post, a LinkedIn post, and a launch email with one call to action, or a plain answer that it is too small to announce.
license: CC-BY-4.0
compatibility: generic-agent, claude-style-workflow, codex-style-workflow, mcp-friendly
metadata:
  author: OutcomeKit
  version: "1.1.0"
  category: marketing
  pack-tier: basic
---

# Launch Announcement Writer

## Purpose
This skill turns a product update into the three posts you actually need on launch day: a short X post, a longer LinkedIn post, and an email to your list. Each one is written for its format rather than the same paragraph pasted three times.

## Best Use Cases
- Announcing a feature the same afternoon it ships
- Writing the X, LinkedIn, and email versions of one update without repeating yourself
- Deciding whether a small change deserves a post or belongs in the next roundup

## Required Inputs
- **What shipped**: The update and what it changes for the person using it
- **Audience and CTA**: Who you are announcing to and the one action you want them to take

## Optional Inputs
- **Voice reference**: Optional. A past post you liked, so the drafts match your tone.
- **Screenshot or demo link**: The asset each post points at
- **Recent announcements**: What you have already posted, so the launch does not repeat itself


## Workflow
1. Identify what changed for the user, not what was built
2. Decide whether the update is substantial enough to announce on its own (it is if users can do something they could not before, something takes noticeably less effort, or they must act because something is being removed)
3. Write the X post: one hook, one concrete detail, one link
4. Write the LinkedIn post: the problem it solves, what shipped, why it matters
5. Write the launch email with two subject line options
6. Apply the same call to action across all three versions

## Decision Rules
- Lead every version with the user-facing change, never with the feature name
- If the update is a bug fix or a minor tweak, say it is too small to announce on its own and write a one-line roundup entry instead of three posts, unless it corrects something you previously said worked, in which case announce it as a correction in plain words
- If the update is an internal refactor with no visible change, write no launch post and say why
- If the update is limited to some accounts or is in beta, say who has it and when everyone else gets it, and never write that it is available to everyone
- If the update removes or deprecates something, lead with what is going away, the date, and what to do instead
- If several small things shipped together, write one post that groups them under the change users care about most, not one post each
- If the product has no audience on a channel, still write that version but tell the founder it can wait until there are followers there
- Use [link] and [screenshot] placeholders; never invent a URL or describe an image that was not provided
- Keep the X post under 60 words and the LinkedIn post under 150
- Use one call to action across all three channels so the launch reads as a single message
- If recent announcements are supplied, do not reuse their hook or phrasing, and say so when this update continues one
- If no voice reference is given, write plainly and keep launch-day hype words out entirely

## Edge Cases
- The update is an internal refactor with no visible user-facing change
- The feature ships to a subset of accounts rather than everyone
- The change is a removal or a deprecation rather than an addition
- The product has no existing audience on any of the three channels
- The update fixes something the company previously said was working
- Three small things shipped the same week and each could be its own post

## Output Requirements
The output must:
- Provide three drafts sized for X, LinkedIn, and email, unless the update is too small to announce (see the last item)
- Lead each version with the user-facing change, not the feature name
- Give two subject line options for the email
- Use the same single call to action across all three channels
- Say plainly when an update is too small to announce on its own, and give a one-line roundup entry instead of the three drafts

## Failure Handling
If required information is missing:
- If the user-facing benefit is unclear, ask what changes for the person using the product before writing anything
- If no voice reference is given, write plainly and flag that the drafts are not tone-matched

If confidence is low (the update is borderline, or the input does not support an impact claim):
- Provide the LinkedIn version only and recommend bundling the update into the next roundup
- Flag any claim about impact that the input does not support

## Constraints
- Do not claim results, adoption numbers, or time savings the input does not support
- Do not describe a minor update as a major launch
- Do not paste the same text across all three channels
- Do not use hype words like revolutionary, game-changing, or unlock
- Do not announce a feature as generally available when it is limited or in beta

## Examples Reference
See `/examples` for a worked standard case.
