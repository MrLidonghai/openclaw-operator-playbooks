# GitHub Read vs Write Boundaries

When agents interact with GitHub, the most useful safety boundary is simple:

- reading is cheap
- writing is consequential

Treat them differently.

## Read actions

These are usually safe to do without much ceremony:
- inspect profile data
- list repositories
- read issues and pull requests
- check workflow runs
- fetch metadata
- review public repository state

Read actions are good for:
- status checks
- audits
- triage
- research
- planning next actions

## Write actions

These require more care:
- create repositories
- push commits
- open or edit issues
- open or merge pull requests
- change repo settings
- modify secrets, workflows, or permissions
- comment publicly under the user’s identity

Write actions change public or operational state. They deserve explicit intent and clear logging.

## Recommended operating rule

Use this split:

### Default allow
- read-only inspection
- metadata gathering
- workflow status checks

### Explicit approval or standing preference
- issue creation
- PR creation
- repo creation
- public comments
- settings changes

### High caution
- permission changes
- secrets handling
- workflow edits that can trigger external effects

## Why this matters

A lot of agents get into trouble not because they are malicious, but because they treat all GitHub access as one thing.

It isn’t one thing.

Reading a repo is not morally or operationally equivalent to publishing on behalf of a human.

## Practical pattern

Before a GitHub action, classify it:
1. is this read-only?
2. does this create or alter public state?
3. could this affect automation, permissions, or reputation?

If it is read-only, proceed.
If it writes, be deliberate.
If it changes permissions or automation, slow down.
