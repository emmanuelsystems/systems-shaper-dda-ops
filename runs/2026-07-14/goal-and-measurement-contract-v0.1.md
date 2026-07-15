---
title: Meeting-to-Goal Experiment Goal and Measurement Contract
asset_type: goal_measurement_contract
status: frozen_setup_review_only
version: v0.1
owner: Root Orchestrator
decision_owner: Emmanuel Olana
created: 2026-07-14
approval_status: approved_for_setup_not_dispatch
goal_id: M2G-2026-07-14-01
parent_goal: DDA goal-centered orchestration improvement
parent_sha: 8063e95081d640f53f78db9ef345ab03ad8441ca
candidate_sha: assigned_by_git_commit_containing_this_packet
runtime_claim: none
github_path: runs/2026-07-14/goal-and-measurement-contract-v0.1.md
---

# Meeting-to-Goal Experiment Goal and Measurement Contract

## Goal

Within one bounded review-only run, use one root orchestrator plus separate researcher, executor, and independent-verifier conversations to convert the July 14 meeting evidence into a frozen, source-backed decision packet that determines whether the minimum multi-conversation loop should advance, while requiring no human redirection of intermediate specialist work.

## Why This Goal

The meeting identified the missing value loop as goal definition, delegation, evidence tracing, independent verification, and measured improvement. A broader swarm or frontend would add burden before this minimum loop is proven.

## Decision Owner

Emmanuel Olana decides whether the experiment hypothesis is accepted, revised, held, or rejected. The root orchestrator may recommend a decision but may not make the human gate decision.

## Scope

Included after a separate dispatch authorization:

- one read-only researcher return;
- one bounded executor return;
- root-orchestrator reconciliation into one frozen candidate;
- one independent verifier result;
- one baseline comparison and decision-ready scoreboard.

Excluded:

- external writes;
- production frontend work;
- automation or runtime changes;
- memory, skill, or eval activation;
- PR or `main` promotion;
- repo replacement;
- infrastructure, canon, or runtime-readiness claims.

## Measurement Start and Stop

- Start: the root sends the first frozen specialist contract after human dispatch authorization.
- Stop: the independent verifier returns a scoped verdict and the root records the final scoreboard for human decision.
- Initial setup authorization and the final human decision are outside the human-intervention count.
- Each lane must record its start time, end time, source count, tool-call count when available, and number of return or correction cycles.
- Token or cost totals must be recorded only when exposed by the task environment; otherwise record `not_available` without estimation.

## Measures and Thresholds

| Measure | Method | Pass threshold |
|---|---|---|
| Goal stability | Count unapproved changes to this goal after first dispatch | `0` |
| Task traceability | Delegated tasks linked to `M2G-2026-07-14-01` divided by all delegated tasks | `100%` |
| Evidence coverage | Material claims with exact source or produced-evidence anchors divided by all material claims | At least `95%`; decision and proof-boundary claims must be `100%` |
| Human redirection | Count human messages that change or redirect intermediate specialist work | `0` |
| Human clarification | Count human clarifications required after dispatch, excluding final decision | At most `1`; a second clarification triggers hold |
| Active-time burden | Sum of recorded active lane time | At most `120 minutes` |
| Return-cycle burden | Primary returns plus requested correction cycles | One primary return per specialist and at most one correction cycle total |
| Recovery burden | Verifier time and artifact count needed to recover goal, task lineage, candidate, and evidence | At most `10 minutes` and `5` artifacts |
| Verifier decision readiness | Independent verdict against this contract | `accepted` for decision-readiness scope |
| Material improvement | Comparison with the researcher-established manual baseline | Better on at least `2` comparable measures, with no regression in proof-boundary compliance |
| Next-action correctness | Human decision on the root's recommended next action | Accepted without substantive rewrite |

## Quality Criteria

- The goal remains observable, bounded, and linked to a human decision.
- Direct evidence, inference, and unknowns remain separate.
- Conflicting sources are named rather than averaged.
- All lane returns use the required task and goal IDs.
- The executor does not self-accept.
- The verifier reviews a frozen candidate and does not modify it.
- Review-only, candidate, accepted, validated, and runtime-ready remain distinct.
- The final packet measures outcome and burden, not activity alone.

## Required Evidence

- Human decision record and frozen goal contract.
- Conversation-lane ledger with exact task IDs, status transitions, timestamps, and intervention log.
- Researcher source-to-claim map and manual-baseline table.
- Executor artifact manifest, checks, limitations, and burden record.
- Root reconciliation with conflicts and unresolved holds.
- Frozen candidate artifact manifest and exact candidate SHA when committed.
- Independent verifier verdict with defects and proof limitations.
- Final baseline comparison, scoreboard, and human decision record.

## Success

The experiment passes only when every threshold above is satisfied, the verifier accepts the frozen packet for decision-readiness scope, and the result shows material improvement over the recorded manual baseline without weakening human acceptance or proof boundaries.

## Failure

The experiment fails when the completed run misses a pass threshold, requires human redirection, produces an untraceable material claim, allows self-verification, or reports activity without a decision-ready outcome.

## Hold

Hold rather than fail when a required source is missing, evidence conflicts cannot be resolved within the contract, a metric cannot be measured, the candidate is moving, permissions are insufficient, or a human-owned decision is required.

## Escalation

Escalate to Emmanuel when:

- the goal, scope, threshold, or permission boundary must change;
- more than one post-dispatch human clarification is required;
- an external write or runtime action appears necessary;
- a source conflict changes the recommended decision;
- the executor cannot produce a frozen candidate from the allowed inputs;
- the verifier lacks independence or cannot recover the evidence;
- any promotion, acceptance, or repository-role decision is proposed.

## Current Gate

Stages 1-2 are authorized and complete at the contract level. Specialist dispatch and Stages 3-7 remain held.
