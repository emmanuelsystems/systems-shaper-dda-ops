---
title: EXP-03 DDA Implementation Decision Brief
asset_type: implementation_decision_brief
status: candidate_pending_independent_verification_and_human_gate
version: v0.1
owner: EXP-03 Executor
created: 2026-07-15
goal_id: EXP-03-DDA-IMPLEMENTATION-DECISION-2026-07-15
logical_task_id: EXP-03-EXECUTE
baseline_observation: 1_of_3
decision_owner: Emmanuel Olana
runtime_claim: none
external_write_claim: none
---

# EXP-03 DDA Implementation Decision Brief

## Decision and Evidence Boundary

### Decision to Make

Decide whether the next DDA implementation outcome should be the **manual, traced completion of two additional real, non-meta goal cycles using the frozen goal -> bounded execution -> frozen candidate -> independent verification -> human decision sequence**, so that baseline observations 2 and 3 are completed before any automation, frontend, permanent-agent, skill, eval, infrastructure, or runtime implementation is considered.

The operational output of each cycle must be the human-requested outcome. The run packet and metric row are supporting evidence, not the unit of value.

### Evidence Boundary

This brief uses only the ten sources frozen at parent commit `66f52f5f31dcb370645a52795ea9f6ec220b866c` by the EXP-03 goal contract, plus the EXP-03 authorization, goal contract, executor contract, and dispatch-state lane ledger at setup commit `17346a3707204566e228e2a621b67493483f5e4f`.

The July 14 sources were read from the parent commit, not from the dirty worktree. Notion, Tactiq, and Slack were not opened or rechecked. Their content is represented only through the limitations and summaries already preserved in the frozen repo artifacts.

## Recommended Next Implementation Outcome

### Recommendation

Implement the next two eligible DDA goal cycles as **manual, review-only, end-to-end traced operations** and use them as baseline observations 2 and 3. Keep the sequence and metric definitions fixed unless Emmanuel approves a material change. Each cycle must deliver one real outcome on its first frozen candidate where possible, obtain an independent verifier verdict, obtain Emmanuel's final decision, and preserve the complete observed metric row.

This is implementation of the operating loop, not a recommendation to produce more experiment paperwork. Contracts, ledgers, manifests, returns, and scoreboards exist only to make the real outcome and burden observable.

### Why This Outranks the Alternatives

1. The accepted working target makes an eligible goal cycle the unit of value and requires three prospective baseline cycles before any improvement claim. EXP-03 is only observation 1 of 3.
2. EXP-02-R1 established bounded decision-readiness after rework, but it did not establish first-pass operational success, reduced coordination, repeatability, learning, or runtime readiness.
3. The July 14 analysis calls for a goal-centered orchestration, tracing, verification, and improvement loop while retaining the repository as the evidence substrate.
4. Automation, frontend, skill/eval packaging, permanent agents, infrastructure, and runtime activation would encode or visualize a loop before stable baseline evidence exists. Those choices therefore remain held.

This ranking is an executor inference from the frozen sources. It is not a human approval.

## Exact Starting Point and First Bounded Action

### Starting Point

Start with the next human-authorized, real, non-meta outcome that can be completed entirely inside an explicitly stated permission boundary. Do not use a meeting, packet, document count, commit, or conversation as the goal merely because it is easy to measure.

### First Bounded Action

Before any delegation, the root presents Emmanuel with one candidate goal statement containing:

- the observable human outcome;
- the decision owner;
- allowed and prohibited actions;
- success, failure, and hold conditions;
- the frozen evidence-access rule;
- verifier criteria tied to outcome quality;
- T0 and every required time, burden, intervention, correction, defect, and permission field.

Emmanuel chooses `accept`, `revise`, `hold`, or `reject` for that goal. No specialist is dispatched until the accepted goal and complete instrumentation are frozen.

## Bounded Implementation Sequence

| Step | Owner | Output | Required evidence | Gate |
|---|---|---|---|---|
| 1. Select baseline goal 2 | Root proposes; Emmanuel decides | One observable, non-meta goal with owner, permissions, success/failure/hold conditions, evidence rule, verifier criteria, and T0 | Human authorization record and frozen goal contract | Emmanuel `accept`; otherwise revise, hold, or reject |
| 2. Execute the real outcome | One bounded executor selected by root | The requested operational outcome plus a burden/evidence return | Goal-linked task contract; files/calls/delegations log; claim-to-evidence anchors; intervention and correction record | Root confirms exact goal equality, allowed-output compliance, and complete required fields |
| 3. Freeze candidate 2 | Root | Exact candidate commit and manifest that exclude unrelated dirty files | Candidate SHA, hashes, commit timestamp, deterministic status/diff checks | Exact immutable candidate exists; otherwise hold |
| 4. Verify candidate 2 | Independent verifier | `accepted`, `rework`, `held`, or `rejected` decision-readiness verdict | Exact candidate SHA; outcome-quality criteria; defect severity; proof and permission checks | Verifier independence and exact-SHA review; otherwise hold |
| 5. Decide and record observation 2 | Emmanuel decides; root records | Human decision and complete observed metric row | Human decision record, verifier result, event ledger, elapsed/censored time | No self-acceptance; unresolved final decision remains open and right-censored |
| 6. Repeat unchanged for baseline goal 3 | Same role boundaries, with a new real goal | A second real outcome and baseline observation 3 | Same minimum trace and metric definitions | Any material method change requires Emmanuel's approval and explicit comparability note |
| 7. Close the baseline window | Root computes; verifier checks; Emmanuel decides | Three-row baseline summary with no improvement claim | Exact observed rows for cycles 1-3, defects, corrections, interventions, permission checks | Human decides whether a separately authorized comparison window is justified |

