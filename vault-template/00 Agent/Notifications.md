---
type: rules
---
# Notifications (ntfy)

How the agent sends reminders to the phones, and how to rebuild it from scratch.

## In short
- The phones run the **ntfy** app, subscribed to a private topic on `ntfy.sh` (or a self-hosted server).
- The topic name works like a password: it lives in the password manager and in the environment variable `NTFY_TOPIC`, never in this vault.
- Reminders within the next 3 days go to ntfy (the service's limit for scheduled messages); anything later goes to the calendar.
- Priority 4 for ordinary reminders, 5 for important ones.

## New phone
1. ntfy app → **+** → topic → Subscribe.
2. In the topic screen: **⋮ → Enable instant delivery** (otherwise messages can arrive late through the phone vendor's push channel).
3. Battery settings for ntfy: **Unrestricted**.
4. Turn off the calendar app's own notifications: one channel per job.

## How the agent sends
```
scripts/ntfy-send "Call the garage" --title "Reminder" --at "2026-11-03 15:00"
scripts/ntfy-send "Water the plants" --in "2h"
```
The script refuses quiet hours (Sunday 09:00–12:00, nights 22:00–07:00) unless `--night yes` is given because someone explicitly asked.

## Rebuild from scratch
1. Copy `scripts/ntfy-send` and make it executable.
2. Set `NTFY_TOPIC` (and `NTFY_SERVER` if self-hosted) in the agent's environment.
3. Allow the agent to run the script without asking each time.
4. Send a test message.
