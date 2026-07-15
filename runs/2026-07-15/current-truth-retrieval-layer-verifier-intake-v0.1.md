---
title: DDA Current Truth and Artifact Retrieval Layer Verifier Intake
asset_type: verifier_contract
status: draft_held_for_candidate_sha
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: CTR-01
logical_task_id: CTR-01-VERIFY
candidate_sha: supplied_at_dispatch
approval_status: not_approved
---

# DDA Current Truth and Artifact Retrieval Layer Verifier Intake

## Task

Independently review the exact committed CTR-01 candidate supplied at dispatch. Read committed Git objects only. Do not edit or repair the candidate, inspect a moving worktree as evidence, write externally, or implement the proposed `current/` layer.

## Required Inputs

- Exact `candidate_sha` supplied at dispatch, frozen on a scoped branch whose candidate parent is `66f52f5f31dcb370645a52795ea9f6ec220b866c` so concurrent EXP-03 history is not part of this candidate lineage.
- `current-truth-retrieval-candidate-manifest-v0.1.md` at that SHA.
- The six candidate packet files named by the manifest.
- The governing and real-data source files named in `current-truth-retrieval-source-index-v0.1.md`.

## Verification Questions

1. Is the three-surface topology the minimum that answers the required queries?
2. Are current truth, artifact identity/lineage, recovery bundles, and canon-promotion authority structurally separate?
3. Can every required field be populated from real EXP-02-R1 evidence without guessing or scope inflation?
4. Do the fixture rows preserve original EXP-02 `rework`, R1 `accepted` decision-readiness, and the later human scope exactly?
5. Are `evidence_sha`, `reviewed_sha`, review status, review scope, lineage, and supersession unambiguous?
6. Does each recovery bundle use no more than five individually counted physical primary files?
7. Can a fresh reviewer recover goal, owner, decision, holds, next action, lineage, and reviewed SHA within ten minutes and without extra search?
8. Can a material update be represented without editing any earlier run artifact and by touching no more than three projection files?
9. Do deterministic rules detect missing fields, conflicts, impossible status/SHA combinations, supersession cycles, multiple next owners, and bundle overflow?
10. Does the design keep frontend, automation, runtime, canon, infrastructure, external writes, and promotion held?

## Thresholds

| Measure | Threshold |
|---|---:|
| Required query coverage | `6/6` |
| Required field population on fixture | `100%`, allowing only explicit `not_yet_frozen`, `not_reviewed`, or `not_applicable` |
| Incorrect authority or scope upgrades | `0` |
| Original-versus-R1 lineage errors | `0` |
| Recovery time | `<= 600 seconds` per bundle |
| Primary physical files opened | `<= 5` per bundle |
| Extra searches for the bounded answer | `0` |
| Material unresolved conflicts without owner/reference | `0` |
| History files modified by proposed update protocol | `0` |
| Projection files touched per ordinary material update | `<= 3` |
| Unauthorized actions or promotion claims | `0` |

Update elapsed time has no pass threshold yet. It must be observed over the first three real manual updates before an improvement claim or automation decision.

## Required Test Scenarios

1. Recover current CTR-01 status from `RB-CTR-01-V0.1`.
2. Recover EXP-02/R1 outcome and lineage from `RB-EXP-02-R1-V0.1`.
3. Simulate, without editing files, a later `rework` decision for CTR-01 and name exactly which projection rows/files would change.
4. Simulate an equal-authority conflict and confirm the outcome is `held_conflict`, not a merged value.
5. Simulate a superseding artifact and confirm the predecessor's historical review status stays unchanged.
6. Confirm absence of explicit canon or runtime approval yields a hold, regardless of accepted decision-readiness.

## Verdict Vocabulary

Return exactly one result for design sufficiency: `accepted`, `held`, `rework`, or `rejected`.

An `accepted` result means only that the frozen fields and retrieval model are sufficient for a later manual review-only implementation. It does not authorize that implementation.

## Return Shape

Return: exact candidate SHA, manifest integrity result, timing and physical-file count for both bundles, criteria table, scenario results, field omissions, ambiguity defects by severity, burden observations, verdict and scope, proof limitations, next owner, and next action.

## Independence and Proof Boundary

The verifier makes no candidate edits and no external writes. Frontend, automation, runtime activation, live current-state files, skill/eval or permanent-agent promotion, infrastructure, canon, PR, `main`, push, repo replacement, and operational-improvement claims remain held. Emmanuel remains the human decision owner after verification.
