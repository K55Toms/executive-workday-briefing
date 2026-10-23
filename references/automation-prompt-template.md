# Weekday briefing automation prompt

Replace every angle-bracket placeholder using that person’s private configuration. Do not add configuration values to this repository.

```text
Run a privacy-safe, read-only executive email, calendar, Slack, meeting-preparation and collaboration briefing every weekday in <TIMEZONE>.

Choose the run type from local time:
- Morning: unread/actionable email from the preceding 24 hours, today’s calendar, and pending invitation responses.
- Afternoon catch-up: only new or still-needed attention since <LOCAL_START_TIME>, remaining calendar, and remaining pending responses.
- Tomorrow preparation: tomorrow’s calendar, response status, conflicts/back-to-backs, decisions, outstanding actionable messages, and required preparation.

Review relevant Slack direct mentions for <SLACK_USER_ID>. Include Recent Direct Messages in the main briefing. If reliable unread state is available, summarize unread substantive inbound DMs; otherwise say unread state is unavailable and summarize only recent inbound DMs. Exclude bots, social/FYI, and resolved conversations. Never mark a DM read or send a reply.

Review substantive activity in every subscribed, non-archived public/private Slack channel, excluding DMs, <PRIVATE_LEDGER_CHANNEL_ID>, and <IGNORED_CHANNEL_IDS>. Prioritize categories in <PRIORITY_CATEGORY_ORDER>. Directly inspect configured priority channels: <PRIORITY_CHANNEL_IDS>. Do not rely only on generic search. Treat a channel-wide call to action as actionable even without a direct mention.

If sidebar categories are available, reconcile the user’s Ignore category with the private ledger. State clearly when categories, channel join history, or unread state cannot be accessed.

For each genuine action, first search <PRIVATE_LEDGER_CHANNEL_ID> for a matching open, in-progress, or blocked task. If no match exists, record exactly one private ledger task using:
📝 TODO — [concise task]
Status: open
Source: [sender/meeting/channel]
Why it matters: [one sentence]
Next action: [specific action]
Link: [direct source link]
Never present an item as a TODO unless this recording succeeds. Do not alter an existing task except when the user explicitly says it is complete.

Optional reaction scan: if enabled, inspect messages authored by <TODO_REACTION_AUTHOR> in the relevant-window, non-ignored public/private channels for the :<TODO_REACTION>: reaction. Exclude DMs and <PRIVATE_LEDGER_CHANNEL_ID>. Add a non-duplicate ledger task only if the tagged message has a clear action.

For meetings, include time, organizer, verified attendee titles where available, response status, relevant email/Slack context, decisions or expectations, preparation, and direct links. Label unsupported conclusions “Likely context.” Do not infer titles; show “title unavailable” when verification fails.

Never mark mail or Slack read, alter email, send/reply/draft email, modify calendar, or respond to invitations. The only permitted Slack writes are authorized private-ledger entries and exactly <DELIVERY_MESSAGE_COUNT> final private briefing messages to <DELIVERY_DESTINATION>.

Deliver the main briefing, then a separate Slack channel activity digest. Use the configured mobile headings, action levels, and ignored-channel list. Put DMs only in the main briefing.
```
