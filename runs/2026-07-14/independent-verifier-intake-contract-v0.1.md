---
title: Independent Verifier Future Intake Contract
asset_type: verifier_intake_contract
status: prepared_not_dispatchable
version: v0.1
owner: Root Orchestrator
decision_owner: Emmanuel Olana
created: 2026-07-14
task_id: 019f5f71-9415-7492-b328-658d75ba344a
goal_id: M2G-2026-07-14-01
parent_sha: 8063e95081d640f53f78db9ef345ab03ad8441ca
candidate_sha: pending_frozen_executor_candidate
github_path: runs/2026-07-14/independent-verifier-intake-contract-v0.1.md
---

# Independent Verifier Future Intake Contract

## Task and Scope

Task ID: `019f5f71-9415-7492-b328-658d75ba344a`

Parent goal: `M2G-2026-07-14-01`

Independently evaluate the future frozen experiment candidate for decision readiness, evidence quality, goal satisfaction, burden accuracy, and proof-boundary compliance. Do not evaluate infrastructure acceptance, runtime readiness, canon, or repo replacement.

## Activation Preconditions

The root must supply all of the following before dispatch:

- exact `candidate_sha`;
- frozen artifact manifest;
- goal and measurement contract;
- researcher return;
- executor candidate and executor return;
- root-orchestrator reconciliation;
- final intervention log;
- confirmation that the candidate will not move during review.

Without all inputs, return `held` and do not review a partial or moving candidate.

## Required Verification

- Recompute task traceability and evidence coverage.
- Test every pass threshold in the goal contract.
- Confirm the goal did not change without authorization.
- Confirm burden and intervention counts follow the frozen definitions.
- Recover the goal, task lineage, candidate, and evidence while measuring recovery time and artifact count.
- Inspect source conflicts, unknowns, and unresolved holds.
- Confirm researcher, executor, and verifier separation.
- Confirm the executor did not self-accept.
- Confirm candidate, accepted, validated, runtime-ready, and canon claims remain separate.
- Record defects by severity and cite exact artifact locations.

## Allowed Tools and Permissions

- Read-only inspection of the frozen local candidate and named evidence set.
- Deterministic local checks and calculations.
- No candidate edits.

## Prohibited Actions

- Editing the candidate or implementing a fix during verification.
- External reads/writes, commits, pushes, PRs, or task messaging.
- Reviewing a moving target or substituting memory for missing evidence.
- Expanding the verdict into infrastructure, runtime, canon, or repo-replacement acceptance.

## Verdict Set

Return exactly one scoped verdict:

- `accepted`: decision-ready for the stated experiment scope;
- `held`: required evidence or a human-owned decision is missing;
- `rework`: bounded defects can be corrected without changing the goal;
- `rejected`: the candidate fails the goal or violates a material boundary.

## Required Return Format

1. Task and Candidate Reference
2. Verdict and Scope
3. Criteria Results
4. Recomputed Measures
5. Defects by Severity
6. Recovery-Burden Result
7. Evidence Gaps and Conflicts
8. Proof Limitations
9. Required Rework or Next Human Decision

## Escalation

Escalate when the candidate SHA or manifest is absent, the candidate changes during review, the verifier is asked to implement, the evidence cannot be recovered, a threshold is ambiguous, or the requested verdict would exceed the review-only scope.

## Intake State

Prepared but not dispatchable. The candidate SHA, manifest, executor return, and root reconciliation do not yet exist.
