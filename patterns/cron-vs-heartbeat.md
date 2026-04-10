# Cron vs Heartbeat

Use the right mechanism for the job.

## Use cron when

- exact timing matters
- the task should run later or repeatedly on a schedule
- the task is self-contained
- you want isolation from the main conversation
- you want a reminder at a real time

Examples:
- remind me at 9:00
- send a morning summary every weekday
- review a backlog every evening

## Use heartbeat when

- several lightweight checks can be batched
- slight timing drift is acceptable
- recent conversation context matters
- you want quiet, opportunistic maintenance

Examples:
- rotate through inbox, calendar, and project checks
- maintain memory files
- do light housekeeping when nothing urgent is happening

## Anti-patterns

Do not use:
- `sleep` loops as fake scheduling
- repeated polling to simulate reminders
- cron for tasks that require constant human judgement

## Rule of thumb

- precise and scheduled = cron
- lightweight and opportunistic = heartbeat
