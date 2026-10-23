# Executive briefing configuration

Copy this into a private location for each person. Do not commit filled-in values.

```yaml
person:
  display_name: "<name>"
  timezone: "<IANA timezone>"
  delivery:
    destination: "<private Slack DM user ID or approved destination>"
    main_and_digest_message_count: 2

schedule:
  weekday_times_local:
    - "08:30" # morning
    - "14:30" # afternoon catch-up
    - "16:00" # tomorrow preparation

slack:
  direct_mention_user_ids: ["<user ID>"]
  private_ledger_channel_id: "<private channel ID>"
  priority_categories: ["<category names in preferred order>"]
  priority_channels: ["<channel ID>"]
  ignored_channels: ["<channel IDs>"]
  review_all_subscribed_channels: true
  include_recent_direct_messages: true
  todo_reaction:
    enabled: false
    author: "<message author: self or named user>"
    reaction: "todo"
    exclude_channels: ["<private ledger channel ID>"]

email:
  source: "primary mailbox"
  actionable_window: "morning: previous 24h; afternoon: since 08:30 local"
  excluded_senders_or_patterns: ["<optional automation patterns>"]

calendar:
  include_pending_responses: true
  include_verified_attendee_titles: true

ledger:
  enabled: true
  format: |
    📝 TODO — <concise task>
    Status: open
    Source: <source>
    Why it matters: <one sentence>
    Next action: <specific action>
    Link: <direct source link>
```

Use opaque IDs rather than names where a connector supports them. Keep this file private because it maps people and delivery destinations to internal systems.
