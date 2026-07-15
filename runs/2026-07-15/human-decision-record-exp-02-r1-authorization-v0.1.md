---
title: EXP-02-R1 Bounded Rework Authorization
asset_type: human_decision_record
status: approved_for_bounded_rework
version: v0.1
owner: Emmanuel Olana
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
iteration_id: EXP-02-R1
original_candidate_sha: bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5
original_verifier_result_sha: b4bbf9cac7e71c08f3802edf0770f61ebbfa3aa1
candidate_sha: pending
---

# EXP-02-R1 Bounded Rework Authorization

## Human Decision

On 2026-07-15, Emmanuel instructed: `Approve rework and run EXP-02-R1`.

This authorizes a separately identified rework iteration. It does not revise the original EXP-02 result, which remains `rework` at candidate `bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5`.

## Authorized Repairs

1. Restore the selected implementation goal exactly as qualified from the researcher return:

   > Establish a repeatable, review-only post-meeting-to-execution sequence that converts source-backed meeting direction into one measurable implementation goal, complete owner-tagged tasks, an unsent progress update, and one explicit human decision.

2. Replace the false claim that the altered goal was unchanged with a truthful R1 lineage statement.
3. Recompute the material-claim ledger and evidence coverage against the repaired candidate.
4. Describe recovery burden using physical files, not logical packets.
5. Freeze a new R1 candidate commit and run an independent read-only verifier against that exact SHA.

## Execution Boundary

- Reuse the existing frozen source set, root-qualified researcher return, goal-and-measurement contract, and original verifier defect report.
- Use a bounded executor correction lane and an independent verifier lane. A new researcher run is unnecessary because the required correction and exact source wording are already known.
- Write only review-only R1 artifacts under `runs/2026-07-15/` and the dated source index required to route them.
- Run deterministic local checks and create scoped commits required to freeze the candidate and record the verifier result.
- Preserve all unrelated worktree changes.

## Held Scope

No external write, push, runtime action, automation activation, skill/eval promotion, permanent-agent promotion, frontend work, PR, `main` promotion, infrastructure acceptance, canon claim, or replacement of `dda-agent-ops` is authorized.

## Human Gate

The root may reconcile specialist returns and recommend a result. Emmanuel retains the final `accept`, `revise`, `hold`, or `reject` decision for EXP-02-R1.
