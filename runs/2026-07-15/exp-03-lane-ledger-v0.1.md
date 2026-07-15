---
title: EXP-03 Lane and Instrumentation Ledger
asset_type: lane_ledger
status: setup_frozen_before_delegation
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-03-DDA-IMPLEMENTATION-DECISION-2026-07-15
baseline_observation: 1_of_3
---

# EXP-03 Lane and Instrumentation Ledger

## Lane State Before Delegation

| Lane | Logical task | State | Allowed return | Current gate |
|---|---|---|---|---|
| Root | `EXP-03-ROOT` | Goal and measurement contract frozen | Reconciliation, manifest, scoreboard, source-index update | Executor not yet dispatched |
| Executor | `EXP-03-EXECUTE` | Contract frozen; not yet dispatched | Decision brief and executor return only | Await dispatch |
| Verifier | `EXP-03-VERIFY` | Intake prepared; not dispatchable | Read-only verifier return only | Await exact candidate SHA |

## Prospective Event Ledger

| Event | Timestamp (+08:00) | Evidence | Burden / intervention note |
|---|---|---|---|
| T0 instrumentation begins | `2026-07-15T12:17:57.4045122+08:00` | Goal contract front matter | First deterministic timestamp after source recovery; before goal freeze/delegation |
| Goal freeze | `2026-07-15T12:19:08.0141500+08:00` | Final dispatch goal-contract SHA-256 `CE1D42B53726AFF3353D19214ADE566E9A8620204E5D327B7B7673EB180CB9A9` | No human clarification or redirection after T0 |
| First actionable task frozen | `2026-07-15T12:19:08.0141500+08:00` | Executor contract SHA-256 `46462EC4142C02FE9C6C772C91520939E89CA3AE992D4D27960367DFB7E8B979` | No delegation yet |
| Executor dispatch | pending | Lane task ID | Must follow completed setup freeze |
| Executor primary return | pending | Return file and lane result | Corrections start at zero |
| Candidate freeze | pending | Candidate commit SHA/timestamp and manifest | Must exclude dirty unrelated files |
| Verifier dispatch | pending | Lane task ID and exact candidate SHA | No verifier work before freeze |
| Verifier result | pending | Verifier return and result commit | Defects recorded by severity |
| Final human decision | pending | Human decision record | Human acceptance gate cannot be self-filled |

## Counters at Setup Freeze

| Measure | Value |
|---|---:|
| Post-T0 human coordination minutes | `0` |
| Human clarifications | `0` |
| Human redirections | `0` |
| Root scheduling interventions | `0` |
| Executor primary returns | `0` |
| Executor correction cycles | `0` |
| Verifier primary returns | `0` |
| Major verifier defects | `0` before review |
| Minor verifier defects | `0` before review |
| Unauthorized external/runtime actions | `0` |

Counters are prospective observations, not claims about pre-T0 orientation work.
