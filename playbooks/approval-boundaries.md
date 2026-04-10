# Approval Boundaries

Good operator setup depends on one boring but important distinction:

Some actions are safe to automate.
Some actions should still ask first.

If you blur those together, the agent either becomes useless or dangerous.

## Goal

Define approval boundaries that preserve autonomy for low-risk work while keeping humans in control of consequential actions.

## Actions that are usually safe without asking

- reading local files
- reviewing logs and memory
- collecting read-only GitHub data
- drafting documents, plans, and suggestions
- low-risk housekeeping inside the workspace
- preparing patches without applying them externally

These actions help the operator without changing outside state.

## Actions that should usually ask first

- public posting
- sending emails or messages
- creating or editing issues or PRs in your name
- publishing repos or packages
- deleting files or performing destructive resets
- touching permissions, secrets, or auth
- spending money or making purchases

These actions create external consequences.

## The middle category

Some actions can become auto-allowed if the operator explicitly chooses that posture.

Examples:
- creating draft GitHub repos
- scheduling low-risk cron jobs
- updating non-sensitive config files
- promoting validated changes from a staging branch

The trick is to make that permission explicit, narrow, and reversible.

## Good policy design

A useful approval policy should be:
- easy to understand
- easy to audit
- narrow enough to prevent surprise
- broad enough that the agent can still be useful

## Failure modes

### Too strict
The agent asks about everything and becomes an expensive menu system.

### Too loose
The agent starts taking identity-bearing or destructive actions without a clear operator decision.

## Recommended rule of thumb

- read freely
- draft freely
- prepare safely
- publish deliberately
- delete cautiously
- expand access rarely

## Logging

Whenever an action crosses an approval boundary, the reason should be visible.

That way the operator is not forced to reverse-engineer why the agent thought a risky action was acceptable.
