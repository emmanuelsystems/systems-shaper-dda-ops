---
title: EXP-02 Goal and Measurement Contract
asset_type: goal_measurement_contract
status: frozen_for_execution
version: v0.1
owner: Root Orchestrator
decision_owner: Emmanuel Olana
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
parent_sha: 8063e95081d640f53f78db9ef345ab03ad8441ca
candidate_sha: pending
---

# EXP-02 Goal and Measurement Contract

## Goal

Within one bounded review-only run, convert the July 14 meeting evidence into a decision-ready post-meeting execution packet that identifies one highest-value implementation goal, maps every action to an owner, output, evidence requirement, and gate, drafts a source-backed progress update, and defines the next human decision without external writes or unsupported proof claims.

## Required Candidate Contents

1. Meeting direction and source anchors.
2. One selected implementation goal and rejection rationale for alternatives.
3. Owner-tagged execution tasks with outputs, dependencies, evidence, and gates.
4. A repeatable post-meeting-to-execution sequence.
5. A progress-update draft for David that is not sent.
6. Risks, conflicts, unknowns, and explicit proof boundary.
7. One recommended next human decision.

## Measures and Thresholds

| Measure | Method | Pass threshold |
|---|---|---|
| Goal stability | Count unapproved changes after researcher dispatch | `0` |
| Task traceability | Tasks linked to the goal divided by all proposed tasks | `100%` |
| Evidence coverage | Material claims with exact source anchors divided by all material claims | At least `95%`; proof-boundary claims `100%` |
| Action completeness | Tasks containing owner, output, dependency, evidence, and gate | `100%` |
| Human redirection | Post-dispatch user messages that redirect specialist work | `0` |
| Human clarification | Required post-dispatch clarifications | At most `1` |
| Return-cycle burden | Specialist primary returns and corrections | One primary return per specialist; at most one correction total |
| Recovery burden | Time and artifact count needed to recover goal, lineage, candidate, and evidence | At most `10 minutes` and `5` artifacts |
| External-write compliance | Unauthorized external writes | `0` |
| Next-action correctness | Human decision on recommended next action | Pending final human gate |

## Success

The run is decision-ready only when the executor produces the required candidate, the root reconciles it into a frozen review set, the independent verifier returns `accepted` for decision-readiness scope, all measurable thresholds pass, and no proof boundary is weakened.

## Hold

Hold when a frozen source is unavailable, a required measure cannot be supported, source conflict changes the goal, the candidate is moving, verifier independence is compromised, or a human-owned decision is required.

## Failure

Fail when the goal drifts without authorization, material claims are untraceable, the executor self-accepts, required action fields are missing, or external/runtime actions occur outside scope.

## Final Human Gate

Emmanuel decides `accept`, `revise`, `hold`, or `reject`. A positive experiment decision does not create runtime, automation, skill, infrastructure, or canon approval.
