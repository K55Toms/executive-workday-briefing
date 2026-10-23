---
name: executive-workday-briefing
description: Create or run a privacy-safe weekday executive briefing that summarizes connected email, calendar, Slack, meetings and tracked actions. Use when a user wants a personal daily work briefing or to configure one for a team; do not use for sending routine messages unrelated to the briefing.
---

# Executive Workday Briefing

Create a concise, mobile-friendly briefing from the user's connected email, calendar, and Slack. Begin by reading [the configuration template](references/team-config-template.md), then adapt it to the user's stated preferences and available connectors.

## Privacy and authorization

- Treat every person, mailbox, channel, user ID, event link, company name, and workspace URL as private configuration. Never copy these into reusable files or examples.
- Do not create an external repository, invite collaborators, or publish a repository without the user's explicit destination and visibility choice.
- Keep the workflow read-only unless the user has explicitly authorized the exact write. Commonly safe writes are a dedicated private action ledger and the final briefing DM; everything else remains read-only.
- Never mark messages read, alter mail, change calendar responses, or send email as part of the briefing.

## Workflow

1. Establish the delivery window and run type in the user's timezone: morning, afternoon catch-up, or tomorrow preparation.
2. Read the relevant email and calendar items, distinguishing actionable work from FYI, automation, cancellations, and completed threads.
3. For Slack, inspect direct mentions, recent inbound DMs when unread state is supported, subscribed channels, and any configured priority categories. State clearly if a connector cannot expose unread state, sidebar categories, or join history.
4. Treat direct or channel-wide asks as actions only when there is a specific next step. Before surfacing an action, check for a matching open item in the private ledger; record a non-duplicate ledger entry only if the user has authorized that ledger.
5. Prepare meeting context from invitations, relevant email, Slack context, and verified attendee data. Label inference as “Likely context”; never infer job titles from names, seniority, or subjects.
6. Deliver the requested main briefing and separate Slack channel digest using the agreed recipient and count of messages.

## Content rules

- Use the headings and priority conventions in the user’s configuration. Keep each section short enough for a phone.
- Direct messages belong in the main briefing, not the channel digest.
- If a Slack connector cannot reliably return unread state, call the section “Recent Direct Messages” and say why; do not label messages unread.
- For reaction-based actions, scan only the exact author/reaction relationship the user requests. Exclude DMs and the action ledger unless the user explicitly includes them.
- Maintain an explicit ignore list. Synchronize any user-managed ignore category only when its available connector data makes the state verifiable.
- When reporting a task as complete, do so only after the user explicitly says it is complete or the underlying source conclusively demonstrates completion.

## Resources

- Use [the configuration template](references/team-config-template.md) to gather the team member’s preferences and identifiers outside the shared repository.
- Use [the automation prompt template](references/automation-prompt-template.md) when creating a recurring scheduled briefing.
