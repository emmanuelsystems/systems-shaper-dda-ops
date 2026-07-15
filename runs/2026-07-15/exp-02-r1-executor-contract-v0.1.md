---
title: EXP-02-R1 Executor Contract
asset_type: specialist_delegation_contract
status: frozen_for_execution
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
iteration_id: EXP-02-R1
logical_task_id: EXP-02-R1-EXECUTE
original_candidate_sha: bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5
---

# EXP-02-R1 Executor Contract

## Task

Create a separately identified R1 candidate that repairs only the defects in `exp-02-verifier-return-v0.1.md`. Preserve the original EXP-02 artifacts and result unchanged.

## Frozen Inputs

- `exp-02-goal-and-measurement-contract-v0.1.md`
- `exp-02-researcher-return-v0.1.md`
- `exp-02-researcher-return-qualification-v0.1.md`
- original candidate at `bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5`
- `exp-02-verifier-return-v0.1.md` from verifier-result commit `b4bbf9cac7e71c08f3802edf0770f61ebbfa3aa1`
- `human-decision-record-exp-02-r1-authorization-v0.1.md`

## Exact Goal

Use this wording verbatim:

> Establish a repeatable, review-only post-meeting-to-execution sequence that converts source-backed meeting direction into one measurable implementation goal, complete owner-tagged tasks, an unsent progress update, and one explicit human decision.

## Requested Files

Create only:

1. `runs/2026-07-15/exp-02-r1-post-meeting-execution-candidate-v0.1.md`
2. `runs/2026-07-15/exp-02-r1-executor-return-v0.1.md`

## Required Repairs

- Copy the original candidate into the R1 lineage without modifying the original file.
- Restore the exact goal above.
- State truthfully that R1 restores the root-qualified goal after the original verifier found drift; do not claim the original candidate was unchanged or passed.
- Count recovery inputs as physical files. Use an explicit list of no more than five physical files capable of recovering goal, lineage, candidate, and evidence.
- Preserve the seven goal-linked tasks, required fields, source limitations, unknown baseline values, unsent-update boundary, and all non-claims unless a change is necessary for R1 accuracy.
- Measure R1 executor burden separately from the original iteration.

## Rules

- Edit only the two requested files.
- No external reads or writes, commits, pushes, messages, task delegation, runtime changes, or edits to original EXP-02 artifacts.
- Do not create or promote a skill, permanent agent, automation, frontend, model policy, infrastructure, or canon.
- Do not self-accept. R1 remains pending root reconciliation, exact-SHA freeze, independent verification, and the human gate.

## Return Requirements

Record exact artifacts, evidence used, deterministic checks, timing, tool-call burden, clarifications, redirections, corrections, assumptions, defects, proof limitations, and recommended next action.
