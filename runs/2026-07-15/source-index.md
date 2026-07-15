---
title: July 15 DDA Experiment Source Index
asset_type: run_artifact
status: exp_03_verifier_accepted_human_gate_pending_ctr_01_frozen
version: v0.1
owner: Emmanuel Olana
created: 2026-07-15
approval_status: r1_accepted_target_authorized_for_bounded_design
parent_sha: 8063e95081d640f53f78db9ef345ab03ad8441ca
candidate_sha: bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5
r1_candidate_sha: 7437f21e0a5461ee559196f36f145cae41b4caa2
exp_03_setup_sha: 17346a3707204566e228e2a621b67493483f5e4f
exp_03_candidate_sha: 763ef60c3923cb2dbfaa7ed94f068bcfaf1b531a
exp_03_verifier_result_sha: 2e80b24c6fb0609a940209a8cfb42a96e9030da7
ctr_01_candidate_sha: b472bd1d65b064c32fe22b44b2fe504f9e18be8a
runtime_claim: none
automation_claim: none
skill_claim: none
external_write_claim: github_transport_only
github_push_claim: transport_only
github_path: runs/2026-07-15/source-index.md
---

# July 15 DDA Experiment Source Index

## Purpose

Record the July 15 EXP-02/EXP-02-R1 calibration sequence, the accepted working optimization target, and EXP-03 baseline observation 1 as separate bounded review-only cycles with exact proof boundaries.

EXP-02 is independent of EXP-01 completion. It does not imply that EXP-01 passed.

The original EXP-02 candidate at `bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5` received a `rework` verdict. EXP-02-R1 is a separately authorized correction iteration. It preserves that original result and repairs only the exact goal-lineage, evidence-ledger, and physical-file counting defects identified by the verifier.

## Frozen Source Set