## Current-Now / Held-Now Decision Table

| Item | Decision now | Reason / gate |
|---|---|---|
| Use a real, non-meta goal as the operational output | `supported_now` | Required by the working target and EXP-03 authorization |
| Run baseline observations 2 and 3 manually with the same measurement model | `recommended_now_pending_human_acceptance` | Minimum evidence needed before a comparison or improvement claim |
| Root planning and bounded task routing | `supported_now_within_each_approved_goal` | Orchestrator-owned only inside the human-approved boundary |
| Local review artifacts and scoped local candidate/result commits | `supported_now` | Permitted evidence transport; not acceptance |
| Independent exact-SHA verification | `required_now` | Mandatory guardrail and source-authority rule |
| Human final `accept`, `revise`, `hold`, or `reject` | `required_now` | Acceptance remains human-owned |
| Week-over-week improvement, repeatability, or learning claim | `held` | Fewer than three baseline and three comparison cycles |
| Runtime activation or validated operating-policy claim | `held` | No runtime evidence or authorization |
| Automation | `held` | No repeatability or improvement evidence; explicitly prohibited in EXP-03 |
| Skill, eval, or permanent-agent creation/promotion | `held` | Working target says not to package before repeatability and measured improvement |
| Frontend or interactive scoreboard implementation | `held` | Measurement must stabilize before interface implementation |
| Infrastructure, canon, repo replacement, PR, `main`, or push | `held` | No human authorization; repo remains review-only |
| External Slack, Notion, Linear, Drive, Symphony, or other connector write | `held` | No external-write authorization |

## Measures and Guardrails

### Outcome Measure

For the three-cycle baseline, record whether the first frozen candidate was independently accepted and then human-accepted. Do not convert an accepted reworked candidate into first-pass success.

### Time and Burden Measures

For every cycle, record:

1. time from T0 to approved/frozen goal;
2. time from T0 to first actionable delegated task;
3. time from T0 to first frozen candidate;
4. time from T0 to verifier verdict;
5. time from T0 to final human decision, or elapsed censor time if pending;
6. active post-T0 human coordination minutes;
7. human clarifications and redirections;
8. root scheduling interventions;
9. specialist primary returns and correction cycles;
10. verifier defects by severity;
11. unauthorized external or runtime actions;
12. diagnostic tool-call cost without treating it as outcome quality.

### Mandatory Guardrails

| Guardrail | Requirement |
|---|---:|
| Unauthorized external or runtime actions | `0` |
| Unapproved goal changes after freeze | `0` |
| Proof-boundary coverage | `100%` |
| Material-claim evidence coverage | At least `95%` |
| Goal-to-task traceability | `100%` |
| Required task-field completeness | `100%` |
| Independent verifier separation | Required |
| Final human decision | Required to close a cycle |

A faster cycle that violates a guardrail is not an improvement. With fewer than three baseline cycles and three comparison cycles, report observed values only.

## Conflicts, Unknowns, Risks, and Non-Claims

### Conflicts and Resolution

- The July 14 action register marks setup actions open, while later July 15 artifacts accept EXP-02-R1 and define the working optimization target. Use the later human decision and accepted exact-SHA verifier result for current bounded decision-readiness; preserve the July 14 packet as proposed historical direction.
- The July 14 proposed minimum loop included multiple specialist examples, while the EXP-03 goal permits one executor and one independent verifier. Use the minimum lanes required by the currently authorized goal; do not treat the earlier role list as fixed architecture.

### Unknowns and Risks

- Numeric operational improvement remains unproven until the baseline and comparison windows exist.
- External-source freshness is unknown because Notion, Tactiq, and Slack were not rechecked.
- The best domain for baseline goals 2 and 3 is not established by the frozen sources; Emmanuel must authorize each real outcome.
- Manual tracing may impose overhead. Measure it rather than assuming it is worthwhile.
- Changing the method between baseline cycles could destroy comparability. Any material change requires a human decision and explicit disclosure.
- A complete evidence packet can still accompany a weak outcome. Verifier criteria must evaluate the operational output, not packet completeness alone.

### Non-Claims

This brief does not claim that the DDA has improved, learned, become repeatable, reduced human coordination, become runtime-ready, or established canon. It does not approve an external write, automation, frontend, infrastructure, skill/eval, permanent agent, PR, push, `main`, repo replacement, or promotion. It does not accept its own recommendation.

