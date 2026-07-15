---
title: EXP-02-R1 Independent Verifier Intake
asset_type: verifier_contract
status: frozen_held_for_candidate_sha
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
iteration_id: EXP-02-R1
logical_task_id: EXP-02-R1-VERIFY
candidate_sha: supplied_at_dispatch
---

# EXP-02-R1 Independent Verifier Intake

## Task

Review the exact R1 candidate commit supplied by the root. Work read-only from committed Git objects. Do not edit or repair the candidate and do not review a moving working tree.

## Required Inputs

- Exact R1 `candidate_sha` supplied at dispatch.
- `exp-02-r1-candidate-manifest-v0.1.md` at that SHA.
- Original candidate `bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5` and original verifier-result commit `b4bbf9cac7e71c08f3802edf0770f61ebbfa3aa1`.
- R1 authorization, executor contract, candidate, executor return, root reconciliation, goal contract, researcher return, and researcher qualification at the supplied SHA.

## Verification Criteria

1. Confirm the supplied SHA exists, the manifest hashes match committed blobs, and the candidate remains frozen.
2. Compare the selected goal byte-for-byte with the exact root-qualified researcher wording.
3. Confirm R1 truthfully preserves the original drift and `rework` result rather than relabeling history.
4. Recompute R1 goal stability. Distinguish original EXP-02's historical `1` change from R1's post-authorization changes.
5. Recompute task traceability and action completeness from the seven task rows.
6. Recompute material-claim and proof-boundary evidence coverage from the explicit ledger and source anchors.
7. Confirm recovery counting uses five physical files. Time a fresh recovery of goal, lineage, candidate, and evidence from those exact files.
8. Reconcile the disclosed root scheduling intervention, executor return burden, clarifications, corrections, and unauthorized external-write evidence.
9. Confirm source limitations, unknown baselines, unsent-update status, role separation, and all proof/non-promotion boundaries.
10. Return exactly one scoped decision-readiness verdict: `accepted`, `held`, `rework`, or `rejected`.

## Thresholds

| Measure | Threshold |
|---|---|
| R1 goal stability | `0` unapproved post-R1-authorization changes |
| Task traceability | `100%` |
| Evidence coverage | At least `95%`; proof-boundary coverage `100%` |
| Action completeness | `100%` |
| Human redirection | `0` |
| Human clarification | At most `1` |
| R1 return-cycle burden | One primary executor return; at most one R1 content correction |
| Recovery burden | At most `10 minutes` and `5` physical files |
| Unauthorized external writes | `0` |
| Next-action correctness | Pending final human gate |

The one disclosed root scheduling stop/resume is measured separately. It is not a goal change or human redirection, but the verifier must report it as orchestration burden.

## Return Shape

Return task/candidate reference, timing and tool calls, exact verdict/scope, criteria table, recomputed measures, defects by severity, recovery result with physical file list, evidence gaps/conflicts, proof limitations, and required next human decision. Make no repository or external writes.

## Proof Boundary

An `accepted` verifier verdict would mean only that the frozen R1 packet passes the stated decision-readiness criteria. It would not accept the original candidate, validate runtime behavior, approve automation, skills, agents, frontend, infrastructure, canon, PR, `main`, external posting, or replacement of `dda-agent-ops`. Emmanuel remains the final R1 decision owner.
