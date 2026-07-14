---
title: Codex Multi-Conversation Structure - July 14 MTA Interpretation
asset_type: architecture_candidate
status: proposed_review_only
version: v0.1
owner: Emmanuel Olana
created: 2026-07-14
approval_status: not_approved
parent_sha: ff94794298acdd5dd0812f4a0f380520f047768d
candidate_sha: assigned_by_git_commit_containing_this_packet
github_path: runs/2026-07-14/codex-multi-conversation-structure-v0.1.md
---

# Codex Multi-Conversation Structure

## Interpretation

David did not merely recommend creating more agents. He described an operating pattern in which one root orchestrator conversation receives Emmanuel's intent and coordinates separate bounded conversations.

The root orchestrator should plan, delegate, track, reconcile, and measure. Specialist conversations should research, execute, design, advise, or verify. Emmanuel should focus on intent, boundaries, evaluation criteria, and final acceptance rather than directing every intermediate prompt.

## Minimum First Structure

```text
DDA Root Orchestrator
|-- Researcher conversation
|-- Executor conversation
`-- Independent verifier conversation
```

This is the smallest useful test. A larger swarm would add coordination burden before the orchestration hypothesis is proven.

## Root Orchestrator Responsibilities

- Interpret human intent.
- Define or refine the goal.
- Establish success, failure, quality, time, and burden criteria.
- Create the plan.
- Decide which bounded work lanes are required.
- Send task contracts to specialist conversations.
- Track the status and evidence returned by every lane.
- Reconcile conflicts rather than averaging them.
- Route the frozen return to independent verification.
- Compare the result with the original goal and baseline.
- Maintain current truth, decisions, holds, and next action.
- Escalate decisions that remain human-owned.

## Specialist Conversation Responsibilities

### Researcher

- Gather named sources.
- Separate direct evidence from inference.
- Identify missing or conflicting evidence.
- Return a source-indexed research packet.
- Remain read-only unless explicitly authorized otherwise.

### Executor

- Perform the bounded implementation or artifact-generation task.
- Stay within the task contract and allowed tools.
- Return changed artifacts, checks, limitations, and remaining holds.
- Avoid self-acceptance.

### Independent Verifier

- Review the frozen executor return, not a moving target.
- Evaluate goal satisfaction and evidence quality.
- Record defects, burden, missing evidence, and proof limitations.
- Return accepted, held, rework, or rejected for the stated scope.
- Avoid implementation changes during the verification pass.

## Optional Later Roles

- Advisor: critiques the plan and strategic assumptions.
- Designer: explores interface and workflow form.
- Workflow builder: converts a proven loop into a repeatable SOP.
- Template builder: packages stable return structures.
- Routine worker: performs lower-risk repeatable execution.
- Deep worker: performs high-consequence analysis or review.

These remain examples, not an approved permanent taxonomy.

## Delegation Contract

Every task sent by the orchestrator should include:

- goal ID and parent goal;
- reason the task exists;
- requested output;
- source set;
- allowed tools and permissions;
- prohibited actions;
- acceptance criteria;
- required evidence;
- return format;
- decision owner;
- escalation condition.

## Return Contract

Every specialist return should include:

- task and parent-goal reference;
- work completed;
- evidence used or produced;
- checks performed;
- assumptions and uncertainty;
- defects or unresolved questions;
- proof limitations;
- recommended next action.

## V-Loop Rhythm

```text
Human intent
-> goal definition
-> plan
-> delegated specialist work
-> evidence return
-> independent verification
-> orchestrator reconciliation
-> human accept / hold / rework / reject
-> next iteration
```

## Required State

The orchestrator should maintain:

- conversation-lane ledger;
- current goal and goal history;
- goal-to-task lineage;
- delegation and return status;
- decision log;
- packet manifest;
- current-truth record;
- verifier findings;
- unresolved holds;
- next owner and action.

The dated run folder remains the durable evidence layer for this state. The orchestrator must actively use the evidence to direct the next action instead of treating the repo as a passive archive.

## Human Role

Emmanuel remains responsible for:

- stating intent;
- confirming the goal;
- setting permissions and boundaries;
- approving evaluation criteria;
- making final acceptance and promotion decisions.

The orchestrator and specialist conversations should handle more of the middle: decomposition, research, execution, trace maintenance, verification routing, reconciliation, and proposed next action.

## Model Allocation Boundary

David described using stronger reasoning capacity for orchestration and lighter configurations for bounded work. This is an efficiency principle to test.

No specific model name, tier, or permanent role assignment is approved by this document. Actual cost, quality, and reliability must be measured before policy is adopted.

## Success Condition

This structure is useful only if it coordinates multiple conversations toward one measurable goal, preserves traceability, detects defects through independent verification, reduces Emmanuel's manual intervention, and produces a better result than the current context-collection baseline.

## Hold

This is a review-only architecture candidate. It does not activate an orchestrator, create agents, change runtime permissions, approve automation, or accept infrastructure.
