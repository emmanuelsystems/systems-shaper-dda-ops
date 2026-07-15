---
title: EXP-03 Goal and Measurement Contract
asset_type: goal_and_measurement_contract
status: frozen_before_delegation
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-03-DDA-IMPLEMENTATION-DECISION-2026-07-15
baseline_observation: 1_of_3
decision_owner: Emmanuel Olana
instrumentation_start: 2026-07-15T12:17:57.4045122+08:00
runtime_claim: none
---

# EXP-03 Goal and Measurement Contract

## Observable Goal

Produce one review-ready, source-backed implementation decision brief for Emmanuel and David that identifies the highest-value next DDA implementation outcome, states where to start, gives a bounded execution sequence with decision gates, and distinguishes actions supported now from actions that must remain held.

The decision brief, not the experiment packet, is the operational outcome.

## Selection Rationale

The July 14 evidence asks for a specific answer about the DDA's end goal, measurement model, tracing mechanism, and what to implement next. EXP-02-R1 was human-accepted only for bounded decision-readiness and then defined the working optimization target. The next highest-value supported step is to convert those accepted inputs into a usable implementation decision, without building unapproved software or promoting an unproven workflow.

## Permissions

Allowed:

- read the frozen local evidence set;
- write only EXP-03 review artifacts in `runs/2026-07-15/`;
- use one executor and one independent verifier;
- run deterministic local text, hash, Git, and consistency checks;
- create scoped local commits needed to freeze the candidate and verifier result.

Prohibited:

- external writes or connector writes;
- push, PR, `main`, runtime, automation, frontend, infrastructure, canon, repo replacement, skill/eval promotion, or permanent-agent promotion;
- edits or commits to pre-existing dirty `AGENTS.md` or `runs/2026-07-14/` files;
- unsupported external-source claims;
- self-acceptance by the executor, root, or verifier.

## Frozen Evidence Rule

The executor may use only these committed sources at parent commit `66f52f5f31dcb370645a52795ea9f6ec220b866c`:

1. `README.md`;
2. `docs/source-of-truth.md`;
3. `docs/source-authority-ladder.md`;
4. `runs/2026-07-15/source-index.md`;
5. `runs/2026-07-15/dda-optimization-target-v0.1.md`;
6. `runs/2026-07-15/exp-02-r1-human-decision-record-v0.1.md`;
7. `runs/2026-07-15/exp-02-r1-verifier-return-v0.1.md`;
8. `runs/2026-07-15/exp-02-r1-final-scoreboard-v0.1.md`;
9. `runs/2026-07-14/mta-analysis-v0.1.md` as stored in the parent commit;
10. `runs/2026-07-14/next-action-items-v0.1.md` as stored in the parent commit.

The July 14 worktree versions are excluded because they are dirty and moving. External Notion, Tactiq, and Slack sources are inherited context only and may not be represented as independently rechecked.

## Required Decision-Brief Contents

The candidate must contain:

1. the decision to be made and the evidence boundary;
2. one recommended next implementation outcome and why it outranks alternatives;
3. the exact starting point and first bounded action;
4. a short implementation sequence with owner, output, evidence, and gate for each step;
5. a current-now / held-now decision table;
6. measures and guardrails inherited from the accepted optimization target;
7. conflicts, unknowns, risks, and non-claims;
8. the next human decision in `accept`, `revise`, `hold`, or `reject` form;
9. a material-claim ledger with exact repo anchors.

## Success Conditions

EXP-03 reaches `decision_ready_pending_human_gate` only if:

- the first frozen candidate contains every required section;
- one recommendation is explicit and does not merely recommend producing more experiment paperwork;
- every execution step has owner, output, evidence, and gate;
- material-claim evidence coverage is at least `95%`;
- proof-boundary coverage is `100%`;
- goal-to-task traceability is `100%`;
- required task-field completeness is `100%`;
- unapproved goal changes are `0`;
- unauthorized external or runtime actions are `0`;
- an independent verifier returns `accepted` for decision-readiness against the exact frozen candidate;
- Emmanuel then makes the final human decision.

## Failure Conditions

The run fails if the candidate changes the frozen goal without human approval, recommends an unauthorized action as currently approved, lacks a usable implementation decision, fabricates evidence, violates verifier independence, edits unrelated dirty files, performs an external/runtime action, or overclaims improvement, validation, canon, or runtime readiness.

## Hold Conditions

Hold if the exact candidate cannot be frozen, the frozen sources conflict on a material decision without a bounded resolution, required evidence is unavailable, verifier independence is unavailable, or the final decision remains human-owned and pending.

## Prospective Instrumentation

All durations use `instrumentation_start` as T0. T0 is the first deterministic EXP-03 timestamp recorded after source recovery and before goal freeze or delegation; earlier orientation time is excluded and disclosed.

| Event / measure | Definition | Required evidence |
|---|---|---|
| T0 intent/instrumentation | First deterministic EXP-03 timestamp | This contract front matter and lane ledger |
| Time to goal | T0 to frozen goal-contract timestamp | Filesystem/Git timestamp plus ledger event |
| Time to first actionable task | T0 to frozen executor-contract timestamp | Executor contract hash plus ledger event |
| Time to frozen candidate | T0 to candidate commit timestamp | Candidate commit SHA and timestamp |
| Time to verifier result | T0 to verifier return timestamp | Verifier return and result commit |
| Time to final human decision | T0 to human decision timestamp | Human decision record; if pending, report elapsed censor time, not `unknown` |
| Human coordination minutes | Active post-T0 human clarification/redirection time only; initial intent excluded | Ledger entries; zero only if no post-T0 human exchange occurs |
| Human clarifications/redirections | Count of human messages that resolve ambiguity or change course | Ledger |
| Root scheduling interventions | Stop, resume, re-dispatch, or corrective routing action | Ledger with reason and effect |
| Specialist returns | Primary returns by lane | Lane task ID and return file |
| Correction cycles | Returned candidate changes after initial primary return | Ledger and diff/hash evidence |
| Verifier defects | Major/minor defects reported against the frozen candidate | Verifier return |
| Permission defects | Unauthorized action count | Git status, connector count, and verifier check |

## Baseline Rule

This is baseline observation 1 of 3. Report observed values only. One accepted result cannot establish repeatability, learning, or improvement. If the human decision is still pending, the observation remains open and time-to-final-decision is right-censored at the reporting timestamp.
