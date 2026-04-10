# Self-Improve Example Pack

This folder contains small reference files for a firebreak-based self-improvement setup.

## Files

- `state/allowlist.example.json`
- `state/policies.example.json`

## Purpose

These are not universal defaults. They are starting points.

Use them to:
- define a mutation surface
- block obviously dangerous targets
- set promotion rules conservatively
- give the operator something concrete to review

## Usage notes

- start narrow
- keep blocked paths broader than mutable paths
- allow more only after repeated stable behaviour
- avoid copying examples blindly into a live system without review
