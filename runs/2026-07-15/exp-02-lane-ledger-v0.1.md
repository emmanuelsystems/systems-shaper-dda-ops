---
title: EXP-02 Lane Ledger
asset_type: conversation_lane_ledger
status: root_reconciled_candidate_freeze_pending
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
candidate_sha: pending
---

# EXP-02 Lane Ledger

| Lane | Logical task | Status | Required input | Expected return | Next action |
|---|---|---|---|---|---|
| Root | `EXP-02-ROOT` | candidate reconciled | Human authorization and frozen contracts | Reconciled candidate, manifest, final scoreboard | Freeze candidate |
| Researcher | `EXP-02-RESEARCH` | return qualified for dependency use | Frozen source set | Source-to-direction map, alternative goals, baseline, conflicts | Complete |
| Executor | `EXP-02-EXECUTE` | return qualified after one correction | Frozen goal plus qualified research | Execution candidate and executor return | Complete |
| Independent verifier | `EXP-02-VERIFY` | intake prepared, not dispatchable | Exact candidate SHA and frozen manifest | Scoped verdict and recomputed measures | Hold |

## Intervention Log

| Event | Counted | Effect |
|---|---|---|
| Human authorization to run EXP-02 and choose tasks/goals | No | Opens bounded setup and specialist execution |
| Researcher primary return | Yes | `3` tool calls, `0` clarifications, `0` corrections, `0` writes |
| Executor primary return | Yes | `19` tool calls through correction checks, `0` clarifications, `1` encoding-only correction, `0` external writes |

## Current Truth

- Goal, measures, source set, and specialist contracts are frozen.
- Researcher return is root-qualified for executor dependency use only.
- Executor return is root-qualified after one encoding-only correction.
- Root reconciliation is complete; candidate commit freeze is pending.
- Verifier waits for a frozen candidate and exact SHA.
- No final experiment result or human decision exists.
