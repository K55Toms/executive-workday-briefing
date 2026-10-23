# Executive Workday Briefing

A shareable Codex skill for creating privacy-safe weekday email, calendar, Slack, meeting-preparation, and action-ledger briefings.

The repository intentionally contains no people, channels, workspace IDs, schedule destinations, company names, or message data. Each person keeps their completed configuration outside the repository, then uses the included automation prompt template to create their own scheduled briefing.

## Contents

- `SKILL.md` — reusable briefing workflow and safety rules.
- `references/team-config-template.md` — private per-person configuration template.
- `references/automation-prompt-template.md` — placeholder-based automation prompt.

## Use

1. Copy the private configuration template to an approved private location and fill it in.
2. Install or copy the `executive-workday-briefing` skill into the user’s Codex skills directory.
3. Use the automation prompt template with their approved connectors and delivery destination.

Review connector permissions before enabling a schedule. The default workflow is read-only except for explicitly approved private action-ledger entries and final briefing delivery.
