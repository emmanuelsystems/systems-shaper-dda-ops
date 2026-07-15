---
title: Frozen Executor Delegation Contract
asset_type: specialist_delegation_contract
status: frozen_not_dispatched
version: v0.1
owner: Root Orchestrator
decision_owner: Emmanuel Olana
created: 2026-07-14
task_id: 019f5f71-2819-7dd3-95ac-502b6f135921
goal_id: M2G-2026-07-14-01
parent_sha: 8063e95081d640f53f78db9ef345ab03ad8441ca
candidate_sha: assigned_by_git_commit_containing_this_packet
github_path: runs/2026-07-14/executor-delegation-contract-v0.1.md
---

# Frozen Executor Delegation Contract

## Task and Reason

Task ID: `019f5f71-2819-7dd3-95ac-502b6f135921`

Parent goal: `M2G-2026-07-14-01`

Create the bounded review-only candidate that converts the frozen goal, lane evidence, and root-qualified researcher baseline into a decision-ready experiment scoreboard. Root qualification means complete enough for dependency use; it is not human acceptance. This tests execution toward a measurable goal rather than adding a broad template system.

## Preconditions

- Separate human authorization to dispatch this contract.
- Researcher return received and qualified by the root as complete enough for dependency use.
- Root provides that exact qualified researcher return as a frozen input.
- No goal, measure, or permission change since contract freeze.

If any precondition is unmet, return `held` without editing files.

## Requested Output

Create only these files under `runs/2026-07-14/`:

1. `experiment-scoreboard-candidate-v0.1.md`
2. `executor-return-v0.1.md`

The scoreboard candidate must contain the goal outcome, task lineage, evidence coverage calculation, intervention count, time and burden record, baseline comparison, unresolved holds, proof boundary, and recommended human decision.

The executor return must contain the exact changed-artifact manifest, evidence used, checks performed, assumptions, uncertainty, defects, proof limitations, and recommended next action.

## Frozen Inputs

- `runs/2026-07-14/human-decision-record-experiment-setup-v0.1.md`
- `runs/2026-07-14/goal-and-measurement-contract-v0.1.md`
- `runs/2026-07-14/conversation-lane-ledger-v0.1.md`
- `runs/2026-07-14/source-index.md`
- `runs/2026-07-14/mta-analysis-v0.1.md`
- `runs/2026-07-14/codex-multi-conversation-structure-v0.1.md`
- `runs/2026-07-14/meeting-to-goal-experiment-contract-v0.1.md`
- Root-qualified researcher return supplied at dispatch.

## Allowed Tools and Permissions

- Read the frozen inputs inside this repository.
- Write only the two requested run artifacts.
- Run deterministic local consistency and diff checks.

## Prohibited Actions

- Editing `AGENTS.md`, governance docs, the source index, goal contract, lane ledger, or researcher return.
- External reads/writes, specialist messaging, commits, pushes, PRs, or `main` changes.
- Expanding scope, changing thresholds, or creating additional templates.
- Self-accepting the candidate or claiming validation, runtime readiness, infrastructure approval, canon, or repo replacement.
- Hiding unknown or unavailable measures.

## Acceptance Criteria

- Only the two requested files are changed by the executor.
- Every scoreboard field maps to the goal contract.
- Task lineage is explicit and uses the exact task and goal IDs.
- Material-claim and evidence-coverage calculations are reproducible.
- Baseline comparisons cite the root-qualified researcher return.
- Unknown or not-yet-measured values remain visible.
- Human interventions and burden follow the frozen definitions.
- The candidate remains review-only and makes no self-verdict.
- Local Markdown, link/path, status, and proof-boundary checks pass with no skipped check hidden.

## Return Format

Use these headings in `executor-return-v0.1.md`:

1. Task Reference
2. Work Completed
3. Changed Artifacts
4. Evidence Used
5. Checks Performed
6. Burden and Intervention Record
7. Assumptions and Uncertainty
8. Defects and Remaining Holds
9. Proof Limitations
10. Recommended Next Action

## Escalation

Stop and return `held` when a precondition is unmet, frozen inputs conflict, a required measure cannot be represented, an additional file or permission is required, or the requested candidate would imply an unsupported acceptance or runtime claim.

## Dispatch State

Frozen but not dispatched. Do not begin until the root receives separate human dispatch authorization and supplies the root-qualified researcher return.
