---
title: David and Emmanuel Branch Reconciliation
asset_type: evidence_freeze
status: reconciled_read_only_candidate
version: v0.1
owner: Firstmate
created: 2026-08-06
---

# Compared heads

| Side | Branch | SHA | Date | Purpose |
|---|---|---|---|---|
| Common base | `codex/bootstrap-systems-shaper-dda-ops-20260706` | `66f52f5f31dcb370645a52795ea9f6ec220b866c` | 2026-07-15 | Default branch and shared ancestor |
| David | `codex/david-pmot-01-research-return-20260728` | `9a8a65f20658c3be2bb3b207768d539fafd0ee64` | 2026-07-28 | PMOT-01 research return |
| Emmanuel | `codex/emmanuel-pmot-01-contract-20260729` | `a46960c9c91529494b8f72f4475e65f667f3764` | 2026-07-29 | PMOT-01 contract and review package |

No merge, rebase, checkout, or branch write was performed.

## Common base

Both branches descend from `66f52f5f31dcb370645a52795ea9f6ec220b866c`.

The common base contains the repository governance, source authority, initial workflows, templates, references, and EXP-02-R1 evidence.

## Files changed on David's branch

David added the receiving-side entry point and eight PMOT/reconciliation artifacts:

- `START_HERE.md`
- `runs/2026-07-26/david-ssi-119-four-corrections-disposition-v0.1.md`
- `runs/2026-07-27/david-recovered-state-alignment-disposition-and-first-outcome-test-plan-v0.1.md`
- `runs/2026-07-27/pmot-01-revised-decision-paths-lane-authorization-and-execution-shape-v0.2.md`
- `runs/2026-07-27/pre-meeting-outcome-test-question-and-manual-baseline-v0.1.md`
- `runs/2026-07-27/source-index.md`
- `runs/2026-07-28/pmot-01-lane-contract-and-ledger-v0.1.md`
- `runs/2026-07-28/pmot-01-researcher-return-v0.1.md`
- `runs/2026-07-28/source-index.md`

The branch intent is receiving-side state recovery, correction disposition, manual-baseline comparison, lane authorization, research return, and path selection.

## Files changed on Emmanuel's branch

Emmanuel modified `AGENTS.md` and added the cumulative July 14 through July 29 contract, experiment, pre-meeting, validation, and PMOT package.

The July 29 PMOT additions are:

- `runs/2026-07-29/source-index.md`
- `runs/2026-07-29/pmot-01-transcript-to-goal-pilot-contract-v0.1.md`
- `runs/2026-07-29/recovered-state-independent-verification-request-decision-v0.1.md`
- `runs/2026-07-29/david-agent-alignment-prompt-v0.1.md`
- `runs/2026-07-29/emmanuel-july-29-gameplan-and-completion-v0.1.md`

The cumulative earlier additions include July 14 conversation and lane contracts, July 15 EXP-03 artifacts, July 17 decision closure material, July 22 SSI-119 artifacts, July 23 pre-meeting packets, and July 27 recovered-state validation packets.

The branch intent is Emmanuel-side preparation, exact source-manifest definition, contract packaging, execution boundaries, and a separate verifier request.

## Workflow differences

David's branch emphasizes a serial research protocol with a five-artifact limit, a manual comparator, a burden ledger, and an executor not released until gates pass.

Emmanuel's branch emphasizes a single exact PMOT source manifest, one bounded Goal Packet draft, strict stop conditions, and a separate David review before execution authorization.

The structures are compatible in sequence but are not yet reconciled into one accepted contract.

## Decision differences and conflicts

Both branches select `PILOT_NOW` as the recommended path toward a named transcript-to-goal-packet pilot.

David records execution as held pending data classification, scope, burden, manifest, and fresh authorization.

Emmanuel records the contract as a candidate pending David review and states that execution is not started.

This is a sequencing and gate-detail difference, not a direct contradiction about execution having occurred.

Both branches preserve the exclusions of CTR-01, SSI-120, historical-object publication, Outcome Launcher implementation, runtime action, and external writes outside explicit authorization.

## Unique useful material

David uniquely contributes the receiving-side `START_HERE` entry point, the four-correction disposition, the manual baseline, the lane authorization, the burden ledger, and the research return.

Emmanuel uniquely contributes the exact S1-S7 PMOT source manifest, first bounded action, stop condition, David review questions, execution authorization boundary, and separate verifier request.

## Pull-request relationships

GitHub reports zero pull requests for this repository, open or closed.

Therefore neither branch has a PR review, merge status, review thread, or accepted PR relationship to reconcile.

## Likely authoritative review head

No single head is authoritative for every purpose.

David's `START_HERE.md` is the strongest receiving-side entry point for alignment and hold state.

Emmanuel's `a46960c` is the latest dated contract package and is the strongest source for the proposed PMOT execution contract.

The correct current interpretation is a paired evidence set, not an accepted merge.

## Recommended PR base

Do not open a PR during this evidence freeze.

If a PR is later authorized, the mechanical base should be the GitHub default branch `codex/bootstrap-systems-shaper-dda-ops-20260706`, because no `main` branch or alternative integration base exists.

That base recommendation is a transport choice, not a claim that the default branch is the latest or most authoritative content.

## PMOT-01 disposition

Based only on available evidence, PMOT-01 is `PILOT_NOW` path-selected, contract-prepared, pending David review, and execution-held.

No evidence authorizes Cycle 001 execution, a Goal Packet run, external posting, a verifier dispatch, or implementation.

## Remaining holds

- David's disposition of Emmanuel's July 29 contract.
- Shared access to the primary transcript and exact source-manifest inputs.
- Data classification, burden baseline, and fresh execution authorization.
- Independent review and human disposition of the July 27 recovered-state candidate.
- Any PR, `main`, infrastructure, runtime, automation, canon, migration, or repository-role promotion.

## Decisions still required

- David: accept, revise, hold, or reject the PMOT-01 contract.
- Emmanuel: authorize or decline Cycle 001 after David's review.
- Emmanuel and David: select a durable integration base and decide whether a PR is warranted.
- Emmanuel and David: resolve any remaining source-access or burden assumptions.
