# OutcomeKit free agent skills

Three free workflow packs for founders and small teams, from [OutcomeKit](https://outcomekit.ai). Each one follows the open [Agent Skills](https://agentskills.io) format, so it works with Claude Code, Cursor, Hermes Agent, OpenClaw and other SKILL.md-compatible agents.

| Pack | What you get |
|---|---|
| [Meeting Prep Brief](skills/meeting-prep-brief) | A one-page brief with context, goals, risks and questions before a customer, candidate or internal meeting |
| [Weekly Metrics Summary](skills/weekly-metrics-summary) | What moved this week, likely drivers and what to discuss at your team sync |
| [Weekly Founder Update Writer](skills/weekly-founder-update-writer) | An investor, advisor or team update from a week of scattered notes |

Each pack includes `SKILL.md` (instructions and decision rules), `manifest.json`, a buyer-facing `README.md` and a worked example.

## Install

Copy a pack folder from `skills/` into your agent's skills directory. Keep the folder name as-is.

| Agent | Skills directory |
|---|---|
| Claude Code | `~/.claude/skills/` (global) or `.claude/skills/` (project) |
| Cursor | `.cursor/skills/` |
| Hermes Agent | `~/.hermes/skills/` |
| OpenClaw | `skills/` in your workspace, or `~/.openclaw/skills/` |

```bash
git clone https://github.com/webshark/outcomekit-free-agent-skills
cp -R outcomekit-free-agent-skills/skills/meeting-prep-brief ~/.claude/skills/
```

Full guide: [How to install an AI workflow pack](https://outcomekit.ai/learn/how-to-install-ai-workflow-pack)

## Want more?

These are OutcomeKit's free packs. The paid packs add input and output schemas, six worked examples, test cases and a QA checklist:

- [Qualify Inbound Leads](https://outcomekit.ai/skills/qualify-inbound-leads): score each new lead for fit, urgency and next step against your ideal customer profile
- [Browse all packs](https://outcomekit.ai/browse)

## License

Copyright (c) 2026 OutcomeKit. Licensed under [CC BY 4.0](LICENSE). Use, share and adapt freely, including commercially, with credit to OutcomeKit and a link to [outcomekit.ai](https://outcomekit.ai).
