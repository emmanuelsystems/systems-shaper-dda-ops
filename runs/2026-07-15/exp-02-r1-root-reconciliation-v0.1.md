---
title: EXP-02-R1 Root Reconciliation
asset_type: root_reconciliation
status: reconciled_ready_for_candidate_freeze
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
iteration_id: EXP-02-R1
original_candidate_sha: bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5
candidate_sha: assigned_by_commit_containing_this_reconciliation
---

# EXP-02-R1 Root Reconciliation

## Scope

Reconcile the separately authorized R1 executor return against the original verifier defects, exact researcher-qualified goal, frozen measures, and proof boundaries. This record qualifies an R1 candidate for exact-SHA independent review. It does not change the original EXP-02 `rework` result or accept R1.

## Required-Repair Results

| Required repair | Root observation | Result |
|---|---|---|
| Restore exact selected goal | Candidate contains the researcher-qualified sentence verbatim and contains no altered variant | Pass |
| Correct false unchanged claim | Candidate states that the original drifted, received `rework`, and R1 restores the goal | Pass |
| Recompute material-claim coverage | `16/16`, `100%`, with explicit anchors | Pass pending verifier recomputation |
| Count physical recovery files | Five individually named Markdown files; no logical packet compression | Pass pending timed verifier recovery |
| Preserve original result | Original candidate, executor return, and verifier return show zero diff from `b4bbf9c` | Pass |
| Preserve task structure | `7/7` goal-linked rows with owner, output, dependency, evidence, and gate | Pass |

## R1 Burden and Interventions

| Measure | Observation | Boundary |
|---|---:|---|
| Primary R1 executor returns | `1` | Separate from original iteration |
| R1 content corrections | `0` | Pass |
| R1 executor instrumented time | `273.990 seconds` | Recorded, not compared to an unknown manual baseline |
| R1 executor tool calls | `9` | Recorded |
| Human redirections | `0` | Pass |
| Human clarifications | `0` | Pass |
| Root scheduling interventions | `1` stop/resume | Disclosed orchestration burden; no goal or content change |
| Unauthorized external writes | `0` recorded | Pass from available evidence |

The root intervention stopped a delayed lane after no files appeared, then resumed the same executor with a minimal mechanical instruction. It did not change the goal, frozen sources, required repairs, or allowed files. It is not counted as a user redirection, but it is preserved as orchestration burden.

## Material-Claim Ledger

| Claim | Candidate claim group | Anchor | Root result |
|---|---|---|---|
| C01 | Repo/evidence layer and goal-centered loop | E1-E4, E6-E9 | Anchored |
| C02 | External-source limitations | E9 | Anchored |
| C03 | Exact selected goal restored | E9, E11-E13 | Anchored |
| C04 | Original drift and `rework` preserved | E10-E12 | Anchored |
| C05 | Decision-readiness gates | E7, E12, E13 | Anchored |
| C06 | Failure conditions | E7, E13 | Anchored |
| C07 | Hold conditions | E7, E13 | Anchored |
| C08 | General orchestration system excluded | E3, E5, E6, E9, E12 | Anchored |
| C09 | Frontend/interface held | E1, E4, E5, E9, E12 | Anchored |
| C10 | Skill, permanent-agent, automation, and model-policy work held | E5, E9, E12, E13 | Anchored |
| C11 | Seven complete goal-linked tasks | Candidate section 4 and deterministic root check | Reproducible |
| C12 | Nine-step gated sequence | E2, E3, E6-E9 and candidate section 5 | Anchored |
| C13 | Five physical recovery files | Candidate section 7 | Reproducible |
| C14 | Numeric manual baseline remains unknown | E9 and candidate section 8 | Anchored |
| C15 | No external/runtime/promotion/acceptance claims | E7, E8, E12, E13 and candidate section 9 | Anchored |
| C16 | Next gate is freeze and independent review, not acceptance | E7, E11-E13 and candidate section 10 | Anchored |

Root evidence coverage before independent review: `16/16`, `100%`. Proof-boundary claim groups C04-C07, C10, C15, and C16: `7/7`, `100%`.

## Goal-Stability Accounting

- Original EXP-02: `1` unapproved change; historical fail remains unchanged.
- EXP-02-R1: `0` unapproved goal changes after the explicit R1 authorization and frozen executor contract.
- Restoring the exact qualified wording is the authorized repair, not a retroactive claim that the original candidate was stable.

## Root Disposition

`qualified_for_r1_candidate_freeze`

The exact R1 review set may be committed on the current scoped branch and given to the independent verifier. The resulting commit is the R1 `candidate_sha`. Commit is freeze/transport evidence only.

## Remaining Holds

Independent verification, timed fresh recovery, next-action correctness, and the final human decision remain pending. External writes, push, runtime, automation, skill/eval or permanent-agent promotion, frontend, PR, `main`, infrastructure, canon, validation, and repo replacement remain held.