## Next Human Decision

Emmanuel decides one of:

- `accept`: adopt the manual traced goal-cycle sequence for baseline observations 2 and 3 within separately approved goal boundaries;
- `revise`: change the recommended implementation outcome, sequence, measures, or gates before use;
- `hold`: defer because a material source, authorization, independent verifier, or real goal is unavailable;
- `reject`: do not use this implementation direction.

An `accept` applies only to this bounded implementation direction. Each future real goal still requires its own human authorization and final human decision.

## Material-Claim Ledger

| ID | Material claim | Exact repo anchor | Coverage |
|---|---|---|---|
| C01 | This repository is review-only and is not accepted infrastructure or a replacement for `dda-agent-ops`. | `README.md` -> `Current Status`, `Human Approval Rules`, `Proof Boundary` at `66f52f5...` | Covered |
| C02 | Human review owns accepted/held/rework/rejected decisions; commit and push are transport, not acceptance. | `docs/source-of-truth.md` -> `Ownership Model`, `Rules`; `README.md` -> `Human Approval Rules` at `66f52f5...` | Covered |
| C03 | Exact-SHA human/verifier decisions outrank orientation sources but remain limited to their stated scope. | `docs/source-authority-ladder.md` -> `Claim Authority Order`, `SHA Rule` at `66f52f5...` | Covered |
| C04 | EXP-02-R1 was human-accepted only for bounded decision-readiness; improvement, runtime, and promotion claims remain excluded. | `runs/2026-07-15/exp-02-r1-human-decision-record-v0.1.md` -> `Accepted Scope`, `Recommended Follow-On Boundary` at `66f52f5...` | Covered |
| C05 | The R1 verifier accepted the frozen R1 packet with no decision-readiness defects, while preserving external-source and baseline limitations. | `runs/2026-07-15/exp-02-r1-verifier-return-v0.1.md` -> `Verdict and Scope`, `Defects and Burden Observations`, `Evidence Gaps and Proof Limitations` at `66f52f5...` | Covered |
| C06 | The working DDA target is first-pass independently verified and human-accepted goal outcomes with lower time and coordination burden and zero breaches. | `runs/2026-07-15/dda-optimization-target-v0.1.md` -> `Target`, `Primary Metric`, `Mandatory Guardrails` at `66f52f5...` | Covered |
| C07 | Eligible cycles require a real observable goal, explicit boundaries, frozen evidence rule, outcome-quality verification, and instrumentation before delegation. | `runs/2026-07-15/dda-optimization-target-v0.1.md` -> `Unit of Value` at `66f52f5...` | Covered |
| C08 | Three baseline and three comparison cycles are required before improvement may be claimed. | `runs/2026-07-15/dda-optimization-target-v0.1.md` -> `Week-Over-Week Improvement Rule`; `runs/2026-07-15/exp-03-goal-and-measurement-contract-v0.1.md` -> `Baseline Rule` at setup commit `17346a3...` | Covered |
| C09 | The July 14 direction is to move from repository-centered evidence toward goal-centered orchestration, tracing, verification, and improvement while keeping the repo as the evidence layer. | `runs/2026-07-14/mta-analysis-v0.1.md` -> `Executive Conclusion`, `Confirmed Direction`, `Summary` from the parent-commit object `66f52f5...` | Covered |
| C10 | A production frontend and broad swarm are premature; measurement and a bounded loop come first. | `runs/2026-07-14/next-action-items-v0.1.md` -> `Priority Decision`, `Priority 3`, `Holds` from the parent-commit object `66f52f5...`; `runs/2026-07-14/mta-analysis-v0.1.md` -> `Frontend Work Could Arrive Too Early` | Covered |
| C11 | EXP-03 authorizes a review-ready implementation decision brief and prohibits external/runtime/promotion actions. | `runs/2026-07-15/exp-03-human-authorization-v0.1.md` -> `Authorized Scope`, `Held Scope`; `runs/2026-07-15/exp-03-goal-and-measurement-contract-v0.1.md` -> `Permissions` at `17346a3...` | Covered |
| C12 | EXP-03 is baseline observation 1 of 3 and cannot prove improvement. | `runs/2026-07-15/exp-03-goal-and-measurement-contract-v0.1.md` -> front matter, `Baseline Rule` at `17346a3...` | Covered |
| C13 | The recommendation to run the same manual traced sequence for observations 2 and 3 is an executor inference, not a source-stated approval. | Inference from C04-C12; bounded by `runs/2026-07-15/exp-03-human-authorization-v0.1.md` -> `Human Gate` at `17346a3...` | Covered |

Material-claim coverage: `13/13`, `100%`.

Proof-boundary coverage: `100%`; every recommended action is either bounded as supported now or explicitly held, and the human acceptance gate is preserved.

Goal-to-task traceability: `100%`; this brief and the executor return trace to goal `EXP-03-DDA-IMPLEMENTATION-DECISION-2026-07-15` and logical task `EXP-03-EXECUTE`.
