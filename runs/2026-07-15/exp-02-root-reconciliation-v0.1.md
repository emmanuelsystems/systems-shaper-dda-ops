---
title: EXP-02 Root Reconciliation
asset_type: root_reconciliation
status: reconciled_ready_for_candidate_freeze
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
candidate_sha: assigned_by_commit_containing_this_reconciliation
---

# EXP-02 Root Reconciliation

## Scope

Reconcile the researcher return, executor candidate, executor return, frozen goal, and current proof boundaries into one exact candidate review set. This is root qualification for independent-review intake, not experiment acceptance.

## Specialist Returns

| Lane | Primary return | Corrections | Root disposition |
|---|---:|---:|---|
| Researcher | `1` | `0` | Qualified for executor dependency use |
| Executor | `1` | `1` | Qualified after encoding-only correction |

The executor correction replaced two mojibake sequences with ASCII `--`, refreshed hashes and metadata, and made no substantive or scope change.

## Contract Results Before Verification

| Measure | Root observation | Status |
|---|---|---|
| Goal stability | `0` unapproved changes | Pass pending verifier recomputation |
| Task traceability | `7/7` tasks linked to `EXP-02-PM2E-2026-07-15` | `100%` |
| Action completeness | `7/7` tasks contain owner, output, dependency, evidence, and gate | `100%` |
| Human redirection | `0` | Pass |
| Human clarification | `0` | Pass |
| Return-cycle burden | One primary return per specialist; one correction total | Pass at allowed maximum |
| Unauthorized external writes | `0` | Pass |
| Recovery burden | Artifact path designed; fresh timed recovery not yet measured | Pending verifier |
| Next-action correctness | No human decision yet | Pending human gate |

## Material-Claim Ledger

| Claim | Candidate statement | Anchor | Root result |
|---|---|---|---|
| C01 | Repo remains useful as durable evidence, not the value loop | E1 | Anchored |
| C02 | Direction is goal-centered orchestration, tracing, verification, and measurement | E2-E4 | Anchored |
| C03 | Selected post-meeting execution goal fits the frozen objective | E7, E9 | Anchored |
| C04 | Broad orchestration system is too broad for EXP-02 | E3, E5, E6, E9 | Anchored |
| C05 | Interface work remains held until measurement exists | E1, E4, E5, E9 | Anchored |
| C06 | Skill, agent, automation, and model-policy packaging is unsupported for this run | E5, E8, E9 | Anchored |
| C07 | Every task requires goal link and bounded return fields | E6, E7 | Anchored |
| C08 | Repeatable sequence follows intent through human decision | E2, E3, E6-E9 | Anchored |
| C09 | Goal stability observed as `0` | Executor return and intervention record | Anchored |
| C10 | Task traceability is `7/7` | Candidate task table and executor checks | Reproducible |
| C11 | Action completeness is `7/7` | Candidate task table and executor checks | Reproducible |
| C12 | Executor redirections and clarifications are `0` | Executor return | Anchored |
| C13 | Unauthorized external writes are `0` | Researcher and executor returns | Anchored |
| C14 | Manual numeric baseline remains unknown | E9 | Anchored |
| C15 | Candidate SHA and verifier result are pending before freeze | Candidate and verifier intake | Anchored |
| C16 | Human acceptance and promotion boundaries remain separate | Governance, E7, E8 | Anchored |

Root evidence coverage before verifier recomputation: `16/16`, or `100%`. This counts claim groups defined above and does not convert inherited external-source wording into independently verified fact.

## Conflicts Reconciled

- EXP-02 is independently authorized by the July 15 human record. It does not depend on or prove EXP-01 completion.
- Interface and scoreboard language is treated as future work because the same meeting packet requires measurement first.
- Slack, transcript, and Notion wording not directly opened by specialists remains inherited and explicitly limited.
- Unknown manual-baseline values remain `unknown`; no numeric improvement claim is made.

## Root Disposition

`qualified_for_candidate_freeze`

The exact candidate set may be committed on the current scoped branch and passed to the independent verifier at that commit SHA. Commit is transport and freeze evidence only; it is not acceptance.

## Remaining Holds

- Independent verification has not run.
- Recovery burden has not been timed by the verifier.
- No final scoreboard or human experiment decision exists.
- No external update is authorized.
- Skills, agents, automation, frontend, runtime, PR, `main`, infrastructure, canon, and repo replacement remain held.
