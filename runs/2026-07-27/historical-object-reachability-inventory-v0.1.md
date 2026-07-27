---
title: Historical Object Reachability Inventory
asset_type: evidence_inventory
status: candidate_evidence_frozen_historical_delivery_held
version: v0.1
owner: Emmanuel Olana
created: 2026-07-27
branch: codex/emmanuel-recovered-state-validation-20260727
parent_sha: b1e8e4bd006a455aac45db54cb4d1a1dba9515b0
candidate_sha: assigned_by_git_commit_containing_this_packet
approval_status: pending_human_review
delivery_status: committed_and_pushed_to_scoped_branch
external_write_claim: scoped_candidate_branch_push_only
---

# Historical Object Reachability Inventory

## Result

All five requested original commit objects exist in Emmanuel's local checkout.
None is contained by a current remote-tracking ref, and a fresh remote-head
check returned no head for any of their four named local branches.

Classification:

`local_original_remote_unreachable`

This is not object loss. It is a shared-delivery and provenance gap.

## Object Inventory

| Object | Parent | Subject | Local branch/ref | Remote head | Dependent claim |
|---|---|---|---|---|---|
| `2d6d1499811ec3fdcf0747514a8ae91e6d0e5f85` | `73ed7fad2a7b230ba88780a6dc23e6c866707451` | `run: revise EXP-03 outcome classification` | `codex/exp-03-classification-20260717` | none found | EXP-03 is `pre_baseline_meta_operational`; real-outcome baseline remains `0/3` |
| `ed0410f6033462eff9046bb0f72957fdaf2ca4c4` | `b472bd1d65b064c32fe22b44b2fe504f9e18be8a` | `run: prepare CTR-01-R1 retrieval correction` | `codex/current-truth-retrieval-r1-20260717`; ancestor of local verifier-result branch | none found | CTR-01-R1 candidate design and provenance |
| `ee379505cbcefb25f2a5fa9ec50dfcb6b1b37640` | `ed0410f6033462eff9046bb0f72957fdaf2ca4c4` | `run: record CTR-01-R1 verifier result` | `codex/current-truth-retrieval-r1-verifier-result-20260717` | none found | CTR-01-R1 correction completeness and design decision-readiness only |
| `d45d8d924be41396db0f541c5c0c0fbac668195e` | `73ed7fad2a7b230ba88780a6dc23e6c866707451` | `run: replay EXP cases with TOML routing policy` | `codex/exp-policy-rerun-20260717` | none found | Open-book TOML routing-policy replay candidate |
| `188b417a9a5405c266a4a3d0af279f59d87bf0be` | `d45d8d924be41396db0f541c5c0c0fbac668195e` | `run: record TOML replay verifier result` | `codex/exp-policy-rerun-20260717` | none found | Retrospective consistency only; no causal or runtime proof |

## Exact Changed Paths

### `2d6d1499811ec3fdcf0747514a8ae91e6d0e5f85`

- `runs/2026-07-17/codex-to-dda-exp-03-classification-completion-v0.1.md`
- `runs/2026-07-17/dda-to-codex-exp-03-classification-handoff-v0.1.md`
- `runs/2026-07-17/exp-03-human-classification-decision-v0.1.md`
- `runs/2026-07-17/source-index.md`

### `ed0410f6033462eff9046bb0f72957fdaf2ca4c4`

- `runs/2026-07-17/codex-to-dda-current-truth-retrieval-r1-completion-v0.1.md`
- `runs/2026-07-17/ctr-01-r1-source-index-v0.1.md`
- `runs/2026-07-17/ctr-01-verifier-return-reconciliation-v0.1.md`
- `runs/2026-07-17/current-truth-retrieval-layer-r1-candidate-v0.1.md`
- `runs/2026-07-17/current-truth-retrieval-layer-r1-real-data-fixture-v0.1.md`
- `runs/2026-07-17/current-truth-retrieval-layer-r1-verifier-intake-v0.1.md`
- `runs/2026-07-17/current-truth-retrieval-r1-candidate-manifest-v0.1.md`
- `runs/2026-07-17/human-decision-record-ctr-01-r1-authorization-v0.1.md`

### `ee379505cbcefb25f2a5fa9ec50dfcb6b1b37640`

- `runs/2026-07-17/ctr-01-r1-human-decision-record-v0.1.md`
- `runs/2026-07-17/ctr-01-r1-verifier-return-v0.1.md`
- `runs/2026-07-17/source-index.md`

### `d45d8d924be41396db0f541c5c0c0fbac668195e`

- `runs/2026-07-17/exp-02-r1-toml-policy-replay-return-v0.1.md`
- `runs/2026-07-17/exp-03-toml-policy-replay-return-v0.1.md`
- `runs/2026-07-17/source-index.md`
- `runs/2026-07-17/toml-policy-exp-replay-candidate-manifest-v0.1.md`
- `runs/2026-07-17/toml-policy-exp-replay-comparison-v0.1.md`
- `runs/2026-07-17/toml-policy-exp-replay-contract-v0.1.md`
- `runs/2026-07-17/toml-policy-snapshot-v0.1.md`

### `188b417a9a5405c266a4a3d0af279f59d87bf0be`

- `runs/2026-07-17/codex-to-dda-toml-policy-exp-replay-completion-v0.1.md`
- `runs/2026-07-17/source-index.md`
- `runs/2026-07-17/toml-policy-exp-replay-human-decision-record-v0.1.md`
- `runs/2026-07-17/toml-policy-exp-replay-verifier-return-v0.1.md`

## Remote-Reachability Check

Checked current GitHub heads for:

- `codex/exp-03-classification-20260717`;
- `codex/current-truth-retrieval-r1-20260717`;
- `codex/current-truth-retrieval-r1-verifier-result-20260717`;
- `codex/exp-policy-rerun-20260717`.

Result: no remote branch heads returned.

Immutable GitHub commit and blob links cannot be supplied yet without first
making the original objects remotely reachable. No substitute commits or
lookalike history were created.

## Claims Held from David's Decision Basis

- EXP-03 human classification as `pre_baseline_meta_operational` and its
  associated `0/3` real-outcome-baseline claim.
- CTR-01-R1 correction and verifier-result claims beyond the target lineage's
  `source-recovered/report-limited` statement.
- TOML replay retrospective consistency and verifier-result claims.

These claims can remain working local evidence, but they cannot be treated as
shared durable evidence until the exact originals are remotely reachable and
independently reviewed.

## Recovery Decision Required

Owner: Emmanuel for source preservation and proposed transport.

Human decision required before transport:

1. authorize exact existing branch publication, or choose another
   non-rewriting transport;
2. name the permitted remote branches/refs;
3. preserve original SHAs and parents;
4. verify remote reachability after transport;
5. submit the exact objects for independent review;
6. decide which dependent claims may re-enter the shared decision basis.

No push, ref move, rebase, history rewrite, or substitute reconstruction is
authorized by this inventory.
