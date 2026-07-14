---
title: July 14 MTA Next Action Items
asset_type: action_register
status: proposed_review_only
version: v0.1
owner: Emmanuel Olana
created: 2026-07-14
approval_status: not_approved
parent_sha: ff94794298acdd5dd0812f4a0f380520f047768d
candidate_sha: assigned_by_git_commit_containing_this_packet
github_path: runs/2026-07-14/next-action-items-v0.1.md
---

# July 14 MTA Next Action Items

## Priority Decision

The next work should not be another broad template expansion or production frontend build.

The highest-value next step is one bounded, review-only meeting-to-goal orchestration experiment that tests whether the DDA can convert intent into a measurable goal, delegate work, preserve evidence, obtain independent verification, and reduce Emmanuel's manual coordination.

## Priority 0 - Required Before the Experiment

| Owner | Action | Completion evidence | Status |
|---|---|---|---|
| Emmanuel | Define one bounded DDA optimization target | Goal statement names observable outcome, allowed actions, constraints, success, failure, and decision owner | Open |
| Emmanuel | Define what a successful run measures | Measurement contract covers outcome quality, evidence, time, burden, human interventions, and next-action correctness | Open |
| Emmanuel | Confirm the human decision boundary | Written list of decisions the orchestrator may propose versus decisions only a human may approve | Open |
| Emmanuel | Move project-specific Slack instructions out of global personalization | Project-level `AGENTS.md` contains the scoped rule; global instructions no longer constrain unrelated work | Directed; not verified by this packet |
| Emmanuel | Freeze the experiment source set | Source index names the transcript, Notion MTA, repo SHA, and applicable governance files | Proposed in this run packet |

## Priority 1 - Build the Minimum Conversation Loop

| Owner | Action | Completion evidence | Status |
|---|---|---|---|
| Emmanuel / Codex | Create one root orchestrator conversation contract | Contract defines planning, delegation, reconciliation, tracing, evaluation, and escalation duties | Open |
| Emmanuel / Codex | Create one researcher lane | Bounded task contract and evidence-return shape | Open |
| Emmanuel / Codex | Create one executor lane | Bounded implementation contract and completion-return shape | Open |
| Emmanuel / independent reviewer | Create one verifier lane | Verifier is separated from implementation and scores the frozen return against stated criteria | Open |
| Orchestrator | Maintain a conversation-lane ledger | Ledger records goal, task, owner, status, inputs, return, verifier result, and next action | Open |
| Orchestrator | Maintain goal-to-task-to-evidence lineage | Every returned claim and artifact can be traced to its parent goal and evidence | Open |

## Priority 2 - Run and Measure the Experiment

| Owner | Action | Completion evidence | Status |
|---|---|---|---|
| Orchestrator | Convert this meeting into one measurable goal | Goal is selected from candidate intents with rationale | Open |
| Orchestrator | Delegate at least two independent work lanes | Task packets include boundaries, source set, acceptance criteria, and return format | Open |
| Researcher / executor | Return work without Emmanuel directing each intermediate step | Returned packets record human interventions and escalation points | Open |
| Independent verifier | Evaluate the frozen return | Result is accepted, held, rework, or rejected for the stated scope | Open |
| Emmanuel | Compare with current manual baseline | Scorecard shows time, human interventions, evidence coverage, defects, and result quality | Open |
| Emmanuel | Make the human gate decision | Hypothesis is accepted, revised, held, or rejected | Open |

## Priority 3 - Explore the Interface Only After Measurement Exists

| Owner | Action | Completion evidence | Status |
|---|---|---|---|
| Emmanuel / design lane | Define the minimum scoreboard fields | Goals, tasks, evidence, verifier result, holds, burden, and next decision are represented | Open |
| Design lane | Produce a review-only wireframe | Wireframe uses real experiment data and does not claim production readiness | Open |
| Human reviewer | Decide whether a frontend prototype is justified | Decision cites the experiment results and measurement contract | Held until experiment evidence exists |

## David Follow-Ups

| Owner | Action | Completion evidence | Status |
|---|---|---|---|
| David | Resend or share the referenced custom instructions | Accessible source link or document | Promised; receipt not verified |
| David | Share the updated intent-to-prompt material | Accessible prompt or source artifact | Promised; receipt not verified |
| David | Provide a walkthrough or research artifact on his orchestration workflow | Follow-up recording, document, or repo evidence | Intended; timing not fixed |

## Research Inputs to Review

- Intent-to-Prompt Compiler material shared by David.
- Hamming's research and engineering principles, focusing on hypothesis, measurement, and important-problem selection.
- The orchestration articles, skills, and plugin examples shared during the meeting.
- Current Codex project-level instruction and conversation configuration.
- Actual usage and performance evidence before adopting model-routing policy.

## Holds

- Do not start a broad swarm before the minimum four-conversation loop is tested.
- Do not build a production frontend before the measurement contract exists.
- Do not treat a model-role example as approved configuration.
- Do not treat the MTA or this action register as an implementation verifier result.
- Do not promote `main`, accept infrastructure, or replace `dda-agent-ops` from this packet.

## Immediate Next Owner and Action

Owner: Emmanuel.

Action: approve or revise the single experiment goal in `meeting-to-goal-experiment-contract-v0.1.md` before any orchestration implementation begins.
