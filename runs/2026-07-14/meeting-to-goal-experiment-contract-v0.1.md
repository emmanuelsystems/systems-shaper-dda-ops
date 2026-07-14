---
title: Meeting-to-Goal Orchestration Experiment Contract
asset_type: experiment_contract
status: proposed_review_only
version: v0.1
owner: Emmanuel Olana
created: 2026-07-14
approval_status: not_approved
parent_sha: ff94794298acdd5dd0812f4a0f380520f047768d
candidate_sha: assigned_by_git_commit_containing_this_packet
runtime_claim: none
github_path: runs/2026-07-14/meeting-to-goal-experiment-contract-v0.1.md
---

# Meeting-to-Goal Orchestration Experiment Contract

## Status

Proposed and review-only. Human approval is required before execution.

## Source Input

- July 14 David / Emmanuel meeting transcript.
- July 14 MTA analysis.
- Current repo governance and review-only boundaries.
- Repo state at parent SHA `ff94794298acdd5dd0812f4a0f380520f047768d`.

## Human Intent

Test whether the DDA can use a meeting as source context, define a bounded useful goal, delegate work across separate conversations, preserve the decision and evidence trace, obtain an independent verifier result, and reduce Emmanuel's manual coordination.

## Experiment Goal

Demonstrate that one root orchestrator can convert the July 14 meeting into one measurable DDA improvement goal, delegate at least two bounded tasks, reconcile the returns, obtain an independent verifier result, and produce a decision-ready scoreboard without Emmanuel directing every intermediate step.

## Hypothesis

If the DDA is organized around a measurable goal and a root orchestrator with bounded researcher, executor, and verifier lanes, then it will produce a more traceable and decision-ready result with fewer manual interventions than the current context-collection workflow.

## Scope

Included:

- goal definition;
- research and execution delegation;
- lane and evidence trace;
- independent verification;
- baseline comparison;
- review-only scoreboard;
- human decision.

Excluded:

- production frontend;
- autonomous external writes;
- PR or `main` promotion;
- runtime, automation, memory, skill, or eval activation;
- replacement of `dda-agent-ops`;
- permanent model-routing policy.

## Required Conversation Lanes

1. Root orchestrator.
2. Researcher.
3. Executor.
4. Independent verifier.

## Required Stages

### Stage 1 - Intent and Goal

- Extract candidate intents, directives, hypotheses, constraints, and open questions from the transcript.
- Select one goal.
- State why it is the highest-value bounded test.
- Name the human decision owner.

### Stage 2 - Measurement Contract

Define:

- success condition;
- failure condition;
- quality criteria;
- evidence requirements;
- time boundary;
- cost or token-burden boundary;
- allowed human interventions;
- escalation rule.

### Stage 3 - Plan and Delegation

- Produce a task plan.
- Delegate at least one research task and one execution task.
- Give each lane a bounded source set, permissions, acceptance criteria, and return format.
- Record every task in the conversation-lane ledger.

### Stage 4 - Returns and Reconciliation

- Collect the specialist returns.
- Identify conflicts and missing evidence.
- Reconcile the returns into one frozen candidate result.
- Record the exact artifact set and SHA when committed.

### Stage 5 - Independent Verification

- Give the verifier the frozen candidate, goal, criteria, and evidence set.
- Do not allow the verifier to modify the candidate during review.
- Require accepted, held, rework, or rejected with reasons and proof limitations.

### Stage 6 - Baseline Comparison

Compare the experiment with the current manual workflow on:

- human interventions;
- completion time;
- recovery burden;
- evidence coverage;
- goal traceability;
- defects found;
- output quality;
- next-action correctness;
- execution burden.

### Stage 7 - Scoreboard and Human Gate

The orchestrator returns:

- goal outcome;
- task status;
- evidence coverage;
- verifier result;
- unresolved holds;
- human interventions;
- burden score;
- baseline comparison;
- recommended next decision.

Emmanuel returns one human decision: accept the hypothesis, revise it, hold it, or reject it.

## Minimum Measures

| Measure | Definition |
|---|---|
| Goal clarity | Goal names observable outcome, constraints, and decision owner |
| Task traceability | Percentage of delegated tasks linked to the goal |
| Evidence coverage | Percentage of material claims linked to sources or produced evidence |
| Verifier defects | Number and severity of defects detected independently |
| Human interventions | Number of times Emmanuel must redirect intermediate work |
| Recovery burden | Time and artifact count needed to recover current state |
| Execution burden | Time, token, or cost estimate by lane |
| Next-action correctness | Whether the generated next action is accepted by the human reviewer |
| Material improvement | Whether the result is better than the manual baseline on agreed criteria |

## Pass Condition

Pass only if:

- one goal remains stable through the run;
- at least two bounded tasks are delegated and returned;
- the evidence trace is recoverable;
- the independent verifier can evaluate the frozen return;
- manual intervention is measured;
- the result materially improves on the baseline;
- human acceptance boundaries remain intact.

## Hold Conditions

Hold if:

- the goal changes without a recorded human decision;
- specialist tasks cannot be traced to the goal;
- the verifier is not independent;
- evidence or current truth cannot be recovered;
- the scoreboard measures activity rather than outcome;
- the experiment requires unapproved external writes or runtime changes.

## Required Return Artifacts

- experiment source index;
- goal and measurement contract;
- conversation-lane ledger;
- researcher task and return;
- executor task and return;
- orchestrator reconciliation;
- independent verifier return;
- baseline comparison;
- scoreboard;
- human decision record.

## Decision Required Before Execution

Emmanuel must approve, revise, hold, or reject this experiment goal and scope.
