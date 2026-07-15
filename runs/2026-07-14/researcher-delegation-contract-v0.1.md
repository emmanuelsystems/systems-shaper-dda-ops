---
title: Frozen Researcher Delegation Contract
asset_type: specialist_delegation_contract
status: frozen_not_dispatched
version: v0.1
owner: Root Orchestrator
decision_owner: Emmanuel Olana
created: 2026-07-14
task_id: 019f5f73-0cbe-7843-89e1-aa2d53f0421e
goal_id: M2G-2026-07-14-01
parent_sha: 8063e95081d640f53f78db9ef345ab03ad8441ca
candidate_sha: assigned_by_git_commit_containing_this_packet
github_path: runs/2026-07-14/researcher-delegation-contract-v0.1.md
---

# Frozen Researcher Delegation Contract

## Task and Reason

Task ID: `019f5f73-0cbe-7843-89e1-aa2d53f0421e`

Parent goal: `M2G-2026-07-14-01`

Establish the evidence-backed manual baseline and source-to-claim map required to decide whether the minimum multi-conversation loop materially improves on the July 14 context-collection workflow.

## Requested Output

Return one concise Markdown research packet to the root orchestrator containing:

1. a baseline table for every comparable measure in the goal contract;
2. exact source anchors for each observed baseline value;
3. `unknown` where the named sources do not support a value;
4. a direct-evidence / inference / unknown separation;
5. source conflicts and their effect on the experiment;
6. a claim-evidence map for the future executor;
7. recorded start time, end time, source count, tool-call count when available, and correction-cycle count;
8. a recommended next action and remaining holds.

## Frozen Source Set

- `README.md`
- `docs/source-of-truth.md`
- `docs/source-authority-ladder.md`
- `runs/2026-07-14/source-index.md`
- `runs/2026-07-14/mta-analysis-v0.1.md`
- `runs/2026-07-14/codex-multi-conversation-structure-v0.1.md`
- `runs/2026-07-14/meeting-to-goal-experiment-contract-v0.1.md`
- `runs/2026-07-14/goal-and-measurement-contract-v0.1.md`

## Allowed Tools and Permissions

- Read-only local file inspection inside this repository.
- Deterministic text search and counting over the frozen source set.
- No repository writes.

## Prohibited Actions

- External browsing or external-system reads/writes.
- File edits, commits, pushes, PRs, or messages to another task.
- Expanding the source set without root authorization.
- Inventing baseline values or treating missing data as zero.
- Changing the goal, measures, thresholds, proof boundary, or repository role.
- Making acceptance, validation, runtime, infrastructure, or repo-replacement claims.

## Acceptance Criteria

- Every baseline value is anchored or marked `unknown`.
- Every comparable metric from the goal contract is addressed.
- Direct evidence and inference are visibly separate.
- Conflicts are named rather than averaged.
- The return uses the exact task ID and parent goal ID.
- The return contains no implementation or self-acceptance claim.
- Burden and human-intervention observations are recorded using the goal contract definitions.

## Return Format

Use these headings exactly:

1. Task Reference
2. Work Completed
3. Baseline Table
4. Claim-Evidence Map
5. Conflicts and Unknowns
6. Checks Performed
7. Burden and Intervention Record
8. Proof Limitations
9. Recommended Next Action

## Escalation

Stop and return `held` when a required source is missing, a source conflict changes the baseline materially, a metric cannot be interpreted using the frozen contract, or any external source or permission appears necessary.

## Dispatch State

Frozen but not dispatched. Do not begin until the root receives separate human dispatch authorization.
