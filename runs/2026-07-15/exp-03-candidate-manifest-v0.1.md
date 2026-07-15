---
title: EXP-03 Candidate Manifest
asset_type: candidate_manifest
status: ready_for_candidate_commit
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-03-DDA-IMPLEMENTATION-DECISION-2026-07-15
candidate_sha: assigned_by_commit_containing_this_manifest
---

# EXP-03 Candidate Manifest

## Freeze Rule

The Git commit containing this manifest is the EXP-03 `candidate_sha`. The verifier must read only that commit, confirm the listed SHA-256 values, and avoid all moving worktree files. This manifest does not hash itself because including its own final hash would change the file.

## Candidate Files and Pre-Commit SHA-256

All paths are relative to `runs/2026-07-15/`.

| File | SHA-256 |
|---|---|
| `source-index.md` | `766E0F766957766636B90B439C874B264ADC71DDCCA170EAF7F0552EFF0B3F73` |
| `exp-03-human-authorization-v0.1.md` | `4C7CE8B57BD8A3CD54ADEAAA02486F8AA895C7CEA5532A84B27BD0140CC036A8` |
| `exp-03-goal-and-measurement-contract-v0.1.md` | `CE1D42B53726AFF3353D19214ADE566E9A8620204E5D327B7B7673EB180CB9A9` |
| `exp-03-executor-contract-v0.1.md` | `46462EC4142C02FE9C6C772C91520939E89CA3AE992D4D27960367DFB7E8B979` |
| `exp-03-independent-verifier-intake-v0.1.md` | `FB6B96333EC903CFFBE040712DAF332D824A8B1F2085088EF2BFE621FE32702D` |
| `exp-03-lane-ledger-v0.1.md` | `BAEA44E21833FE74AF21526C22604DA9901E4784BE40BCED8F623FD3991BFF81` |
| `exp-03-dda-implementation-decision-brief-v0.1.md` | `3F7D3C9AEF9B1054F72935D370A912448AE45BB76724B324A772312D4A72AE54` |
| `exp-03-executor-return-v0.1.md` | `5391879F36075FF203363ACFECA59A60D6C8AC24D3A46FB1880DAAD287CCE95F` |
| `exp-03-root-reconciliation-v0.1.md` | `222E8FF6DC753FB0474EDE8800F9112ABF43FB43FA81FAA2F9C54876DEFFCE9E` |

## Excluded Worktree State

The candidate excludes:

- pre-existing dirty `AGENTS.md`;
- all dirty and untracked `runs/2026-07-14/` files;
- unrelated current-truth-retrieval files under `runs/2026-07-15/`;
- any file not listed above or this manifest itself.

## Proof Boundary

The candidate commit is a local evidence freeze only. It does not create independent acceptance, human acceptance, validation, runtime readiness, automation, frontend, infrastructure, skill/eval or permanent-agent promotion, canon, PR, push, `main` promotion, repo replacement, learning, repeatability, or improvement.
