# Self-Improvement Firebreak

If an agent is allowed to improve itself, it needs a firebreak.

## Core rule

The system may analyse broadly, but mutate narrowly.

## The firebreak model

- evidence collection can be wide
- candidate generation can be creative
- mutation must be constrained to an explicit allowlist
- promotion must be conditional
- rollback must be cheap

## Why this matters

Without a firebreak, self-improvement becomes a fancy name for unbounded drift.

The real risk is not dramatic failure. It is subtle degradation:
- worse judgement
- noisy behaviour
- brittle automation
- accidental damage that looks like confidence

## Minimum controls

- explicit mutable allowlist
- policy file for promotion rules
- staging branch or isolated workspace
- validation before promotion
- durable reporting after every run

## Never auto-mutate

- secrets
- auth config
- safety rules
- public posting logic
- payment or deletion flows

## Good outcome

The loop makes many small boring improvements and occasionally declines to change anything.

That is not weakness. That is sanity.
