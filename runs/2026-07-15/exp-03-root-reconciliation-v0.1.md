---
title: EXP-03 Root Reconciliation
asset_type: root_reconciliation
status: qualified_for_candidate_freeze
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-03-DDA-IMPLEMENTATION-DECISION-2026-07-15
setup_sha: 17346a3707204566e228e2a621b67493483f5e4f
candidate_sha: assigned_by_commit_containing_this_reconciliation
---

# EXP-03 Root Reconciliation

## Disposition

`qualified_for_candidate_freeze`

The executor returned the required real outcome and evidence record in one primary return. The root's deterministic checks found all nine required decision-brief sections, seven complete implementation-sequence rows, thirteen material-claim rows, and all four human-decision states. No content correction was requested.

This qualification permits an exact local candidate commit and independent review. It does not accept the recommendation or close baseline observation 1.

## Goal and Output Check

The frozen goal is unchanged. The candidate's operational output is a decision brief, not a claim that completing EXP-03 paperwork is itself the result.

The brief recommends two additional manual, review-only, real-outcome goal cycles as baseline observations 2 and 3 before automation, frontend, permanent-agent, skill/eval, infrastructure, runtime, or improvement claims are considered. The recommendation is explicitly an executor inference pending verifier and human decisions.

## Deterministic Qualification Results

| Check | Root result |
|---|---|
| Required decision-brief sections | `9/9` |
| Implementation-sequence rows | `7/7` with owner, output, evidence, and gate columns |
| Material-claim rows | `13/13` |
| Claimed material-claim coverage | `100%`, pending verifier recomputation |
| Proof-boundary coverage | `100%`, pending verifier recomputation |
| Goal-to-task traceability | `100%` |
| Human decision states | `accept`, `revise`, `hold`, `reject` all present |
| Unapproved goal changes | `0` |
| External calls/writes | `0` recorded |
| Executor delegations | `0` |
| Post-return correction cycles | `0` |

## Prospective Timing Through Return

| Event | Timestamp (+08:00) | Elapsed from T0 |
|---|---|---:|
| T0 instrumentation | `2026-07-15T12:17:57.4045122+08:00` | `0.000 s` |
| Goal frozen | `2026-07-15T12:19:08.0141500+08:00` | `70.610 s` |
| First actionable task frozen | `2026-07-15T12:19:08.0141500+08:00` | `70.610 s` |
| Setup commit | `2026-07-15T12:20:20+08:00` | `142.595 s` |
| Executor dispatch | `2026-07-15T12:21:01.2452534+08:00` | `183.841 s` |
| Executor primary return visible | `2026-07-15T12:24:21.5571604+08:00` | `384.153 s` |

Earlier source-recovery/orientation time is excluded because T0 was the first deterministic EXP-03 timestamp. This limitation is preserved rather than backfilled.

## Burden and Intervention Reconciliation

| Measure | Root result |
|---|---:|
| Post-T0 human coordination minutes | `0` |
| Human clarifications | `0` |
| Human redirections | `0` |
| Root scheduling interventions | `1` |
| Executor primary returns | `1` |
| Post-return content correction cycles | `0` |
| Executor self-identified material defects | `0` |
| Executor pre-delivery tooling corrections | `1` quoting fix; no candidate change |

The executor classified two root messages as informational and reported zero scheduling interventions. The root ledger classifies the second message at `12:24:11.9575027+08:00` as one scheduling intervention because it was sent after no allowed output was visible and asked the lane to complete promptly. The more conservative root count controls the experiment scoreboard. The message changed no goal, source, output, or criterion.

## Dirty-Worktree Exclusion

The candidate freeze must include only named EXP-03 files and the updated July 15 source index. It must exclude pre-existing dirty `AGENTS.md`, all dirty/untracked `runs/2026-07-14/` files, and unrelated untracked current-truth-retrieval files that appeared under `runs/2026-07-15/` during execution.

## Remaining Gates

1. create and verify the exact candidate manifest;
2. commit only the scoped candidate set;
3. record candidate SHA and timestamp;
4. dispatch the independent verifier against that exact SHA;
5. recompute the scoreboard from the verifier result;
6. present Emmanuel with the final `accept`, `revise`, `hold`, or `reject` decision.

No improvement, repeatability, learning, validation, runtime, promotion, canon, or human-acceptance claim is supported at this gate.
