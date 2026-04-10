# Agent Self-Improvement Operating Notes

This document is for operators who want agents to improve over time without drifting into reckless self-modification.

## The real objective

The goal is not to make an agent endlessly rewrite itself.

The goal is to make it:
- learn from mistakes
- get more useful over time
- keep changes observable
- avoid silent degradation
- stay recoverable when it gets something wrong

## What should improve automatically

These are good candidates for autonomous improvement:
- memory quality
- checklists
- operating notes
- prompt refinements
- task-specific SOPs
- summaries of repeated lessons

These changes are usually small, reversible, and easy to validate.

## What should improve cautiously

These are possible, but require tighter controls:
- skill logic
- helper scripts
- workflow configuration
- validation routines

Treat these as medium-risk. Use tests, a staging branch, and rollback.

## What should not self-mutate freely

Do not allow unrestricted mutation of:
- secrets
- authentication material
- safety policies
- public posting logic
- payment or deletion actions
- external account configuration

If the agent can freely change these, you no longer have an assistant. You have a problem.

## The firebreak model

A sane self-improvement loop has five phases:

1. **Observe**
   - inspect recent runs, memory, failures, and corrections
2. **Distil**
   - turn repeated signals into candidate improvements
3. **Constrain**
   - limit changes to explicitly allowed files and patterns
4. **Validate**
   - test, inspect diff intent, and check policy boundaries
5. **Promote or roll back**
   - keep the win or undo it immediately

This matters because the most dangerous failures are usually subtle. The agent does not explode. It just gets a bit worse while sounding very pleased with itself.

## Promotion rules

A self-generated change should only be promoted if:
- the target files are allowlisted
- the diff matches the claimed intent
- no new permission scope appears
- no new network reach is introduced without approval
- validation passes
- rollback is simple

If any of those fail, do not be heroic. Roll it back.

## Signs the loop is going bad

Watch for:
- increasingly large diffs
- vague justifications for changes
- repeated edits to the same unstable area
- broader permissions over time
- more network behaviour creeping in
- declining usefulness despite more activity

A busy agent is not the same thing as an improving agent.

## Recommended operating cadence

Good default:
- one deep review per day
- one light retrospective later in the day

Maybe acceptable:
- up to four runs per day for a stable, well-bounded system

Bad idea:
- constant unattended self-editing loops every few minutes

## Logging

Every self-improvement run should leave a visible trace:
- what was observed
- what was proposed
- what changed
- what was tested
- whether it promoted or rolled back
- what was learned

No invisible magic. If it changed itself, it should be able to show its homework.

## Success criteria

A healthy self-improvement system should:
- make small useful gains
- reduce repeated mistakes
- occasionally decide to change nothing
- remain understandable to the operator

That last one matters. If you cannot understand why it improved itself, you are not operating it. You are just watching it improvise.
