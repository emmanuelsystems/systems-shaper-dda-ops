---
title: EXP-03 Independent Verifier Intake
asset_type: verifier_intake
status: prepared_not_dispatchable_until_candidate_freeze
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-03-DDA-IMPLEMENTATION-DECISION-2026-07-15
logical_task_id: EXP-03-VERIFY
candidate_sha: pending
---

# EXP-03 Independent Verifier Intake

## Review Rule

Review only the exact candidate commit supplied by the root. Confirm the candidate manifest and file hashes before substantive review. Do not use or edit moving worktree files and do not repair the candidate.

## Required Checks

1. exact candidate SHA and manifest integrity;
2. exact observable-goal stability;
3. required decision-brief contents;
4. recommendation is operational and non-meta;
5. implementation-step owner/output/evidence/gate completeness;
6. material-claim evidence coverage of at least `95%`;
7. proof-boundary coverage of `100%`;
8. goal/task traceability and required fields at `100%`;
9. instrumentation and burden-field completeness;
10. dirty-worktree exclusion and unauthorized action count;
11. conflicts, unknowns, risks, and non-claims;
12. correct baseline-only interpretation and final human gate.

## Verdicts

- `accepted`: first frozen candidate is decision-ready for Emmanuel's review within the stated scope;
- `rework`: correctable candidate defect prevents decision-readiness;
- `held`: evidence, freeze, independence, or human-owned input prevents a verdict;
- `rejected`: the candidate is materially incompatible with the frozen goal or boundary.

The verifier may not claim human acceptance, validation, runtime readiness, learning, improvement, canon, or promotion.
