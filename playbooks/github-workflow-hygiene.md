# GitHub Workflow Hygiene

This playbook is about using GitHub in a way that stays useful as repositories, agents, and automation multiply.

## Goal

Keep GitHub work readable, reversible, and respectful of the difference between observation and action.

## Core habits

- separate read-only inspection from write actions
- do not create noisy issues or PRs just to prove activity
- use clear commit messages
- avoid giant mixed-purpose changes
- leave enough explanation for future review

## Healthy workflow

1. inspect current repository state
2. identify the smallest useful next action
3. make a scoped change
4. validate it
5. write a clear commit message
6. create a PR or issue only when it adds real value

## Common failure modes

- opening issues that do not help anyone
- creating vanity commits
- mixing refactors with behavioural changes
- using automation to increase activity instead of usefulness
- making public changes without a clear reason

## Agent-specific rule

If an agent is acting on GitHub:
- read freely where appropriate
- write deliberately
- log what changed
- avoid pretending that activity equals progress

## Reputation reality

Stars, achievements, and contribution graphs are downstream effects.

The thing that actually compounds is useful work that other people can discover, understand, and trust.

Optimise for that first.
