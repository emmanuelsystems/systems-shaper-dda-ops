---
title: EXP-02 Independent Verifier Return
asset_type: verifier_return
status: rework
version: v0.1
owner: EXP-02 Independent Verifier
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
logical_task_id: EXP-02-VERIFY
candidate_sha: bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5
verifier_result_sha: assigned_by_commit_containing_this_return
---

# EXP-02 Independent Verifier Return

## 1. Task and Candidate Reference

- Task: `EXP-02-VERIFY`
- Goal: `EXP-02-PM2E-2026-07-15`
- Candidate SHA: `bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5`
- Candidate remained frozen: no `runs/2026-07-15/` drift during review.
- Manifest integrity: `12/12` listed hashes matched committed files.
- Start: `2026-07-15T10:38:10.0256429+08:00`
- End: `2026-07-15T10:41:21.0728305+08:00`
- Tool calls: `12`, including one failed read-only hash command and its retry.
- Verifier writes: `0`
- External connectors: `0`

## 2. Verdict and Scope

`rework`

Scope: decision-readiness only.

The candidate is structurally complete and within its proof boundary, but it fails the frozen goal-stability and evidence-coverage thresholds. This verdict does not address runtime readiness, infrastructure acceptance, canon, automation, skills, agents, PR approval, `main`, or replacement of `dda-agent-ops`.

## 3. Criteria Results

| Criterion | Result |
|---|---|
| Frozen SHA and manifest | Pass |
| Required candidate contents | Pass structurally |
| Task traceability | Pass |
| Action completeness | Pass |
| Evidence coverage | Fail |
| Proof-boundary evidence coverage | Pass |
| Goal stability | Fail |
| Human redirection | Pass from recorded evidence |
| Human clarification | Pass |
| Return-cycle burden | Pass at allowed maximum |
| Recovery burden | Pass |
| External-write compliance | Pass from available evidence |
| Conflicts and unknowns visible | Pass |
| Role separation and no executor self-acceptance | Pass |
| Next-action correctness | Pending human gate |

## 4. Recomputed Measures

| Measure | Recomputed result | Threshold | Result |
|---|---:|---:|---|
| Goal stability | `1` unapproved post-researcher goal change | `0` | Fail |
| Task traceability | `7/7`, `100%` | `100%` | Pass |
| Evidence coverage | `15/16`, `93.75%` | At least `95%` | Fail |
| Proof-boundary coverage | `100%` | `100%` | Pass |
| Action completeness | `7/7`, `100%` | `100%` | Pass |
| Human redirection | `0` recorded | `0` | Pass |
| Human clarification | `0` recorded | At most `1` | Pass |
| Return-cycle burden | Researcher `1`; executor `1`; corrections `1` | One primary each; at most one correction | Pass |
| Recovery burden | `190.994 ms`; `5` artifacts | At most 10 minutes and 5 artifacts | Pass |
| Unauthorized external writes | `0` recorded | `0` | Pass |
| Next-action correctness | Pending | Human decision | Pending |

## 5. Defects by Severity

### Major

1. The root-qualified researcher goal says:

   `Establish a repeatable ... an unsent progress update, and one explicit human decision.`

   The executor candidate changes this to:

   `Establish one repeatable ... an unsent progress update, a frozen verifier-ready candidate, and one explicit human decision.`

   The candidate then states the goal is unchanged. The executor contract prohibited changing the goal, and the frozen set contains no authorization for the addition.

2. Root claim `C03` treats the selected goal as fully anchored by E7 and E9, but E9 contains the earlier wording. Material-claim coverage is therefore `15/16`, not `16/16`.

### Minor

1. The executor describes a five-artifact recovery set by treating the researcher return and qualification as one packet. They are two physical artifacts. The verifier's independently measured five-file path passes, but the candidate wording is imprecise.

## 6. Recovery-Burden Result

- Start: `2026-07-15T10:39:56.8521653+08:00`
- End: `2026-07-15T10:39:57.0431590+08:00`
- Duration: `190.994 ms`
- Artifact count: `5`

Artifacts:

1. `source-index.md`
2. `exp-02-goal-and-measurement-contract-v0.1.md`
3. `exp-02-researcher-return-v0.1.md`
4. `exp-02-researcher-return-qualification-v0.1.md`
5. `exp-02-post-meeting-execution-candidate-v0.1.md`

Goal, lineage, candidate, and evidence were recovered within the threshold.

## 7. Evidence Gaps and Conflicts

- Notion, Tactiq, and Slack were not independently inspected; their claims remain inherited and limited.
- Numeric manual-baseline values remain `unknown`.
- External-write compliance is supported by frozen returns and no contradictory repo evidence; external systems were not checked.
- The July 14 open-status register and July 15 authorization conflict is surfaced and bounded to EXP-02.
- Pre-freeze `candidate_sha: pending` fields remain in candidate artifacts. The exact SHA was supplied externally, manifest hashes matched, and no drift occurred; this is not a moving-target blocker.

## 8. Proof Limitations

- Verification used only committed repo evidence and exact Git objects.
- Memory was not used as proof.
- No external source was opened.
- No candidate file was edited or repaired.
- `accepted` cannot be returned while goal stability and evidence coverage fail.
- Commit integrity does not establish human acceptance, validation, runtime readiness, infrastructure approval, or canon.

## 9. Required Rework or Next Human Decision

A new candidate iteration must:

1. Restore the exact root-qualified researcher goal, or record explicit authorization for a changed goal before executor use.
2. Correct the candidate's `unchanged` claim.
3. Recompute the material-claim ledger and evidence coverage.
4. Clarify physical artifact counting in the recovery snapshot.
5. Freeze a new manifest and send the exact new SHA to an independent verifier.

The next human decision is whether to authorize a bounded rework iteration.
