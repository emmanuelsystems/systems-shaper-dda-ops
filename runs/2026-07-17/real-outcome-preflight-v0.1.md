---
title: Monday Priority Plan Real-Outcome Preflight
asset_type: real_outcome_preflight
status: candidate_pending_david_review_and_emmanuel_launch_gate
version: v0.1
owner: Root Orchestrator
created: 2026-07-17
goal_id: REAL-OUTCOME-MONDAY-PRIORITY-PLAN-01
runtime_claim: none
external_write_claim: none
---

# Monday Priority Plan Real-Outcome Preflight

## Proposed Goal

Using a frozen, source-backed context set, produce a same-day Monday priority plan for David that identifies his top three outcomes, a single owner for each outcome, exact supporting evidence, and explicit stop conditions. David must be able to evaluate the plan without Emmanuel explaining the context live.

## Outcome Class

`real_operational_planning_outcome_candidate`

The plan is the unit of value. The source index, trace, verifier return, and metrics are supporting evidence only.

## Launch Gates

All must pass before execution:

1. David reviews this preflight and confirms that the requested planning outcome is useful.
2. Emmanuel explicitly authorizes launch and the frozen source set.
3. The detached completeness verifier returns no unresolved high-severity defect.
4. T0, measures, permissions, success/failure/hold conditions, and verifier criteria are frozen before delegation.

## Frozen Source Set at Launch

The root must record exact links, timestamps, or SHAs for:

- David's most recent priority and operating-direction messages;
- open or due work from the approved planning/task surface, if accessible;
- current repo decision and hold state from the latest dated source index;
- any source David explicitly requires.

Unavailable sources must be named. Missing priority authority or conflicting same-authority sources trigger `hold`; the root must not invent or average priorities.

## Minimum Lane Model

```text
Human authorization
-> Root orchestrator
-> At most one read-only source-recovery lane, only if needed
-> One bounded plan writer
-> Frozen candidate
-> Detached verifier
-> David decision
-> Emmanuel closeout
```

No child dispatch, dynamic dispatch, parallel writer, or self-verification is allowed.

## Required Plan Shape

For each of three outcomes:

| Field | Requirement |
|---|---|
| Outcome | Observable result, not an activity label |
| Owner | One accountable owner; unresolved ownership causes hold |
| Evidence | Exact source link, timestamp, file path, or SHA |
| First action | Smallest action that starts the outcome |
| Stop condition | Evidence-based condition to stop, hold, or escalate |
| Decision dependency | Named human decision or unavailable source, if any |

The plan must also state ordering rationale, conflicts, missing evidence, and what is deliberately not being started.

## Success, Failure, and Hold

### Success

- Exactly three outcomes are present.
- Each has one owner, exact evidence, and a stop condition.
- No material claim lacks an anchor.
- Detached verifier returns `accepted` for decision-readiness.
- David returns `accept` without requiring Emmanuel to reconstruct the context live.
- Unauthorized actions remain `0`.

### Failure

- The plan is activity-centered or meta-operational rather than outcome-centered.
- Priorities are guessed, conflicts are averaged, or sources are fabricated.
- David rejects the plan because the priorities are wrong or unusable.
- A prohibited write or permission breach occurs.

### Hold

- Priority authority is missing or conflicting.
- An owner cannot be named from evidence.
- A required source is inaccessible.
- The verifier finds an unresolved high-severity defect.
- David or Emmanuel has not passed the required gate.

## Measures

Record observed values only:

1. T0 to frozen goal.
2. T0 to first actionable task.
3. T0 to first frozen candidate.
4. T0 to detached verifier verdict.
5. T0 to David's decision, or censored elapsed time if open.
6. Active Emmanuel coordination minutes after T0.
7. David clarification requests.
8. Root scheduling interventions.
9. Writer correction cycles.
10. Verifier defects by severity.
11. Physical files and external sources opened.
12. Unauthorized external or runtime actions.

This single outcome cannot establish repeatability or improvement.

## Allowed Actions

- Read the launch-approved frozen sources.
- Create review-only artifacts in the authorized dated run folder.
- Freeze a scoped candidate commit when separately authorized.
- Perform detached read-only verification.

## Prohibited Actions

- Posting or updating Slack, Linear, Notion, Drive, or other external systems.
- CTR-01 correction or live current-state projection.
- Starting baseline observation 2 before EXP-03 classification is closed.
- Automation, runtime activation, memory write, skill/eval promotion, PR, merge, `main`, canon, or repo replacement.

## Decision Requested from David

Return `accept`, `revise`, `hold`, or `reject` for this preflight. If revising or rejecting, name the better real outcome and the exact evidence that makes it higher value.
