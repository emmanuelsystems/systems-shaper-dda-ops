---
title: PMOT-01 Revised Decision Paths, Lane Authorization, and Execution Shape
asset_type: test_authorization
status: lanes_authorized_not_started
version: v0.2
owner: David Abiera
created: 2026-07-27
branch: codex/david-934fbd7-alignment-disposition-return-20260727
parent_sha: ec8f126520d28bf6eff6952c69c7098e008dfab9
test_id: PMOT-01
supersedes_question_artifact: pre-meeting-outcome-test-question-and-manual-baseline-v0.1.md
manual_baseline_id: PMB-2026-07-23
manual_baseline_sha: b1e8e4bd006a455aac45db54cb4d1a1dba9515b0
approval_scope: revised_decision_paths_and_bounded_lane_execution
lane_authorization: authorized_not_dispatched
experiment_status: not_started
runtime_claim: none
automation_claim: none
external_write_claim: scoped_branch_commit_and_push_only
---

# PMOT-01 Revised Decision Paths, Lane Authorization, and Execution Shape

## Correction to v0.1

The v0.1 candidate actions mixed different levels:

- one vague outcome run;
- one evidence-recovery prerequisite; and
- one research prerequisite.

That comparison was weak. This v0.2 replaces the three actions with comparable
paths toward the same target: one bounded real-world DDA pilot.

The manual baseline `PMB-2026-07-23`, its scorecard, unknowns, measurement
definitions, quality gates, and material-improvement gate remain unchanged.

## Revised Frozen Decision Question

Which path should govern the next DDA cycle toward one bounded real-world
outcome?

### Path 1 — `PILOT_NOW`

Authorize one exact, live, bounded pilot in `dda-agent-ops` without waiting for
the five historical objects or SSI-120.

Selection requirements:

- name the exact live use case, repository evidence, owner, user outcome, and
  stop condition;
- show that neither CTR-01-R1 recovery nor an SSI-120 architecture decision is a
  dependency; and
- keep `systems-shaper-dda-ops` as the review/control surface rather than
  treating it as runtime evidence.

If no exact live use case can be named from verified evidence, classify this
path `BLOCKED_UNKNOWN_USE_CASE`.

### Path 2 — `RECOVER_THEN_PILOT`

Recover and independently review exact CTR-01-R1 candidate
`ed0410f6033462eff9046bb0f72957fdaf2ca4c4` and verifier result
`ee379505cbcefb25f2a5fa9ec50dfcb6b1b37640`, then proceed to a named pilot.

Select this path only if the brief proves that current-truth retrieval is a
required capability for the named pilot and that the missing lineage materially
blocks safe execution.

### Path 3 — `COMPARE_THEN_PILOT`

Create the missing contract-complete SSI-120 comparison artifact, make one
human orchestration-pattern decision, then proceed to a named pilot.

Select this path only if the brief proves that orchestration-pattern choice is
the actual blocker for the named pilot. An open Linear issue or interesting
architecture is insufficient.

### Allowed Hold

Return `HOLD` if:

- no exact pilot use case is currently evidenced;
- two paths remain equally supported;
- a required authority or dependency is unknown; or
- the decision brief cannot distinguish a real blocker from optional research.

## Decision Standard

Select the shortest evidence-backed path to a real user outcome without hiding a
necessary safety or provenance dependency.

The decision brief must return exactly one of:

- `PILOT_NOW`;
- `RECOVER_THEN_PILOT`;
- `COMPARE_THEN_PILOT`;
- `HOLD`.

It must also name:

- the exact proposed pilot use case;
- owner;
- user outcome;
- controlling evidence;
- required dependency;
- first bounded action;
- stop condition; and
- explicitly unauthorized work.

## Lane Authorization

David authorizes the following bounded PMOT-01 lanes. Authorization permits
later dispatch under this exact contract. No lane is dispatched by this record.

Every specialist dispatch must use a self-contained task packet and
`fork_turns = "none"`. The root records route acceptance from the dispatch
result and does not infer model identity from child prose.

### Root Orchestrator

Owner: the current Codex task model.

Responsibilities:

- preserve this frozen question and baseline;
- dispatch each specialist with a self-contained packet;
- validate every return;
- resolve conflicts without averaging them;
- freeze the decision-brief candidate;
- release the verifier only after freeze; and
- return the verified brief to David for the human disposition.

The root may not change the candidate paths, material-improvement gate, or human
decision boundary.

### Researcher

Mode: read-only.

Allowed sources:

