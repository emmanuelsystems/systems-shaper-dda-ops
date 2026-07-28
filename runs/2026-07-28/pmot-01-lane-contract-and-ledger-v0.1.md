---
title: PMOT-01 Lane Contract and Ledger
asset_type: experiment_lane_ledger
status: researcher_return_accepted_pilot_contract_requested_executor_not_released
version: v0.1
owner: David Abiera
created: 2026-07-28
branch: codex/david-pmot-01-research-return-20260728
parent_sha: 27048e4c0d7d03eb3028177e579c13d1bf6b6e8e
test_id: PMOT-01
manual_baseline_id: PMB-2026-07-23
test_start_local: 2026-07-28T01:08:00-0700
test_start_utc: 2026-07-28T08:08:00Z
artifact_number: 1
artifact_limit: 5
external_write_claim: slack_thread_reply_only
---

# PMOT-01 Lane Contract and Ledger

## Frozen Decision

The research lane must return exactly one recommended path:

- `PILOT_NOW`
- `RECOVER_THEN_PILOT`
- `COMPARE_THEN_PILOT`
- `HOLD`

The controlling standard is the shortest evidence-backed path to one real user
outcome without hiding a required safety or provenance dependency.

## Researcher Task Packet

```text
Role: read-only researcher. No descendants.

Objective:
Determine which already-authorized path is justified now:
PILOT_NOW, RECOVER_THEN_PILOT, COMPARE_THEN_PILOT, or HOLD.
Also determine whether Emmanuel has supplied the evidence needed for the
2026-07-28 end-of-day sign-off.

Evidence order:
1. Exact GitHub/repository objects.
2. Linear issue state and comments.
3. Slack coordination narrative.

Repository separation:
- systems-shaper-dda-ops is review/control evidence only.
- dda-agent-ops is pilot/use-case evidence.
Do not conflate them.

Required checks:
1. Identify the strongest exact bounded real-world pilot in dda-agent-ops, or
   return BLOCKED_UNKNOWN_USE_CASE.
2. Decide whether the missing historical-object pair needed by CTR-01 actually
   blocks that pilot.
3. Decide whether the missing SSI-120 comparison artifact actually blocks that
   pilot.
4. Identify anything Emmanuel supplied after or in 934fbd7.
5. Check whether the SSI-120 artifact, five unavailable objects, remote
   reachability, new pushes/logs, or Linear updates now exist.
6. Produce an end-of-day list: review now, request now, defer safely.
7. Give exact evidence handles: repository, branch, SHA, path, Linear
   ID/comment, Slack channel/message/thread timestamp.
8. Report source failures and unresolved unknowns.

Return shape:
- First line: RESEARCH_COMPLETE or RESEARCH_HELD.
- One recommended path only.
- Proven facts.
- Blocking unknowns.
- Evidence ledger.
- Sign-off verdict.
- Exact concise ask to Emmanuel.

Boundaries:
No edits, fetches, branch changes, staging, commits, pushes, Slack/Linear
messages, inferred object reconstruction, or acceptance claims. UNKNOWN blocks
only the dependent claim. A commit or verifier result does not equal human
acceptance.
```

## Release Ledger

| Lane | Release state | Timestamp | Result |
|---|---|---|---|
| Root authorization readback | complete | before dispatch | v0.2 contract and baseline read |
| Researcher | complete | `2026-07-28T01:08:00-0700` dispatch; `2026-07-28T01:11:24-0700` root readback | `PILOT_NOW` returned |
| Root evidence check | complete | `2026-07-28T01:11:24-0700` | return accepted as decision-brief input only |
| Emmanuel pilot-contract request | sent | Slack `1785227020.728379` | response pending; no execution authority created |
| Executor | held | — | opens only after root accepts researcher return |
| Candidate freeze | held | — | opens only after executor return |
| Independent verifier | held | — | opens only after exact candidate freeze |
| David human disposition | held | — | opens only after verifier return |

## Burden Ledger

| Measure | Current value |
|---|---:|
| Execution artifacts created | 2 of 5 |
| Source indexes created for this dated run | 1 |
| Specialist lanes dispatched | 1 |
| External writes | 1 Slack thread reply |
| Runtime actions | 0 |
| Human interventions after authorization | 0 |

The source index is excluded from the five-artifact execution count under the
frozen PMOT-01 contract.

## Proof Boundary

Dispatch acceptance proves only that the researcher route was accepted. It does
not prove tool access, research completion, path selection, model identity,
executor release, verifier acceptance, or David's disposition.

The completed researcher return is recorded in
`pmot-01-researcher-return-v0.1.md`. Root acceptance means only that the return
is sufficiently evidenced for use by the later decision-brief executor.
Executor release has not occurred.

## Root Interpretation Check

An initial interpretation would have returned `HOLD` because no fresh pilot run
was already authorized. That interpretation does not control. The frozen PMOT
question selects the shortest path toward a named next pilot; it does not make
the research lane the runtime authorization gate.

`PILOT_NOW` therefore controls because a bounded transcript-to-goal-packet use
case is exactly evidenced and neither CTR-01 nor SSI-120 is a dependency. Fresh
execution remains stopped by data-classification, scope-contract, burden, source
manifest, and explicit execution-authority gates.

The Slack request asks Emmanuel for the exact pilot owner, user outcome, source
manifest, first bounded action, stop condition, non-dependency confirmation,
and separate `934fbd7` verifier-request status. It explicitly prohibits starting
the pilot or adjacent held work from that message.
