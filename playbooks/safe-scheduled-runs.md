# Safe Scheduled Runs

This playbook explains how to run OpenClaw agents on a schedule without creating noisy, destructive, or misleading automation.

## Goal

Create scheduled routines that are useful, observable, and easy to stop.

## Principles

- use cron for future work, not shell sleep loops
- prefer a few meaningful runs over constant chatter
- schedule isolated work when exact timing matters
- keep destructive or high-risk actions out of unattended schedules
- make outputs easy to audit

## Good candidates for scheduled runs

- daily summaries
- inbox or project review
- memory maintenance
- reminder delivery
- report generation
- low-risk retrospection

## Bad candidates for scheduled runs

- unattended external posting
- open-ended self-modifying loops
- anything that requires fresh human judgement every time
- repeated polling dressed up as automation

## Recommended pattern

1. define the exact purpose of the scheduled task
2. choose cron when timing matters
3. use isolated execution for standalone tasks
4. keep the task prompt narrow and specific
5. define what success looks like
6. define what should trigger a user-facing alert
7. review the first few runs before trusting it

## Safety checks

Before enabling a schedule, ask:
- does this task write externally?
- can it delete or overwrite important data?
- does it need secrets or broad permissions?
- will failure be obvious?
- can I disable it quickly if it goes weird?

If the answer looks uncomfortable, add a human gate.

## Output hygiene

A scheduled task should never claim it sent, queued, or completed something unless it actually did.

Be precise:
- say "prepared" when something was prepared
- say "scheduled" only when a real job exists
- say "sent" only when delivery actually happened

## Recommended cadence

- one deep scheduled review per day
- one light retrospective later in the day
- avoid minute-level loops unless there is a very strong operational reason

## Review loop

For the first week:
- inspect every run
- record false positives
- tighten prompts and scope
- reduce noise before increasing frequency