- exact GitHub objects and branches in `systems-shaper-dda-ops`;
- `dda-agent-ops` only to identify and evidence a live pilot use case;
- current Linear and Slack status as coordination context; and
- current repository governance.

Required findings:

1. the strongest exact live pilot candidate, or
   `BLOCKED_UNKNOWN_USE_CASE`;
2. whether CTR-01-R1 is a true dependency for that pilot;
3. whether SSI-120 is a true dependency for that pilot;
4. evidence, conflicts, unknowns, and failed recoveries for each path; and
5. source and recovery-burden counts.

Prohibited:

- edits;
- Slack, Linear, or other external writes;
- historical-object reconstruction;
- treating coordination narration as delivery proof; and
- descendants.

The researcher returns findings to the root. The root records that return
without expanding its claims or converting unknowns into findings.

### Executor

Mode: one-writer artifact production.

Opens only after the root accepts the researcher return.

Ownership:

- `pmot-01-decision-brief-and-executor-return-v0.1.md`

Required output:

- one concise brief comparing the three revised paths;
- exactly one recommendation or `HOLD`;
- exact evidence and unknowns;
- the proposed pilot use case;
- owner, dependency, first action, stop condition, and prohibited work; and
- measured preparation burden through candidate freeze.

The executor may not open new research lanes, change the question, self-verify,
post externally, or spawn descendants.

### Independent Verifier

Mode: detached read-only review.

Opens only after the root freezes the executor candidate at an exact Git SHA.

Required result:

- `accepted`;
- `held`;
- `rework`; or
- `rejected`.

The verifier checks:

- source support for the proposed live pilot;
- fair comparison of all three paths;
- repository-role separation;
- treatment of `UNKNOWN`;
- burden accounting;
- authority boundaries; and
- compliance with the frozen question and baseline.

The verifier may not edit or repair the candidate, contact other lanes, or spawn
descendants.

The verifier returns its result to the root. The root records the exact result
without changing its disposition or rationale.

### David Human Gate

David receives the verified brief and returns:

- `accept`;
- `hold`;
- `rework`; or
- `reject`.

Only David's response completes the decision-time measure. Verifier acceptance
does not substitute for David's decision.

## Serial Release Order

```text
authorization record
-> researcher
-> root evidence check
-> executor
-> root candidate freeze
-> independent verifier
-> David human disposition
```

These lanes are dependent. Do not run researcher, executor, and verifier in
parallel.

## Five-Artifact Execution Shape

The execution phase may create exactly these five listed artifacts:

| # | Artifact | Purpose | Writer |
|---:|---|---|---|
| 1 | `pmot-01-lane-contract-and-ledger-v0.1.md` | Exact task packets, release status, timestamps, and burden counters | Root |
| 2 | `pmot-01-researcher-return-v0.1.md` | Source-indexed facts, pilot candidate, dependencies, conflicts, and unknowns | Root records the read-only researcher return |
| 3 | `pmot-01-decision-brief-and-executor-return-v0.1.md` | Frozen decision brief and executor completion return | Executor |
| 4 | `pmot-01-independent-verifier-return-v0.1.md` | Detached review of the exact frozen candidate | Root records the read-only verifier return |
| 5 | `pmot-01-human-disposition-and-scoreboard-v0.1.md` | David's decision, prospective measures, baseline comparison, and final classification | Root records David's exact decision |

The existing `runs/2026-07-27/source-index.md` remains the routing ledger and may
be updated. It is excluded from the five listed execution artifacts because the
manual baseline's ten-artifact count also excluded its source index.

Pre-authorization planning and freeze records are outside the prospective
execution window. The artifact-burden clock begins when the researcher is
dispatched.

## Start and Stop

Test start: the recorded timestamp when the root dispatches the researcher.

Preparation stop: the recorded timestamp when the root freezes the executor
candidate.

Decision stop: David's recorded human disposition.

Stop and return `HOLD` if:

- the researcher cannot name an exact live pilot;
- required evidence is unavailable;
- a lane crosses repository or write boundaries;
- the executor changes the frozen question;
- the candidate cannot be frozen;
- the verifier is not independent; or
- the five-artifact limit would be exceeded.

## Current State

- Revised paths: frozen.
- Manual baseline: unchanged and controlling.
- Root, researcher, executor, and verifier lanes: authorized.
- Lane dispatch: not started.
- Experiment clock: not started.
- Slack and Linear writes: not authorized.
- Runtime, provider, automation, memory, skill, eval, PR, merge, and `main`
  actions: not authorized.
