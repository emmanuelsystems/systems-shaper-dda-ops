# Weekly Huddle Machine v0.1

Status: `candidate_review_only`

The Weekly Huddle Machine is a reusable operating system for Emmanuel and David's recurring weekly huddles. It is designed to turn each huddle into a repeatable cycle of state recovery, preparation, conversation, evidence extraction, decision/action reconciliation, routing, and durable carry-forward context.

This is not an autonomous decision system. Human review remains the acceptance gate.

## Purpose

The machine should make each weekly huddle easier to start, easier to review, and easier to continue the following week without rereading the full history.

The target experience is:

```text
Previous durable state
-> Pre-huddle recovery
-> Prep packet
-> Emmanuel + David huddle
-> Transcript intake
-> Evidence + workflow analysis
-> Decision/action reconciliation
-> Approved routing
-> Updated durable state
-> Next huddle
```

## Core Design Principle

Separate the reusable machine from each execution of the machine.

```text
weekly-huddle/
  = reusable protocol, templates, prompts, and state contract

weekly-huddle/runs/YYYY-MM-DD/
  = one execution of the machine
```

## Machine Stages

1. **Pre-huddle intake**
   - Load the previous accepted state.
   - Identify relevant changes since the previous huddle.
   - Collect only bounded sources needed for the current meeting.

2. **State recovery**
   - What changed?
   - What is still active?
   - What is blocked?
   - What needs a human decision?

3. **Huddle preparation**
   - Produce a short prep packet.
   - Surface decision questions, experiment status, open loops, and source gaps.

4. **Live huddle**
   - Emmanuel and David discuss, clarify intent, make decisions, and assign work.
   - The machine does not replace the human conversation.

5. **Transcript intake**
   - Freeze the exact transcript identity.
   - Separate primary meeting evidence from historical context.

6. **Reconciliation**
   - Extract confirmed decisions, proposed ideas, actions, owners, blockers, holds, experiments, and unresolved questions.
   - Distinguish direct evidence from interpretation and recommendation.

7. **Routing**
   - Prepare approved work for GitHub, Linear, Notion, Slack, or Codex only when explicitly authorized.
   - Do not treat routing recommendations as permission to write externally.

8. **Memory / next run**
   - Carry forward only the smallest durable state required for the next cycle.
   - Avoid using raw transcript history as the default memory mechanism.

## Standard Outputs Per Cycle

A mature run should be able to produce:

- `source-index.md`
- `state-snapshot.md`
- `pre-huddle-packet.md`
- `transcript-analysis.md`
- `decision-action-register.md`
- `routing-return.md`
- `next-huddle-state.md`

Not every early pilot must produce every artifact. v0.1 should prove the smallest useful repeatable cycle first.

## Human / Agent Responsibilities

### Emmanuel

- Owns evaluation standards and test scope.
- Confirms source boundaries.
- Reviews action ownership and implementation readiness.
- Approves any Codex execution packet before project changes begin.

### David

- Confirms intent and receiving-side usefulness.
- Makes or confirms decisions that require his authority.
- Accepts, revises, holds, or rejects candidate outputs when needed.

### Firstmate

- Recovers state.
- Coordinates bounded workers when session ownership is valid.
- Reconciles worker findings.
- Preserves approval boundaries.
- Does not merge or execute human decisions without authorization.

### Codex

- Performs bounded repo-local execution after explicit handoff.
- Produces reviewable artifacts and verification evidence.
- Does not convert recommendations into accepted decisions.

## Initial Worker Pattern

The first multi-agent version uses at most two scouts:

- **Transcript Evidence Scout**: decisions, actions, owners, blockers, unresolved questions, source evidence.
- **Workflow Audit Scout**: process friction, duplication, unclear authority, source gaps, and automation opportunities.

Firstmate reconciles both into one review packet.

## Acceptance Criteria for v0.1

The machine is useful when:

- A new huddle run can be initialized in under 5 minutes.
- The primary transcript and source boundary are explicit.
- Decisions are separated from proposals.
- Actions have owners or are explicitly unassigned.
- David decisions are separated from Emmanuel execution work.
- The post-huddle output creates useful next-huddle context.
- The same structure can be used for the next meeting without redesigning the workflow.
- No autonomous implementation is required to demonstrate value.

## Current Known Limitation

The current Codex-only Firstmate setup cannot yet verify primary session ownership through Firstmate's existing process-ancestry lock. Until that integration is fixed and tested, the machine can still be developed and exercised manually or in read-only mode, but Firstmate worker dispatch is not yet considered validated.

## v0.1 Build Scope

This branch establishes the reusable machine only:

- charter
- operating rules
- cycle protocol
- templates
- persistent state contract
- reusable start/process prompts
- a Cycle 001 reference scaffold based on the July 31 huddle

No automation, external routing, worker dispatch, or production implementation is claimed by this scaffold.
