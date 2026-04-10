# OpenClaw Operator Playbooks

Practical playbooks, patterns, and field notes for running OpenClaw agents safely and usefully.

This repository is for people who want agents that are actually helpful, not just theatrically autonomous.

## What this repo is for

- operating OpenClaw agents with clear guardrails
- reducing noisy or unsafe automation
- improving memory, scheduling, and task hygiene
- documenting repeatable patterns that work in real use
- turning lessons from live agent operations into reusable playbooks

## What’s inside

### `playbooks/`
Step-by-step operator guides for common tasks and recurring workflows.

Current topics:
- safe scheduled runs
- memory maintenance
- agent self-improvement operating notes
- GitHub workflow hygiene
- approval boundaries
- operator review rhythm

### `patterns/`
Small reusable patterns for things like:
- safe cron usage
- approval boundaries
- memory maintenance
- GitHub read/write separation
- self-improvement with firebreaks

### `examples/`
Concrete examples, templates, and reference files.

## Why this exists

A lot of agent tooling is either too timid to be useful or too reckless to trust.

The goal here is the middle path:

- autonomous where it should be
- constrained where it must be
- observable, testable, and reversible

## Who this is for

- people operating OpenClaw in personal or small-team contexts
- builders experimenting with long-running agents
- anyone tired of “self-improving” systems that are mostly self-damaging

## Roadmap

### Phase 1
- publish core playbooks
- add practical examples
- refine repository structure

### Phase 2
- add operator checklists
- add reference configurations
- add case studies from real runs

### Phase 3
- add small tooling helpers where they genuinely reduce friction

## Contributing

Contributions are welcome if they improve clarity, safety, or real-world usefulness.

The bar is simple:
- be practical
- be honest
- don’t add complexity for vanity

## License

MIT
