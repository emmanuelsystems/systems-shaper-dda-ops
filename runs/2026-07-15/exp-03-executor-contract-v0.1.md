---
title: EXP-03 Executor Contract
asset_type: delegation_contract
status: frozen_ready_for_dispatch
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-03-DDA-IMPLEMENTATION-DECISION-2026-07-15
logical_task_id: EXP-03-EXECUTE
---

# EXP-03 Executor Contract

## Task

Create the operational decision brief required by `exp-03-goal-and-measurement-contract-v0.1.md` and return a concise evidence/burden record.

## Goal Link

`EXP-03-DDA-IMPLEMENTATION-DECISION-2026-07-15`

## Allowed Inputs

Only the ten frozen sources named in the goal contract plus these frozen EXP-03 setup files:

- `exp-03-human-authorization-v0.1.md`;
- `exp-03-goal-and-measurement-contract-v0.1.md`;
- this executor contract;
- `exp-03-lane-ledger-v0.1.md` as it exists at dispatch.

Read committed parent objects for dirty July 14 paths. Do not use moving worktree changes as evidence.

## Allowed Outputs

Write only:

- `runs/2026-07-15/exp-03-dda-implementation-decision-brief-v0.1.md`;
- `runs/2026-07-15/exp-03-executor-return-v0.1.md`.

## Required Return

Record start/end timestamps, tool calls, files read/written, external calls, delegations, assumptions, material-claim coverage, goal traceability, interventions, corrections, defects, checks, and proof limitations. Do not self-accept or edit setup, ledger, manifest, verifier, scoreboard, source-index, or unrelated files.

## Gate

The root may freeze the primary return only if both files exist, the decision brief satisfies every required-content field, all material claims are anchored, prohibited actions remain zero, and no moving dirty source was used.

## Escalation

Return `held` without inventing content if a material source conflict cannot be resolved, a required claim lacks evidence, or the task would require any prohibited action.