| Source | Use | Authority / limitation |
|---|---|---|
| `README.md` | Repository role and non-claims | Current governance |
| `docs/source-of-truth.md` | Durable-truth rules | Current governance |
| `docs/source-authority-ladder.md` | Evidence authority and conflict handling | Current governance |
| Commit `8063e95081d640f53f78db9ef345ab03ad8441ca` | Frozen July 14 meeting-analysis packet | Committed candidate evidence; not acceptance |
| `runs/2026-07-14/mta-analysis-v0.1.md` at `8063e95` | Meeting direction, risks, measures, and research framing | Primary repo-local analysis source |
| `runs/2026-07-14/next-action-items-v0.1.md` at `8063e95` | Candidate actions and held research inputs | Proposed, not approved |
| `runs/2026-07-14/codex-multi-conversation-structure-v0.1.md` at `8063e95` | Root, researcher, executor, and verifier pattern | Proposed architecture evidence |
| [Notion MTA](https://app.notion.com/p/39d2570090e58139876fc6aa5fcefd38) | Supporting human-readable meeting analysis | Supporting planning surface |
| [Raw Tactiq transcript](https://app.tactiq.io/api/2/u/m/r/4IR6QuNBnAdUdoUt2Zhe?o=sl) | Primary meeting transcript | External source; transcription limitations apply |
| [David post-meeting Slack thread](https://systemsshaperinc.slack.com/archives/D0664PLU01Z/p1784008204828259) | Direction to standardize post-meeting notes and focus on what to implement next, where to start, and how to approach the loop | Coordination evidence only |
| `human-decision-record-exp-02-authorization-v0.1.md` | Current authorization and scope | Current human instruction captured for this run |
| `exp-02-verifier-return-v0.1.md` at result commit `b4bbf9cac7e71c08f3802edf0770f61ebbfa3aa1` | Exact original defects and required rework | Independent decision-readiness verifier result; original verdict remains `rework` |
| `human-decision-record-exp-02-r1-authorization-v0.1.md` | Authorization to run a separately identified R1 correction | Current human instruction; does not approve final R1 acceptance or promotion |

## Conflict Rule

The July 14 action register describes many setup actions as open, while later local EXP-01 artifacts describe partial completion. EXP-02 does not resolve that conflict or use EXP-01 as proof. It uses the committed July 14 meeting packet and the current human authorization as its frozen base.

## Original EXP-02 Artifact Set

| Artifact | Role |
|---|---|
| `human-decision-record-exp-02-authorization-v0.1.md` | Bounded human authorization |
| `exp-02-goal-and-measurement-contract-v0.1.md` | Frozen goal, measures, and gates |
| `exp-02-lane-ledger-v0.1.md` | Lane state and intervention trace |
| `exp-02-researcher-contract-v0.1.md` | Frozen researcher task |
| `exp-02-researcher-return-v0.1.md` | Research evidence return |
| `exp-02-researcher-return-qualification-v0.1.md` | Root dependency qualification |
| `exp-02-executor-contract-v0.1.md` | Frozen executor task |
| `exp-02-post-meeting-execution-candidate-v0.1.md` | Execution candidate |
| `exp-02-executor-return-v0.1.md` | Executor completion and burden record |
| `exp-02-root-reconciliation-v0.1.md` | Root claim ledger and candidate qualification |
| `exp-02-verifier-intake-v0.1.md` | Frozen verifier contract |
| `exp-02-candidate-manifest-v0.1.md` | Exact candidate file and hash manifest |
| `exp-02-verifier-return-v0.1.md` | Independent `rework` verdict at candidate `bc4b4cc` |
| `exp-02-final-scoreboard-v0.1.md` | Recomputed measures and decision logic |
| `exp-02-human-decision-record-v0.1.md` | Pending final human gate |

## EXP-02-R1 Artifact Set

| Artifact | Role |
|---|---|
| `human-decision-record-exp-02-r1-authorization-v0.1.md` | Bounded human R1 authorization |
| `exp-02-r1-executor-contract-v0.1.md` | Frozen correction task |
| `exp-02-r1-lane-ledger-v0.1.md` | R1 lane state and iteration accounting |
| `exp-02-r1-post-meeting-execution-candidate-v0.1.md` | Separately identified repaired candidate |
| `exp-02-r1-executor-return-v0.1.md` | R1 executor evidence and burden return |
| `exp-02-r1-root-reconciliation-v0.1.md` | R1 claim ledger and candidate qualification |
| `exp-02-r1-verifier-intake-v0.1.md` | Exact-SHA, read-only verifier contract |
| `exp-02-r1-candidate-manifest-v0.1.md` | R1 candidate file and hash manifest |
| `exp-02-r1-verifier-return-v0.1.md` | Independent R1 verdict |
| `exp-02-r1-final-scoreboard-v0.1.md` | R1 recomputed measures and decision logic |
| `exp-02-r1-human-decision-record-v0.1.md` | Human acceptance of bounded R1 decision-readiness |
| `human-decision-record-dda-optimization-target-v0.1.md` | Human instruction authorizing the working target definition |
| `dda-optimization-target-v0.1.md` | Working DDA optimization target and measurement model |

R1 candidate `7437f21e0a5461ee559196f36f145cae41b4caa2` received an independent `accepted` verdict for decision-readiness only. Emmanuel then accepted that bounded R1 result. Every promotion, external-write, canon, and runtime decision remains held.

## Current Working Optimization Target

The DDA now has a human-directed working target for bounded experiment design: maximize first-pass delivery of human-approved, independently verified, human-accepted goal outcomes while reducing time-to-outcome and human coordination burden, under zero permission or proof-boundary breaches.

The full metric definitions, eligibility rule, improvement rule, decision rights, and trace requirements are in `dda-optimization-target-v0.1.md`.

## EXP-03 Baseline Observation 1 of 3

EXP-03 is the first prospective real-outcome cycle under the working optimization target. Its operational goal is to produce a review-ready implementation decision brief for Emmanuel and David that states what to implement next, where to start, how the bounded loop should run, and what remains held.

The decision brief is the outcome. The remaining EXP-03 files are instrumentation and review evidence.

| Artifact | Role |
|---|---|
| `exp-03-human-authorization-v0.1.md` | Human authorization and held boundary |
| `exp-03-goal-and-measurement-contract-v0.1.md` | Frozen observable goal, permissions, evidence rule, success/failure/hold conditions, and prospective measures |
| `exp-03-executor-contract-v0.1.md` | First actionable delegated task |
| `exp-03-independent-verifier-intake-v0.1.md` | Prepared read-only verifier criteria; not dispatchable before candidate freeze |
| `exp-03-lane-ledger-v0.1.md` | Prospective timestamps, lane state, coordination, interventions, corrections, and defects |
| `exp-03-dda-implementation-decision-brief-v0.1.md` | Real operational outcome: review-ready implementation decision brief |
| `exp-03-executor-return-v0.1.md` | Executor evidence, timing, burden, and limitation record |
| `exp-03-root-reconciliation-v0.1.md` | Root qualification, conflict resolution, and candidate-freeze decision |
| `exp-03-candidate-manifest-v0.1.md` | Exact candidate file and hash manifest |
| `exp-03-verifier-return-v0.1.md` | Independent exact-SHA verifier result |
| `exp-03-final-scoreboard-v0.1.md` | Baseline observation 1 measures and open-cycle decision logic |
| `exp-03-human-decision-record-v0.1.md` | Pending final human `accept`, `revise`, `hold`, or `reject` gate |

Candidate `763ef60c3923cb2dbfaa7ed94f068bcfaf1b531a` received an independent `accepted` verdict for decision-readiness only. The final human decision remains pending, so baseline observation 1 is open and no improvement claim is supported.

## CTR-01 Current-Truth Retrieval Candidate

CTR-01 is a separate design-only candidate for a minimum current-truth index, artifact registry, and bounded recovery bundles above immutable dated-run evidence.

Its seven-file packet was frozen on branch `codex/current-truth-retrieval-20260715` at candidate `b472bd1d65b064c32fe22b44b2fe504f9e18be8a`, whose parent is accepted-target commit `66f52f5f31dcb370645a52795ea9f6ec220b866c`. EXP-03 history is intentionally excluded from the CTR-01 candidate lineage.

CTR-01 is ready for exact-SHA independent review. It is not accepted, implemented, validated, runtime-ready, or authorized for a live `current/` projection.

## EOD Reporting Artifact

| Artifact | Role |
|---|---|
| `eod-progress-report-v0.1.md` | First-person July 15 experiment report, David-meeting alignment, review links, current holds, and next gates |
| `human-decision-record-eod-report-and-push-v0.1.md` | Current authorization for scoped commit and GitHub push transport only |

## Proof Boundary

No external write beyond the currently authorized GitHub transport, runtime action, automation activation, skill or eval promotion, PR, `main` promotion, infrastructure acceptance, repo replacement, validation, or canon claim is authorized.
