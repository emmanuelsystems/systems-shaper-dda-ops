---
title: EXP-03 Lane and Instrumentation Ledger
asset_type: lane_ledger
status: verifier_accepted_human_gate_pending
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
| Root | `EXP-03-ROOT` | Verifier result reconciled | Scoreboard, result commit, source-index update | Await final human decision |
| Executor | `EXP-03-EXECUTE` | Primary return complete from task `/root/exp_03_executor` | Decision brief and executor return only | No correction requested |
| Verifier | `EXP-03-VERIFY` | `accepted` for decision-readiness only against `763ef60c3923cb2dbfaa7ed94f068bcfaf1b531a` | `exp-03-verifier-return-v0.1.md` | Complete; human gate pending |

## Prospective Event Ledger

| Event | Timestamp (+08:00) | Evidence | Burden / intervention note |
|---|---|---|---|
| T0 instrumentation begins | `2026-07-15T12:17:57.4045122+08:00` | Goal contract front matter | First deterministic timestamp after source recovery; before goal freeze/delegation |
| Goal freeze | `2026-07-15T12:19:08.0141500+08:00` | Final dispatch goal-contract SHA-256 `CE1D42B53726AFF3353D19214ADE566E9A8620204E5D327B7B7673EB180CB9A9` | No human clarification or redirection after T0 |
| First actionable task frozen | `2026-07-15T12:19:08.0141500+08:00` | Executor contract SHA-256 `46462EC4142C02FE9C6C772C91520939E89CA3AE992D4D27960367DFB7E8B979` | No delegation yet |
| Executor dispatch | `2026-07-15T12:21:01.2452534+08:00` | Task `/root/exp_03_executor`; setup commit `17346a3707204566e228e2a621b67493483f5e4f` | Occurred after setup freeze; no contract change |
| Root scheduling check | `2026-07-15T12:24:11.9575027+08:00` | Message to `/root/exp_03_executor` after no allowed output was visible | One intervention; requested prompt completion without changing goal, sources, outputs, or criteria |
| Executor primary return | `2026-07-15T12:24:21.5571604+08:00` | `exp-03-dda-implementation-decision-brief-v0.1.md`; `exp-03-executor-return-v0.1.md`; task `/root/exp_03_executor` | One primary return; zero post-return correction cycles |
| Candidate freeze | `2026-07-15T12:26:32+08:00` | Commit `763ef60c3923cb2dbfaa7ed94f068bcfaf1b531a`; `exp-03-candidate-manifest-v0.1.md` | Exact commit excludes dirty unrelated files |
| Verifier dispatch | `2026-07-15T12:26:41.2293069+08:00` | Task `/root/exp_03_verifier`; exact candidate `763ef60c3923cb2dbfaa7ed94f068bcfaf1b531a` | Dispatch followed candidate freeze |
| Verifier scheduling check | `2026-07-15T12:30:26.4653341+08:00` | Message to `/root/exp_03_verifier` after no return file was visible | One additional intervention; requested prompt same-contract verdict or hold without changing candidate or criteria |
| Verifier immediate status request | `2026-07-15T12:33:35.4947722+08:00` | Verifier replied that all material checks passed and the return was being written | Counted conservatively as a third root scheduling intervention; no review change |
| Verifier result | `2026-07-15T12:33:25.2415178+08:00` | `exp-03-verifier-return-v0.1.md`; task `/root/exp_03_verifier`; verdict `accepted`; result commit `2e80b24c6fb0609a940209a8cfb42a96e9030da7` | Root uses visible return-file time; verifier internal review end was `12:32:34.4840235+08:00` |
| Final human decision | pending; right-censored at `2026-07-15T12:34:17.9846283+08:00` | `exp-03-human-decision-record-v0.1.md` | Elapsed censor time `980.580 s`; human acceptance gate cannot be self-filled |

## Counters at Setup Freeze

| Measure | Value |
|---|---:|
| Post-T0 human coordination minutes | `0` |
| Human clarifications | `0` |
| Human redirections | `0` |
| Root scheduling interventions | `3` |
| Executor primary returns | `1` |
| Executor correction cycles | `0` |
| Verifier primary returns | `1` |
| Major verifier defects | `0` |
| Minor verifier defects affecting decision-readiness | `0` |
| Unauthorized external/runtime actions | `0` |

Counters are prospective observations, not claims about pre-T0 orientation work.
