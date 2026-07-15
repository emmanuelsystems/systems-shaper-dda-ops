---
title: EXP-02 Researcher Contract
asset_type: specialist_delegation_contract
status: frozen_dispatch_authorized
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
logical_task_id: EXP-02-RESEARCH
---

# EXP-02 Researcher Contract

## Task

Read only the frozen source set in `source-index.md`. Return a source-anchored map of meeting directions, candidate implementation goals, dependencies, conflicts, unknowns, and the most defensible goal for the executor.

## Required Return

1. Task reference and timing.
2. Source coverage.
3. Confirmed directions versus proposals.
4. Three or fewer candidate implementation goals.
5. Goal comparison and selected recommendation.
6. Manual baseline for the post-meeting workflow, using `unknown` where evidence is absent.
7. Source conflicts and missing evidence.
8. Proof limitations and executor constraints.

## Rules

- Read only; do not edit files or write externally.
- Do not use uncommitted EXP-01 artifacts as proof that EXP-01 passed.
- Separate direct evidence, inference, and unknown.
- Do not recommend skills, agents, automation, or frontend work unless the source evidence proves they are required for this bounded objective.
- Return `held` if the source set cannot support one bounded goal.
