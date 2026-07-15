---
title: DDA Working Optimization Target
asset_type: optimization_target
status: defined_for_bounded_experiment_design
version: v0.1
owner: Emmanuel Olana
defined_by: Root Orchestrator
created: 2026-07-15
decision_owner: Emmanuel Olana
source_candidate_sha: 7437f21e0a5461ee559196f36f145cae41b4caa2
runtime_claim: none
canon_claim: none
---

# DDA Working Optimization Target

## Target

> Maximize the percentage of human-approved goal cycles that deliver a human-accepted, independently verified outcome on the first frozen candidate, while reducing time-to-outcome and human coordination burden, with zero permission or proof-boundary breaches.

This is the DDA's working optimization target for bounded experiment design. It measures goal outcomes, not the volume of conversations, tasks, documents, commits, or packets.

## Unit of Value

The primary unit is an **eligible goal cycle**.

- A meeting or conversation can supply intent, but is not the unit of value.
- A goal defines the observable outcome and decision boundary.
- Tasks are delegated execution units under the goal.
- A run folder is the evidence container.
- Independent verification evaluates the frozen outcome.
- The human decision closes the cycle.

An eligible goal cycle must begin with:

1. a human-approved goal with an observable, non-meta outcome;
2. explicit success, failure, hold, permissions, and decision owner;
3. a frozen source set or evidence-access rule;
4. verifier criteria tied to outcome quality, not packet completeness alone;
5. complete instrumentation beginning before delegation.

A packet whose main result is that the packet is complete does not count as a successful operational outcome.

## Primary Metric

### First-Pass Accepted Outcome Rate

```text
goal cycles whose first frozen candidate is independently accepted
and then human-accepted
-----------------------------------------------------------------
all eligible goal cycles started in the measurement window
```

The numerator requires both independent verification and the final human decision. A reworked candidate may later become accepted, but it does not count as first-pass success for the original cycle.

## Mandatory Guardrails

Every counted cycle must satisfy:

| Guardrail | Requirement |
|---|---:|
| Unauthorized external or runtime actions | `0` |
| Unapproved goal changes after freeze | `0` |
| Proof-boundary coverage | `100%` |
| Material-claim evidence coverage | At least `95%` |
| Goal-to-task traceability | `100%` |
| Required task-field completeness | `100%` |
| Independent verifier separation | Required |
| Final human decision | Required |

A faster result that violates a guardrail is not an improvement.

## Efficiency and Burden Measures

Measure these for every eligible cycle from the first intent timestamp:

1. time to approved goal;
2. time to first actionable delegated task;
3. time to first frozen candidate;
4. time to verifier verdict;
5. time to final human decision;
6. human coordination minutes;
7. human clarifications and redirections;
8. root scheduling interventions;
9. specialist returns and correction cycles;
10. verifier defects by severity.

Tool calls and token use are diagnostic cost measures. They are not outcome-quality substitutes.

## Week-Over-Week Improvement Rule

The next three eligible goal cycles form the prospective baseline window. Core time, coordination, intervention, correction, outcome, and decision fields may not be left `unknown` for those cycles.

After at least three baseline cycles and three comparison cycles, improvement may be claimed only when:

1. every mandatory guardrail passes;
2. first-pass accepted outcome rate does not decrease;
3. at least one of first-pass outcome rate, median time-to-final-decision, or median human-coordination minutes improves; and
4. neither of the other two measures worsens.

With fewer than three cycles in either window, report observations only. Do not claim learning or week-over-week improvement.

## Decision Rights

### Human-owned

- approve or revise the goal and evaluation criteria;
- set permissions and external-write boundaries;
- approve material goal changes after freeze;
- accept, revise, hold, or reject the final result;
- approve runtime, automation, skills, agents, frontend, infrastructure, canon, PR, or `main` promotion.

### Orchestrator-owned within the approved boundary

- interpret sources and propose the bounded plan;
- select the minimum necessary specialist lanes;
- create goal-linked tasks and route dependencies;
- track state, burden, conflicts, and evidence;
- freeze the candidate and dispatch independent verification;
- reconcile results and propose the next action;
- stop or hold work when a guardrail cannot be preserved.

## Minimum Trace

Every eligible cycle must preserve:

1. human intent and goal decision;
2. goal ID, observable outcome, measures, permissions, and owner;
3. frozen source/evidence rule;
4. plan and goal-linked task contracts;
5. specialist returns and intervention ledger;
6. frozen candidate SHA and manifest;
7. independent verifier result;
8. observed metric row;
9. final human decision;
10. next hypothesis or workflow change.

## EXP-02-R1 Classification

EXP-02-R1 is accepted as calibration evidence that the review-only orchestration sequence can become decision-ready after rework. It is not included as proof of operational improvement because:

- the objective was primarily a process packet;
- the original candidate required rework;
- manual baseline time and coordination measures were incomplete;
- no week-over-week comparison window exists.

## Next Measurement Action

Design the next experiment around one real, non-meta work outcome. Start instrumentation before goal approval and delegation. Use that cycle as baseline observation 1 of 3. Do not create a skill, permanent agent, automation, or frontend from this target until repeatability and measured improvement are independently supported.

## Proof Boundary

This is a human-directed working target for bounded experiment design. It is not validated operating policy, runtime configuration, canon, infrastructure approval, or evidence that the DDA has already improved.
