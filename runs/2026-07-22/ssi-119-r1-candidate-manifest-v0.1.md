---
title: SSI-119 R1 Correction Candidate Manifest
asset_type: candidate_manifest
status: ready_for_candidate_freeze
version: v0.1
owner: Emmanuel Olana
created: 2026-07-22
goal_id: SSI-119-R1
parent_sha: ef539a2fb52439fb824f7f85072d0437b1275389
approval_status: not_accepted
---

# SSI-119 R1 Correction Candidate Manifest

## Freeze Rule

The scoped commit containing this four-file packet freezes the SSI-119 R1 candidate. The immutable candidate SHA and candidate-bound links are supplied by the post-commit dispatch envelope. The detached verifier must read exact committed blobs and must not use a moving worktree or branch URL as evidence.

## Candidate File Hashes

All paths are relative to `runs/2026-07-22/`. Hashes are SHA-256 over the exact file bytes before the candidate commit.

| File | SHA-256 |
|---|---|
| `source-index.md` | `456AFA1FF71737113EF7C788E24F5D7A667D9FBFC2D1B9DC8C57A82D1F90EA5E` |
| `ssi-119-r1-correction-candidate-v0.1.md` | `02B38674BA66199000E52E98732EDBE7B94D852CB7BE72EFD5762CC8CECE7583` |
| `ssi-119-r1-verifier-intake-v0.1.md` | `3B1AF1879638B47026555C392637782E7092F62A155F66F5C868052B76AED087` |

This manifest omits its own hash. A file cannot embed its final SHA-256 without changing the bytes being hashed, so a self-hash would be recursive rather than independently verifiable.

## Exact Changed-Path Set

1. `runs/2026-07-22/source-index.md`
2. `runs/2026-07-22/ssi-119-r1-correction-candidate-v0.1.md`
3. `runs/2026-07-22/ssi-119-r1-candidate-manifest-v0.1.md`
4. `runs/2026-07-22/ssi-119-r1-verifier-intake-v0.1.md`

No completion packet or pre-meeting note is part of this freeze. Those are post-freeze reconciliation artifacts and remain uncreated.

## Proof Boundary

Manifest integrity proves only file identity for detached review. It does not prove acceptance, correctness of the reported Slack disposition, independent verification, CTR-01 repair, implementation, runtime readiness, automation, canon, promotion, PR, merge, `main`, push, external posting, or repository replacement.
